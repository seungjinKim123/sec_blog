---
layout: page
title: 보안 뉴스
subtitle: 최신 보안 트렌드와 뉴스 정리
description: 보안 업계의 최신 동향과 중요한 뉴스를 분석합니다
show_sidebar: false
---

## 📰 보안 뉴스 & 트렌드

보안 업계의 최신 동향과 중요한 뉴스를 정리하고 분석합니다.

{% assign news_posts = site.posts | where: "categories", "news" %}
{% for post in news_posts %}
### [{{ post.title }}]({{ post.url }})
**{{ post.date | date: "%Y년 %m월 %d일" }}**  
{{ post.excerpt | strip_html | truncate: 200 }}

---
{% endfor %}