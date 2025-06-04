---
layout: default
datatable: true
---
# Latest Releases

<table id="releases" class="display">
    <thead>
        <tr>
            <th style="width:90px;">Image</th>
            <th>Novel</th>
            <th>Date</th>
        </tr>
    </thead>
    <tbody>
        {% for post in site.posts %}
        <tr>
            <td>
                {% if post.image %}
                    <img src="{{ post.image }}" style="width:80px; height:auto; display:block;">
                {% endif %}
            </td>
            <td>
                <strong style="font-size: 1.2em;"><a href="{{ post.url }}">{{ post.title }}</a></strong><br>
                {{ post.excerpt }}
            </td>
            <td>
                <small>{{ post.date | date: "%-d %B %Y" }}</small>
            </td>
        </tr>
        {% endfor %}
    </tbody>
</table>