---
layout: home
title: Wildlife by Randika Rathugamage
---

<!-- Thumbnail -->
<section id="thumbnails">{% for photo in site.photos %}
	<article>
		<a class="thumbnail" href="{{ site.images_base_url }}/{{ photo.image }}" data-position="center center">
			<img src="{{ site.images_base_url }}/{{ photo.image }}" alt="{{ photo.caption }}" />
		</a>
		<div class="content">
			<h2>{{ photo.title }}</h2>
			<div class="meta">
				{% assign date_string = photo.title | slice: 0, 8 %}
				{% assign year = date_string | slice: 0, 4 %}
				{% assign month = date_string | slice: 4, 2 %}
				{% assign day = date_string | slice: 6, 2 %}
				<span class="date">{{ month }}/{{ day }}/{{ year }}</span>
				{% if photo.location %}
				<span class="location">{{ photo.location }}</span>
				{% endif %}
			</div>
			<p>{{ photo.caption }}</p>
		</div>
	</article>
{% endfor %}</section>
