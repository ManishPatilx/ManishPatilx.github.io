---
title: posts
layout: single
permalink: /posts/
collection: posts
entries_layout: grid
classes: wide
author_profile: true
---

{% assign sorted = (site.posts | sort: 'date') | reverse %}
{% for item in sorted %}
<div class="grid__item">
 {% assign cover = item.url | split: "/" %}
  <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork">
      <div class="archive__item-teaser">
        <img src="/assets/images/pp.png" alt="">
      </div>
    <h2 class="archive__item-title" itemprop="headline">
        <a href="{{ item.url}}" rel="permalink">{{ item.title }}
</a>
    </h2>
  </article>
</div>
{% endfor %}
