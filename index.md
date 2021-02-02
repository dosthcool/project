---
layout: home
---

<!-- 文章需要倒叙排列，都有唯一的ID。 -->



<div class="time">Feb 2,2021</div>
## [我常用的设计流程][2]
理想化下（没有外部因素压制）设计一个功能或者是产品的流程，这个流程通常也可以运用于独立完成一个项目或者设计测试题。


<div class="time">Feb 2,2021</div>
## [Markdown所有样式][1]
展示一下本站所有Markdown的基础样式。



<!-- 文章链接 -->

[1]:	project
[2]:	process
[3]:	about



<!-- 图片链接 -->

[image-1]:	assets/pic/empty1.png
[image-2]:	assets/pic/empty1.png
[image-3]:	assets/pic/empty.png


---
layout: default
---
{%- include header.html -%}
<main class="post__archive">
  {%- include header_nav.html -%}
  {%- if paginator -%}
  {%- assign posts=paginator.posts -%}
  {%- else -%}
  {%- assign posts=site.posts -%}
  {%- endif -%}
  {%- for post in posts -%}
    <article class="post__entry">
      <a href="{{ post.url | relative_url }}" class="post__entry__link">
        <h2>{{ post.title }}</h2>
        <div class="post__meta">
          <time>{{ post.date | date: "%Y-%m-%d" }}</time>
        </div>
        <div class="post__excerpt">
          {{ post.excerpt | markdownify | strip_html | truncate: 100 }}
        </div>
        <div class="post__more_arrow"></div>
      </a>
    </article>
  {%- endfor -%}
  {%- include pagination.html -%}
</main>
{%- include footer.html -%}