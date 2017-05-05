---
layout: post
title: "Message encodings"
date: 2018-05-04 16:52:00
categories: misc
---

### Message 1 : Initial client connection attempt

Used during initial client connection. Helps server check client version compatibility.

| Byte  | Type    | Value       | Description                          | 
|:------|:-------:|:-----------:|-------------------------------------:|
| 0-3   | u32     | 7 | Size of message in bytes        |
| 4     | u8      | 10 | Message type |
| 5     | u8      | _major client number_ | Major client version number |
| 6     | u8      | _minor client number_ | Minor client version number |

### Message 2: Initial server response

Server tells client if connection was accepted and what name of server is.

| Byte  | Type    | Value       | Description                          | 
|:------|:-------:|:-----------:|-------------------------------------:|
| 0-3   | u32     | 6         | Size of message in bytes             |
| 4     | u8      | 11        | Message type                         |
| 5     | u8      | _code_      | Connection status (see table under)  |

#### Connection status codes
* 0 Connection denied
* 1 Connection accepted
* 2 Connection error, wait for generic error message.

### Message 3: Start of world sync

Message used by server to tell client a full level sync will occur. Server sends the name of the given world. The world name is limited to 32 8-bit ASCII chars.

| Byte  | Type    | Value       | Description                          | 
|:------|:-------:|:-----------:|-------------------------------------:|
| 0-3   | u32     | 42         | Size of message in bytes             |
| 4     | u8      | 12        | Message type                         |
| 5-8   | u32     | 32 | Size of the world name string      |
| 9-41  | Str      | _name_     | World name as ASCII string  |

### Message 4: World sync

Server send a chunk update to client.

| Byte  | Type    | Value       | Description                          | 
|:------|:-------:|:-----------:|-------------------------------------:|
| 0-3   | u32     | 36         | Size of message in bytes             |
| 4     | u8      | 13        | Message type                         |
| 5-8   | u32     | _x_         | Chunk x-cord                         |
| 9-12  | u32     | _y_         | Chunk y-cord                         |
| 13-16 | u32     | _width_     | Chunk width                          |
| 17-20 | u32     | _height_    | Chunk height                         |
| 21-35 | u8[]    | _chunk data_ | Chunk data as 128*128 bytes         |

### Message 5: World synch done

Server has provided all chunks to client.

| Byte  | Type    | Value       | Description                          | 
|:------|:-------:|:-----------:|-------------------------------------:|
|0-3    | u32     | 5         | Size of message in bytes             |
| 4     | u8      | 14        | Message type                         |
