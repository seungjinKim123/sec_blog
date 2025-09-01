---
layout: page
title: 번역 자료
subtitle: 해외 보안 기술 자료 번역
description: 유용한 해외 보안 기술 문서와 자료를 번역하여 공유합니다
show_sidebar: false
---

## 🌐 번역 자료

해외의 유용한 보안 기술 문서와 자료를 번역하여 공유합니다.

{% assign translation_posts = site.posts | where: "categories", "translation" %}
{% for post in translation_posts %}
### [{{ post.title }}]({{ post.url }})
**{{ post.date | date: "%Y년 %m월 %d일" }}**  
{% if post.original_url %}
**원문:** [{{ post.original_title }}]({{ post.original_url }})
{% endif %}
{{ post.excerpt | strip_html | truncate: 200 }}

---
{% endfor %}