---
layout: page
title: About
---

> Certis ingeniis immorari et innutriri oportet, si velis aliquid trahere quod in animo fideliter sedeat. Nusquam est qui ubique est. (*Epistulae Morales* 1.2)

> You must spend time with certain thinkers and feed on them only, if you want to draw out something that will stick in your mind. If you are everywhere, you are nowhere.

I skim online too much. So I cultivate deeper reading with the help of this blog, where I write thoughts on juicy excerpts.

### What does "lectio humana" mean?

Just a play on *lectio divina* with a nod to the humanists, whose writings I'm spending time with.

### Why all the Latin?

Because I love it. Also, it's good to seek wisdom in other worlds: in the case of Latin, the pre-industrial Graeco-Roman tradition.

### Why all the Christian stuff? I thought you said humanists.

I mean the humanists of the Renaissance, and their forebears and successors. If you think humanism is just another name for atheism, please read these:

* [Christian Humanism's Manifesto](https://www.tikkun.org/nextgen/christian-humanisms-manifesto-by-roger-e-olson) by Roger Olson
* [Christianity and the Humanist Tradition](http://www.theimaginativeconservative.org/2013/06/christianity-and-the-humanist-tradition.html) by Christopher Dawson
* [Why Christians should believe in humanism, and humanists in Christianity](https://www.theosthinktank.co.uk/cmsfiles/archive/files/Christian%20Humanism%20FINAL%20combined.pdf) by Theos

### Who are you?

{% if site.author.contact %}
{% assign len = site.author.contact | size %}
{% assign current_index = 0 %}
<div class="sidebar-personal-info-section">
<p> Contact me: 
{% for contact in site.author.contact %}
{% assign iconname = contact[0] %}
{% if contact[0] == 'email' %}
{% assign iconname = 'envelope' %}
{% endif %}
<a href="{{ contact[1] }}">
  <i class="fa fa-{{ iconname }}" aria-hidden="true"></i>
</a>
{% assign current_index = current_index | plus: 1 %}
{% if current_index != len %}|{% endif %}
{% endfor %}
</p>
</div>
{% endif %}