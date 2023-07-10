---
permalink: /
layout: home
# title: Links
# list_title: useful links :)
---

Table of Contents
{% for category in site.data.links %}
* *[{{ category.name }}](#{{ category.name }})*   
{% endfor %}

***

{% for category in site.data.links %}

### {{ category.name }} <a name="{{ category.name }}">

| Name | Location | Description |
| --- | --- | --- |
{% for link in category.links %} | [{{link.name}}]({{link.url}}) | {{link.where}} | {{link.info}} |
{% endfor %}

{% endfor %}
