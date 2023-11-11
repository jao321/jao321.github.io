---
layout: blog
title: Blog
permalink: /blog/
---
<div class="finder-right"> 
      {%- for post in site.posts -%}
        {% assign pdate = post.date |  date: "%m/%Y" %}
        {%  assign current = site.time | date: "%m/%Y" %}
        {% if pdate ==  current %} 
            <a class="post-link" href="{{ post.url | relative_url }}">
            <img src="{{ post.thumbnail }}" 
                style="display: block;
                        height: 50px;
                        margin-left: auto;
                        margin-right: auto;
                        border: solid black 2px;"/>
            {{ post.filename | escape }}
            </a>
        {% endif %}
      {%-endfor-%}
    </div>