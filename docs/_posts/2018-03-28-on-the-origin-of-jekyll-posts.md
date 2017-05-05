---
layout: post
title: "On the origin of jekyll posts"
date: 2018-03-28 15:00:00
categories: misc
---

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `bundle exec jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby linenos %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

$$\sum_{x=0}^{100}{\sum_{y=0}^{100}{f_{xy} + f_{yx}}}$$

{% highlight python linenos %}

if __name__ == '__main__':
    # Initial probability vector
    initial_prob = np.array([[0.6],[0.4]])
    
    # Transition probability matrix
    trans_prob = np.array([[0.7, 0.3],
                           [0.4, 0.6]])
    
    # Emission probability matrix
    obs_prob = np.array([[0.1, 0.4, 0.5],
                         [0.6, 0.3, 0.1]])
    
    hmm = HMM(initial_prob=initial_prob, trans_prob=trans_prob,obs_prob=obs_prob)
    observations = [0, 1, 1, 2, 1]
    
    with tf.Session() as sess:
        prob = forward_algorithm(sess, hmm, observations)
        print('Probability of observing {} is {}'.format(observations, prob))
{% endhighlight %}

* item 1
* item 2
* item 3
* item 4

## We will also be testing some headers

### We will also be testing some headers

#### We will also be testing some headers

##### We will also be testing some headers

###### We will also be testing some headers

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/