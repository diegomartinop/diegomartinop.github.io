---
layout: default
title: Publications
permalink: /publications/
---

{% assign pubs_by_year = site.data.publications | group_by: "year" %}
{% assign sorted_pubs = pubs_by_year | sort: "name" | reverse %}

{% for year_group in sorted_pubs %}
### {{ year_group.name }}

{% for pub in year_group.items %}
{{ pub.authors | join: ', ' }} 
({{ pub.year }})
**{{ pub.title}}**{% assign parts = '' %}{% if pub.conference %}{% assign parts = pub.conference %}{% endif %}{% if pub.journal %}{% if parts != '' %}{% assign parts = parts | append: '. ' %}{% endif %}{% assign parts = parts | append: pub.journal%}{% endif %}{% if pub.location %}{% if parts != '' %}{% assign parts = parts | append: '. ' %}{% endif %}{% assign parts = parts | append: pub.location %}{% endif %}{% if parts != '' %}. {{ parts }}{% endif %}.
{% if pub.link %}&nbsp;<i class="fas fa-link icon"></i> [Link]({{ pub.link }}){% endif %}{% if pub.pdf %}&nbsp;<i class="fas fa-file-pdf icon"></i> [PDF]({{ pub.pdf }}){% endif %}{% if pub.comment %}&nbsp;({{ pub.comment }}){% endif %}

{% endfor %}
{% endfor %}
