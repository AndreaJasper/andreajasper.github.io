---
layout: page
title: "Side Quests"
icon: fas fa-scroll
order: 4
publish: false
---

<div id="page-category">
  <div class="ps-lg-2">
    <p><i>Because not everything needs a purpose.</i></p>
    <p>Books, games, coffee shops, creative projects, adventures, hobbies, and the countless interests that don't fit neatly anywhere else.</p>
    <p>Side Quests celebrates the distractions, detours, and passions that make life more interesting. Not everything needs to advance a career or achieve a goal. Sometimes it's enough that something is enjoyable.</p>
  </div>
  <ul class="content ps-0">
    {% for post in site.categories['Side Quests'] %}
      <li class="d-flex justify-content-between px-md-3">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="dash flex-grow-1"></span>
        {% include datetime.html date=post.date class='text-muted small text-nowrap' lang=lang %}
      </li>
    {% endfor %}
  </ul>
</div>