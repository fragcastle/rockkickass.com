---
layout: page
title:
---
{% include JB/setup %}

<br />
<br />
<br />
<br />
{% for post in site.posts limit:6 %}
  {% assign author = site.authors[page.author] %}
 <div class='post '>
  <div class="post-inner">
    <div class='date'>
      <span class="day">{{ post.date | date: "%d" }}</span>
      <span class="month">{{ post.date | date: "%B, %Y" }}</span>
    </div>

    <h3>
      <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    </h3>
    {{ post.content }}
  </div>
</div>
{% endfor %}
