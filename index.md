---
layout: home  # ← 커스텀 홈 레이아웃 생성 권장
title: "메인"  
---
<!-- 
{% for page in site.pages %}
  {% if page.path contains '_pages/projects/' %}
    <div class="project-item">
      <h3>{{ page.title }}</h3>
      <p>{{ page.description }}</p>
      <a href="{{ page.url | relative_url }}">자세히 보기</a>
    </div>
  {% endif %}
{% endfor %} -->

---
layout: home
title: "Welcome to My Blog"
---

<div class="intro">
  <h1>Welcome to My Personal Blog</h1>
  <p>Explore my projects, read my thoughts, and stay updated with my latest posts.</p>
</div>

<div class="latest-posts">
  <h2>Latest Posts</h2>
  {% for post in site.posts limit:5 %}
    <div class="post-item">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt }}</p>
    </div>
  {% endfor %}
</div>

<div class="projects">
  <h2>Featured Projects</h2>
  {% for page in site.pages %}
    {% if page.path contains '_pages/projects/' %}
      <div class="project-item">
        <h3>{{ page.title }}</h3>
        <p>{{ page.description }}</p>
        <a href="{{ page.url | relative_url }}">Read More</a>
      </div>
    {% endif %}
  {% endfor %}
</div>
