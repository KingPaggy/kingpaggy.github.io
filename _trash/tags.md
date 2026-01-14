---
layout: page
title: Tags
permalink: /tags/
---

<div class="tags-expo">
  <div class="tags-expo-list">
    {% for tag in site.tags %}
    <a href="#{{ tag[0] | slugify }}" class="post-tag">{{ tag[0] }} <span class="tag-count">({{ tag[1].size }})</span></a>
    {% endfor %}
  </div>
  <hr/>
  <div class="tags-expo-section">
    {% for tag in site.tags %}
    <h2 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h2>
    <ul class="tags-expo-posts">
      {% for post in tag[1] %}
      <li>
        <a class="post-title" href="{{ post.url | relative_url }}">
          {{ post.title }}
        </a>
        <span class="post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
      </li>
      {% endfor %}
    </ul>
    {% endfor %}
  </div>
</div>

<style>
.tags-expo-list {
  margin-bottom: 24px;
}
.post-tag {
  display: inline-block;
  padding: 4px 12px;
  margin: 4px;
  background: #f0f0f0;
  border-radius: 999px;
  text-decoration: none;
  color: #333;
  font-size: 14px;
  transition: all 0.2s;
}
.post-tag:hover {
  background: #007bff;
  color: white;
  text-decoration: none;
}
.tag-count {
  font-size: 12px;
  opacity: 0.8;
}
.tags-expo-posts li {
  margin-bottom: 8px;
}
</style>
