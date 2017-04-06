---
layout: page
permalink: /tag_cloud/
title: Tag Cloud
---
# Tag Cloud 

<div>
  {% assign sorted-tags = site.tags | sort %}
  <div class="tags-full-list">
    {% for tag in sorted-tags %}
		<a href="/menu/taglist#{{ tag[0] | slugify }}" class="simple-tag" style="font-size: {{ tag | last | size  |  times: 6 | plus: 100  }}%">
			<i class="fa fa-tag" aria-hidden="true">
				{{ tag[0] | replace:'-', ' ' }} ({{ tag | last | size }})
			</i>
		</a>
    {% endfor %}
  </div>
</div>

