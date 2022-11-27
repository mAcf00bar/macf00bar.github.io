---
layout: page
title: Bookmarks
description: Resources, tools, which are useful
---

Various online tools I found or stole from others ;-)

{% for category in site.data.bookmarks %}
{% assign items = category[1] | sort_natural: "name" %}
### {{ category[0] | capitalize }}:
{% for item in items %}
* [{{ item.name }}]({{ item.link }}){:target="_blank"}
  * {{ item.description }}
{% endfor %}
{% endfor %}
