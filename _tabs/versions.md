---
layout: page
title: "Versions"
icon: fas fa-circle-user
order: 4
---

<div id="page-category">
  <div class="ps-lg-2">
    <p><i>Stories from the current version of me.</i></p>
    <p>Life rarely changes all at once. Versions is where I share personal reflections, career transitions, milestones, challenges, and the experiences that shape who I'm becoming.</p>
    <p>These posts capture the evolving nature of growth and the reality that we're all works in progress.</p>
  </div>
  <ul class="content ps-0">
    {% for post in site.categories['Versions'] %}
      <li class="d-flex justify-content-between px-md-3">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="dash flex-grow-1"></span>
        {% include datetime.html date=post.date class='text-muted small text-nowrap' lang=lang %}
      </li>
    {% endfor %}
  </ul>
</div>