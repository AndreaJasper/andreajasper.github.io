---
layout: page
title: "The Ledger"
icon: fa fa-book
order: 2
---

<div id="page-category">
  <div class="ps-lg-2">
    <p><i>A record of progress.</i></p>
    <p>The Ledger is where I document what I've been learning, building, reading, and exploring each week. These entries are intentionally simple—a running account of small wins, completed projects, courses, books, applications, and everything else that contributes to forward motion.</p>
    <p>Think of it as proof that growth is happening, even when it feels slow.</p>
  </div>
  <ul class="content ps-0">
    {% for post in site.categories['The Ledger'] %}
      <li class="d-flex justify-content-between px-md-3">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="dash flex-grow-1"></span>
        {% include datetime.html date=post.date class='text-muted small text-nowrap' lang=lang %}
      </li>
    {% endfor %}
  </ul>
</div>