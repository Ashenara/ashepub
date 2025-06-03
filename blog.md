---
layout: default
title: Blog
---
# Latest Posts

<ul>
  {% for post in site.posts %}
    <li style="list-style: none; margin-left: -30px; margin-bottom: 20px; display: flex; align-items: flex-start;">
      {% if post.image %}
        <div style="flex: 0 0 80px; margin-right: 15px;">
          <img src="{{ post.image }}" style="width:80px; height:auto; display:block;">
        </div>
      {% endif %}
      <div style="flex: 1;">
        <small style="display:block; text-align:left;">{{ post.date | date: "%-d %B %Y" }}</small>
        <strong style="font-size: 1.2em;"><a href="{{ post.url }}">{{ post.title }}</a></strong>
        {{ post.excerpt }}
      </div>
    </li>
  {% endfor %}
</ul>


