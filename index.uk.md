---
layout: default
ref: index
lang: uk
permalink: /uk/
---

<div class="home">

  <h1 class="page-heading">Дописи</h1>

  <ul class="post-list">
    {% assign posts=site.posts | where:"lang", page.lang %}
    {% for post in posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">отримувати оновлення через <a href="{{ "/feed.uk.xml" | prepend: site.baseurl }}">feed RSS</a></p>

</div>
