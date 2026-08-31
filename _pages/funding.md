---
layout: page
title: funding
permalink: /funding/
nav: true
---

The lab's research is funded by the following awards.

<ul>
{% for g in site.data.funding %}
  <li>
    <strong>{{ g.title }}</strong><br>
    {{ g.funder }}{% if g.scheme %}, {{ g.scheme }}{% endif %}{% if g.role %} ({{ g.role }}){% endif %}{% if g.amount_gbp %}, £{{ g.amount_gbp }}{% endif %}{% if g.start %}, {{ g.start }}{% if g.end %} to {{ g.end }}{% endif %}{% endif %}
  </li>
{% endfor %}
</ul>
