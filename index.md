---
layout: page
title: 보안 기술 블로그
subtitle: 매일(?) 학습하고 기록하기
description: 보안 트렌드, 기술 학습, 번역 자료를 정리하는 블로그
hero_image: /assets/images/hero-bg.png
hero_height: is-medium
show_sidebar: false
---

## 환영합니다! 👋

이 블로그는 보안 기술과 트렌드를 학습하고 공유하는 공간입니다.

### 📚 카테고리 소개

**🔸 하루 한 줄** - 매일 학습한 보안 기술이나 개념을 간단히 정리  
**📰 뉴스** - 최신 보안 트렌드와 뉴스 분석  
**🌐 번역** - 해외 보안 자료와 기술 문서 번역

---

### 최근 포스트
{% for post in site.posts limit:3 %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}