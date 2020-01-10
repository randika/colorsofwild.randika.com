---
layout: home
title: Wildlife by Randika Rathugamage
---

<!-- Thumbnail -->
<section id="thumbnails">{% for photo in site.photos %}
	<article>
		<a class="thumbnail" href="{{ site.images_base_url }}/{{ photo.image }}" data-position="left center"><img src="{{ site.images_base_url }}/{{ photo.image }}" alt="" /></a>
		<h2>{{ photo.title }}</h2>
		<p>{{ photo.caption }}</p>
	</article>
{% endfor %}</section>
