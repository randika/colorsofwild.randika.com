---
layout: home
title: Wildlife by Randika Rathugamage
---

<!-- Gallery Section -->
<section id="thumbnails">{% for photo in site.photos %}
	<article>
		<a class="thumbnail" href="{{ site.images_base_url }}/{{ photo.image }}" data-position="left center">
			<img src="{{ site.images_base_url }}/{{ photo.image }}" alt="{{ photo.title }}" />
		</a>
		<div class="content">
			<h2>{{ photo.title }}</h2>
			<p>{{ photo.caption }}</p>
			<div class="meta">
				{% if photo.location %}
					<span class="location">📍 {{ photo.location }}</span>
				{% endif %}
				{% if photo.date %}
					<span class="date">📅 {{ photo.date | date: "%B %d, %Y" }}</span>
				{% endif %}
			</div>
		</div>
	</article>
{% endfor %}</section>
