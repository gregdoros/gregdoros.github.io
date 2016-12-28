---
layout: default
title: About Long Haul
---

<!-- Get the tag name for every tag on the site and set them
to the `site_tags` variable. -->
{% capture site_tags %}{% for tag in site.tags %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}

<!-- `tag_words` is a sorted array of the tag names. -->
{% assign tag_words = site_tags | split:',' | sort %}

<div class="post">

  <!-- Posts by Tag -->
  <div>
    {% for item in (0..site.tags.size) %}{% unless forloop.last %}
      {% capture this_word %}{{ tag_words[item] }}{% endcapture %}
      <h2 id="this_word | cgi_escape }}">tag: {{ this_word }}</h2>
      {% for post in site.tags[this_word] %}{% if post.title != null %}
	        <h3><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
	        <p class="description">{% if post.description %}{{ post.description | strip_html | strip_newlines | truncate: 100 }}{% else %}{{ post.content | strip_html | strip_newlines | truncate: 100 }}{% endif %}</p>
        <div style="clear: both;"></div>
      {% endif %}{% endfor %}
    {% endunless %}{% endfor %}
  </div>
