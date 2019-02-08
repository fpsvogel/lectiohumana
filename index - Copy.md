---
layout: home
title: Home
---

{% assign circetitles = "
“The Classical Polyglot: Everything You Need to Start Learning Latin and Greek”
|“What Is So Great about Latin?”
|“Renaissance Humanists: A Classical Education for Citizenship”
|“Was Greece Really That Special?”
|“Grounding Our Students in a Culture”
" | split: "|" %}

{% assign circeurls = "
https://www.circeinstitute.org/blog/classical-polyglot-everything-you-need-start-learning-latin-and-greek
|https://www.circeinstitute.org/blog/what-so-great-about-latin
|https://www.circeinstitute.org/blog/renaissance-humanists-classical-education-citizenship
|https://www.circeinstitute.org/blog/was-greece-really-special
|https://www.circeinstitute.org/blog/grounding-our-students-culture
" | split: "|" %}

{% assign circedates = "01/19|12/18|11/18|10/18|09/18" | split: "|" %}

{% assign peculiartitles = "
“Do you REALLY know Latin?”
|“Is Latin dead?”
" | split: "|" %}

{% assign peculiarurls = "
https://www.youtube.com/watch?v=AT0U5BJ19aM&list=PLqvZZdoCdlTu63N-cVAPR7WfEbkB6EEoE
|https://www.youtube.com/watch?v=JdFAFfYdkoQ&list=PLqvZZdoCdlTu63N-cVAPR7WfEbkB6EEoE
" | split: "|" %}

## Book
- [*Sursum Corda: Latin Stories and Songs of the Reformers*]({{ site.bookurl }})—An intermediate Latin reader with early Protestant texts. Still in the proof of concept stage.

## Writings
<ul class="tags-expo-posts">
    <a class="post-title" href="{{ site.posts[0].url }}">
    <li>
      Latest at this blog: {{ site.posts[0].title}}
    <small class="post-date">{{ site.posts[0].date| date: "%m/%y" }}</small>
    </li>
    </a>
	
	<a class="post-title" href="https://mereorthodoxy.com/latin-reformed-imagination/">
    <li>
      Mere Orthodoxy: “The Latin and Reformed Imagination”
    <small class="post-date">01/19</small>
    </li>
    </a>
</ul>
<ul>
    <li>On classical education at CiRCE</li>
	<div class="tags-expo-section">
    <ul class="tags-expo-posts">
      {% for i in (0..circetitles.size-1) %}
      <a class="post-title" href="circeurls">
      <li>
        {{ circetitles[i] }}
      <small class="post-date">{{ circedates[i] | date: "%m/%y" }}</small>
      </li>
      </a>
      {% endfor %}
    </ul>
	</div>
</ul>

## Videos
<ul>
    <li><em>Latin, a Peculiar History:</em> A series which I hope to complete someday, based on Jürgen Leonhardt’s [“Latin: Story of a World Language”](https://www.amazon.com/Latin-Story-Language-Jürgen-Leonhardt/dp/0674659961).</li>
	<div class="tags-expo-section">
    <ul class="tags-expo-posts">
      {% for i in (0..peculiartitles.size-1) %}
      <a class="post-title" href="peculiarurls[i]">
      <li>
        {{ peculiartitles[i] }}
      </li>
      </a>
      {% endfor %}
    </ul>
	</div>
</ul>