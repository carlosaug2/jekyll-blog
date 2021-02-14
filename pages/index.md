---
layout: home
title: 
permalink: /
section: home
intro_paragraph: >

---

<section>
<ul>
    {% for post in site.posts %}
    {% assign author = site.data.authors[post.author] %}
      <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
        <time datetime="{{ post.date }}">
          <small>
            <strong>{{ post.date | date_to_string }}</strong>
            {% if author %}
              by {{ author.name }}
            {% endif %}
          </small>
        </time>
        {{ post.excerpt | strip_newlines | truncate: 180 }}
      </li>
    {% endfor %}
  </ul>
  <section>
