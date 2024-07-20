---
title: "Papers"
layout: post
---

{% for paper in site.data.papers %}
<section class="paper">
    <h2>{{ paper.title }}</h2>
    <p class="year">{{ paper.year }}</p>
    <p class="description">{{ paper.description }}</p>
    <ul class="authors">
        {% for author in paper.authors %}
        <li>{{ author }}</li>
        {% endfor %}
    </ul>
    
    <ul class="links">
        <li><a href="{{ paper.paper_url }}" class="paper-link">Paper</a></li>
        {% if paper.source_code_url %}
        <li><a href="{{ paper.source_code_url }}" class="code-link">Source Code</a></li>
        {% endif %}
    </ul>
    
    <ul class="tags">
        {% for tag in paper.tags %}
        <li>{{ tag }}</li>
        {% endfor %}
    </ul>
</section>
{% endfor %}
