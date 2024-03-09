---
title: "{{title}}"
aliases:
  - "{{title}}"
  - "{{citekey}}"
year: "{{year}}"
tags: 
citekey: "{{citekey}}"
keywords: "{{keywords}}"
authors: "[{{authors}}{{contributors}}]"
type: paper
---
{{title}}

# Formatted bibliography

{{bibliography}}
{% if abstractNote %}

# Abstract

{{abstractNote}}
{% endif %}

# Tags
{% for t in tags %}{{t.tag}}{% if not loop.last %}, {% endif %}{% endfor %}

