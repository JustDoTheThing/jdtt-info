---
permalink: /
layout: home
# title: Links
# list_title: useful links :)
---
[Markdown Cheat Sheet](https://markdown.land/markdown-cheat-sheet)

{% for category in site.data.links %}

### {{ category.name }}

| Name | Location | Description |
| --- | --- | --- |
{% for link in category.links %} | [{{link.name}}]({{link.url}}) | {{link.where}} | {{link.info}} |
{% endfor %}

{% endfor %}