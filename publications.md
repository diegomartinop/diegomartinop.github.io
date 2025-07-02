---
layout: default
title: Publications
permalink: /publications/
---

# Publications

{% assign pubs_by_year = site.data.publications | group_by: "year" %}
{% assign sorted_pubs = pubs_by_year | sort: "name" | reverse %}

{% for year_group in sorted_pubs %}
## {{ year_group.name }}

{% for pub in year_group.items %}
- {{ pub.authors | join: ', ' }} 
({{ pub.year }})
**{{ pub.title}}**{% assign parts = '' %}{% if pub.conference %}{% assign parts = pub.conference %}{% endif %}{% if pub.journal %}{% if parts != '' %}{% assign parts = parts | append: '. ' %}{% endif %}{% assign parts = parts | append: pub.journal%}{% endif %}{% if pub.location %}{% if parts != '' %}{% assign parts = parts | append: '. ' %}{% endif %}{% assign parts = parts | append: pub.location %}{% endif %}{% if parts != '' %}. {{ parts }}{% endif %}.
{% if pub.link %}&nbsp;<i class="fas fa-link icon"></i> [Link]({{ pub.link }}){% endif %}{% if pub.pdf %}&nbsp;<i class="fas fa-file-pdf icon"></i> [PDF]({{ pub.pdf }}){% endif %}{% if pub.comment %}&nbsp;({{ pub.comment }}){% endif %}

{% endfor %}
{% endfor %}

<div style="width: 100%; overflow: hidden;text-align: center; margin: 0 auto;">
     <a href="https://www.scimagojr.com/journalsearch.php?q=22489&amp;tip=sid&amp;exact=no" title="SCImago Journal &amp; Country Rank"><img border="0" src="https://www.scimagojr.com/journal_img.php?id=22489" alt="SCImago Journal &amp; Country Rank"  /></a>
     <a href="https://www.scimagojr.com/journalsearch.php?q=25674&amp;tip=sid&amp;exact=no" title="SCImago Journal &amp; Country Rank"><img border="0" src="https://www.scimagojr.com/journal_img.php?id=25674" alt="SCImago Journal &amp; Country Rank"  /></a>
</div>