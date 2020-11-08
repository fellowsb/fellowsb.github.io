---
layout: page
title: Communication Systems
permalink: /comms/
order: 1
---

Flagstaff Solutions is located in California's Inland Empire providing communication system engineering and analysis. Example services include:

- Communication system architecture review
- Independent cost estimate analysis
- Communication site troubleshooting
- Interference investigation

We provide solutions and insight into the challenging world of communication systems.

{% for my_page in site.pages %}
{% if my_page.title == "Contact" %}
[Contact us!]({{ my_page.url | prepend: site.baseurl }})
{% endif %}
{% endfor %}
