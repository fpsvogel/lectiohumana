---
layout: home
title: Home
---

# Book
- [*Sursum Corda: Latin Stories and Songs of the Reformers*]({{ site.bookurl }}) – An intermediate Latin reader with early Protestant texts. Still in the proof of concept stage.

# Writings
{% for post in site.posts %}
	{% unless post.external_url %}
		{% assign recentpost = post %}
	{% endunless %}
{% endfor %}
{% assign circeposts = site.posts | where:"external_site","CiRCE Institute" %}
* Latest at this blog: [{{ recentpost.title }}]({{ recentpost.url }})<small class="post-date">{{ site.recentpost.date| date: "%m/%y" }}</small>
* Mere Orthodoxy: [“The Latin and Reformed Imagination”](https://mereorthodoxy.com/latin-reformed-imagination/)<small class="post-date">01/19</small>
* On classical education at the CiRCE Institute{% for post in circeposts %}
    - [“{{ post.title }}”]({{ post.external_url }})<small class="post-date">{{ post.date| date: "%m/%y" }}</small>
	{% endfor %}

# Videos
* *Latin, a Peculiar History:* A series which I hope to complete someday, based on Jürgen Leonhardt’s [“Latin: Story of a World Language”](Latin: Story of a World Language).
    - [“Do you REALLY know Latin?”](https://www.youtube.com/watch?v=AT0U5BJ19aM&list=PLqvZZdoCdlTu63N-cVAPR7WfEbkB6EEoE)
    - [“Is Latin dead?”](https://www.youtube.com/watch?v=JdFAFfYdkoQ&list=PLqvZZdoCdlTu63N-cVAPR7WfEbkB6EEoE)