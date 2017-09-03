---
permalink: /portfolio/
author_profile: false
excerpt: "Portfolio"
layout: splash
---

{% include base_path %}

{% include toc %}

{% for post in site.portfolio %}
    {% if page.title %}<meta itemprop="headline" content="{{ page.title | markdownify | strip_html | strip_newlines | escape_once }}">{% endif %}
    {% if page.excerpt %}<meta itemprop="description" content="{{ page.excerpt | markdownify | strip_html | strip_newlines | escape_once }}">{% endif %}
    {% if page.date %}<meta itemprop="datePublished" content="{{ page.date | date: "%B %d, %Y" }}">{% endif %}
    {% if page.last_modified_at %}<meta itemprop="dateModified" content="{{ page.last_modified_at | date: "%B %d, %Y" }}">{% endif %}

    <section class="page__content" itemprop="text">
      {{ content }}
    </section>

{% endfor %}




## Test 1

Test111

##  Hello world

hihi


<!--
<div class="grid__wrapper">
  {% for post in site.portfolio %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>
-->
