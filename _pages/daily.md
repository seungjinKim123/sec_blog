---
layout: page
title: 하루 한 줄
subtitle: 매일 학습한 보안 기술 정리
description: 하루에 하나씩 학습한 보안 개념과 기술을 기록합니다
show_sidebar: false
---

## 📖 하루 한 줄 학습 기록

매일 새로운 보안 기술이나 개념을 학습하고 간단히 정리합니다.

{% assign daily_posts = site.posts | where: "categories", "daily" %}
{% for post in daily_posts %}
### [{{ post.title }}]({{ post.url }})
**{{ post.date | date: "%Y년 %m월 %d일" }}**  
{{ post.excerpt | strip_html | truncate: 150 }}

---
{% endfor %}