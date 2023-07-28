---
permalink: /
layout: home
# title: Links
# list_title: useful links :)
---

<div style = "display: flex; flex-flow: row wrap">
{% for category in site.data.links %}
<div style = "
    border: 1px solid #e8e8e8;
    padding: 10px 15px;
    margin: 2px;
    {% cycle '', 'background-color: #f7f7f7;' %}">
    <a href="#{{ category.name }}">{{ category.name }}</a>
</div>
{% endfor %}
</div>


{% for category in site.data.links %}

### {{ category.name }} <a name="{{ category.name }}">

| Name | Location | Description |
| --- | --- | --- |
{% for link in category.links %} | [{{link.name}}]({{link.url}}) | {{link.where}} | {{link.info}} |
{% endfor %}

{% endfor %}

