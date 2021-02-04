---
layout: default
---

<div class="time">Feb 2,2021</div>
## [我常用的设计流程][2]
理想化下（没有外部因素压制）设计一个功能或者是产品的流程，这个流程通常也可以运用于独立完成一个项目或者设计测试题。


<div class="time">Feb 2,2021</div>
## [Markdown所有样式][1]
展示一下本站所有Markdown的基础样式。

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<!-- 文章链接 -->

[1]:	project
[2]:	process