---
layout: blog
title: "Hack"
permalink: /oldblog/hacking/
---

<ul class="posts">
    {% for sanatana in site.categories.hacking %}
        <li>
            <span class="post-date">{{ sanatana.date | date: "%b %d, %Y" }}</span>
            ::
            <a class="post-link" href="{{ sanatana.url }}">{{ sanatana.title }}</a>
            @ {
            {% assign tag = sanatana.tags | sort %}
            {% for category in tag %}<span><a href="{{ site.baseurl }}category/#{{ category }}" class="reserved">{{ category }}</a>{% if forloop.last != true %},{% endif %}</span>{% endfor %}
            {% assign tag = nil %}
            }
        </li>
    {% endfor %}
</ul>
