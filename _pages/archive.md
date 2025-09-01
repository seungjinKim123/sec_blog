---
layout: page
title: 전체 글 목록
subtitle: 모든 포스트를 시간순으로 보기
description: 블로그의 모든 글을 카테고리별, 시간순으로 정리했습니다
show_sidebar: false
---

## 📋 전체 글 목록

{% for post in site.posts %}
  {% assign currentyear = post.date | date: "%Y" %}
  {% assign previousyear = post.previous.date | date: "%Y" %}
  
  {% if currentyear != previousyear %}
  ## {{ currentyear }}
  {% endif %}
  
  **{{ post.date | date: "%m-%d" }}** - [{{ post.title }}]({{ post.url }}) 
  {% if post.categories.size > 0 %}
  `{{ post.categories | join: ", " }}`
  {% endif %}
{% endfor %}