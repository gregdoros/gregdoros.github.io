---
layout: default
title: Nauka pythona & djano!
---

<!-- Get the tag name for every tag on the site and set them
to the `site_tags` variable. -->
{% capture site_tags %}{% for tag in site.tags %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}

<!-- `tag_words` is a sorted array of the tag names. -->
{% assign tag_words = site_tags | split:',' | sort %}

<div id="articles">
  <h1>Artykuły</h1>

  <!-- List of all tags -->
  <ul class="tags">
    {% for item in (0..site.tags.size) %}{% unless forloop.last %}
      {% capture this_word %}{{ tag_words[item] }}{% endcapture %}
      <li>
        <a href="#{{ this_word | cgi_escape }}" class="tag">{{ this_word }}
          <span>({{ site.tags[this_word].size }})</span>
        </a>
      </li>
    {% endunless %}{% endfor %}
  </ul>

  <!-- Posts by Tag -->
  <div>
    {% for item in (0..site.tags.size) %}{% unless forloop.last %}
      {% capture this_word %}{{ tag_words[item] }}{% endcapture %}
      <h2 id="{{ this_word | cgi_escape }}">{{ this_word }}</h2>
      {% for post in site.tags[this_word] %}{% if post.title != null %}
        <div>
        <span class="date">{{ post.date | date_to_string }}</span>
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p class="description">{% if post.description %}{{ post.description  | strip_html | strip_newlines | truncate: 120 }}{% else %}{{ post.content | strip_html | strip_newlines | truncate: 120 }}{% endif %}</p>
        </div>
        <div style="clear: both;"></div>
      {% endif %}{% endfor %}
    {% endunless %}{% endfor %}
  </div>
