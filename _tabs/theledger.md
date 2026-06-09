---
# layout: categories
title: The Ledger
categories: ["The Ledger"]
icon: fas fa-stream
order: 1
---
<section>
    <p>This is my running record of progress.</p>
    <p>
    Not polished articles. Not carefully crafted insights. Just a simple account of what I've been learning, building, studying, applying for, and exploring along the way.</p>
    <p>Some weeks will be packed with milestones. Others will be filled with small steps that barely seem worth mentioning. Both matter.</p>
    <p>The Ledger exists to document the journey as it happens and to remind myself that progress is often easier to see in hindsight than in the moment.</p>
    <p>Every entry is a deposit toward the future I'm building.</p>
</section>

<section>
    <ul>
    {% for post in site.categories['The Ledger'] %}
    <li>
        <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
    </ul>
</section>
