---
layout: single
title: "books"
collection: books
permalink: /books/
---

My public journal. I post here every week.

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
