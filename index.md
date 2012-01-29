---
layout: page
title: Fancy Title!
---
{% include JB/setup %}

{% for post in site.posts limit:1 %}
<h2>
    <a href="{{ BASE_PATH }}{{ post.url }}" rel="bookmark" title="Permanent link to ">{{ post.title }}</a>
</h2>
<span>{{ post.date | date: '%B' }} {{ post.date | date: '%e' }}, {{ post.date | date: '%Y' }}</span>
<p>
    {{ post.content }}
</p>
{% endfor %}

<h3>Most recent entries</h3>
{% for post in site.posts limit:4 %}
<h4>
    <a href="{{ BASE_PATH }}{{ post.url }}" rel="bookmark" title="Permanent link to ">{{ post.title }}</a>
</h4>
<span>{{ post.date | date: '%B' }} {{ post.date | date: '%e' }}, {{ post.date | date: '%Y' }}</span>
{% endfor %}
