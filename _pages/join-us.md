---
layout: page
title: join us
permalink: /join-us/
nav: true
---

We are recruiting. Formal advertisements are coming soon; details of the
funded positions below. Informal enquiries to
[jiabao.xu@glasgow.ac.uk](mailto:jiabao.xu@glasgow.ac.uk) are very welcome.

<ul>
{% for v in site.data.vacancies %}
  <li>
    <strong>Postdoctoral position: {{ v.title }}</strong><br>
    Funded by {{ v.funder }}{% if v.scheme %} ({{ v.scheme }}){% endif %}{% if v.opens %}, opening {{ v.opens }}{% endif %}
  </li>
{% endfor %}
</ul>
