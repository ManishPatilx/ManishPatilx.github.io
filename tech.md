---
layout: single
title: "tech"
collection: tech
permalink: /tech/
---

Books I have read and My two cents on them.

---

{% assign sorted = (site.books | sort: 'date') | reverse %}

<div class = "posts__scribbles">
{% for item in sorted %}
<div class="list__item">
  <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork">
    <h2 class="archive__item-title" itemprop="headline">
        <a href="{{ item.url }}" rel="permalink">{{ item.title }}</a>
    </h2>
    </article>
</div>
  {% endfor %}
</div>
