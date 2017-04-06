---
layout: page
permalink: /tag_cloud/
title: Tag Cloud
---

<h2>Tag Cloud</h2>
{% assign tags = site.tags | sort %}
{% for tag in tags %}
 <span class="site-tag">
    <a href="/tag/{{ tag | first | slugify }}/"
        style="font-size: {{ tag | last | size  |  times: 4 | plus: 80  }}%, .site-tag a {display: inline-block;margin-right: 12px;}">
            {{ tag[0] | replace:'-', ' ' }} ({{ tag | last | size }})
    </a>
</span>
{% endfor %}
