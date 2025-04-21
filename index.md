---
layout: home  # ← 커스텀 홈 레이아웃 생성 권장
title: "메인"  
---

{% for page in site.pages %}
  {% if page.path contains '_pages/projects/' %}
    <div class="project-item">
      <h3>{{ page.title }}</h3>
      <p>{{ page.description }}</p>
      <a href="{{ page.url | relative_url }}">자세히 보기</a>
    </div>
  {% endif %}
{% endfor %}
