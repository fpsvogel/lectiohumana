---
layout: home
title: Home
---

# Book
- [*Stories and Songs in Protestant Latin*]({{ site.bookurl }}) – An intermediate Latin reader and anthology of early Protestant texts. Still in the proof of concept stage.

# Writings
{% assign circeposts = site.posts | where:"external_site","CiRCE Institute" %}
{% assign davenantposts = site.posts | where:"external_site","The Davenant Institute" %}
<ul>
{% for post in site.posts %}
{% unless post.external_url %}
<li>Latest here: <a href="{{ post.url }}">{{ post.title }}: {{ post.subtitle }}</a><small class="post-date">{{ post.date| date: "%m/%y" }}</small></li>
{% break %}
{% endunless %}
{% endfor %}
<li>Mere Orthodoxy: <a href="https://mereorthodoxy.com/latin-reformed-imagination/">“The Latin and Reformed Imagination”</a><small class="post-date">01/19</small></li>
<li>On post-Reformation Latin at the Davenant Institute:
	<ul>
	{% for davenantpost in davenantposts %}
    <li><a href="{{ davenantpost.external_url }}">{{ davenantpost.title }}</a><small class="post-date">{{ davenantpost.date| date: "%m/%y" }}</small></li>
	{% endfor %}
	</ul>
</li>
<li>On classical education at the CiRCE Institute:
	<ul>
	{% for circepost in circeposts %}
    <li><a href="{{ circepost.external_url }}">{{ circepost.title }}</a><small class="post-date">{{ circepost.date| date: "%m/%y" }}</small></li>
	{% endfor %}
	</ul>
</li>
</ul>

# Videos
<ul>
<li><em>Latin, a Peculiar History:</em> A series which I hope to complete someday, based on Jürgen Leonhardt’s <a href="https://www.amazon.com/dp/0674659961"><em>Latin: Story of a World Language</em></a>.
    <ul>
	<li><a href="https://www.youtube.com/watch?v=AT0U5BJ19aM&list=PLqvZZdoCdlTu63N-cVAPR7WfEbkB6EEoE">“Do you REALLY know Latin?”</a></li>
    <li><a href="https://www.youtube.com/watch?v=JdFAFfYdkoQ&list=PLqvZZdoCdlTu63N-cVAPR7WfEbkB6EEoE">“Is Latin dead?”</a></li>
	</ul>
</li>
<ul>