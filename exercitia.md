---
layout: default
title: Exercitia
---

<div class="posts">
  {% for post in paginator.posts %}
	{% if post.exercitia == 'exercitia' %}
	  <div class="post">
		<h1 class="post-title">
		  <a href="{{ site.baseurl }}{{ post.url }}">
			{{ post.subtitle }}
		  </a>
		</h1>
		<h2 class="post-subtitle">{{ post.title }}</h2>

		<span class="post-date">{{ post.date | date_to_string }}</span>
		{% if post.tags %} | 
		{% for tag in post.tags %}
		<a href="{{ site.baseurl }}{{ site.tag_page }}#{{ tag | slugify }}" class="post-tag">{{ tag }}</a>
		{% endfor %}
		{% endif %}

		<article>
		  {{ post.excerpt | markdownify }}
		<article>
		
		<div class="sidebar-personal-info-section">
		<p><h2 class="post-share">Share:&nbsp;
		<a href="https://www.facebook.com/sharer/sharer.php?u={{ site.url }}{{ post.url }}" style="text-decoration: none; font-size: 1.2rem">
		  <i class="fab fa-facebook" aria-hidden="true"></i>
		</a>&nbsp;|&nbsp;
		<a href="https://twitter.com/home?status=Lectio%20Humana—{{ post.author }}, {{ post.subtitle }}: {{ site.url }}{{ post.url }}" style="text-decoration: none; font-size: 1.2rem">
		  <i class="fab fa-twitter" aria-hidden="true"></i>
		</a>&nbsp;|&nbsp;
		<a href="http://www.reddit.com/submit?url={{ site.url }}{{ post.url }}&title=Lectio%20Humana—{{ post.author }}, {{ post.subtitle }}" style="text-decoration: none; font-size: 1.2rem">
		  <i class="fab fa-reddit" aria-hidden="true"></i>
		</a>
		</h2>
		</p>
		</div>
		
		<div class="post-more">
		  {% if site.disqus_short_name %}
		  <a href="{{ site.baseurl }}{{ post.url }}#disqus_thread"> <i class="fa fa-comments" aria-hidden="true"></i>Comment</a>&nbsp;
		  {% endif %}
		</div>
	  </div>
	{% endif %}
  {% endfor %}
</div>

<div class="pagination">
  {% if paginator.next_page %}
    <a class="pagination-item older" href="{{ site.baseurl }}/page{{paginator.next_page}}">Older</a>
  {% else %}
    <span class="pagination-item older">Older</span>
  {% endif %}
  {% if paginator.previous_page %}
    {% if paginator.page == 2 %}
      <a class="pagination-item newer" href="{{ site.baseurl }}/">Newer</a>
    {% else %}
      <a class="pagination-item newer" href="{{ site.baseurl }}/page{{paginator.previous_page}}">Newer</a>
    {% endif %}
  {% else %}
    <span class="pagination-item newer">Newer</span>
  {% endif %}
</div>