---
layout: default
title: DMX Channel Mappings
---

[← Back to Inventory]({{ '/' | relative_url }})

{% for fixture in site.data.fixtures %}
{% if fixture.channels %}
## {{ fixture.name }} {#{{ fixture.name | slugify }}}

**Mode:** {{ fixture.mode }}

| Channel | Description | Value Range |
|---------|-------------|-------------|
{% for ch in fixture.channels %}| {{ ch.ch }} | {{ ch.desc }} | {{ ch.range }} |
{% endfor %}

{% endif %}
{% endfor %}