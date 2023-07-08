---
permalink: /
layout: home
# title: Links
# list_title: useful links :)
---

{% for category in site.data.links %}

### {{ category.name }}

| Name | Location | Description |
| --- | --- | --- |
{% for link in category.links %} | [{{link.name}}]({{link.url}}) | {{link.where}} | {{link.info}} |
{% endfor %}

{% endfor %}