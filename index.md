---
layout: default
title: Whale OS Design Skills
---

{% capture readme %}{% include_relative README.md %}{% endcapture %}
{% comment %}Included Markdown expands after the relative-links plugin runs.{% endcomment %}
{{ readme | remove_first: '# Whale OS Design Skills' | replace: '](skills/README.md)', '](skills/)' }}
