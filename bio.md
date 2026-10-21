---
layout: default
title: Bio
permalink: /bio/
---

## Biography

[One or two paragraphs summarizing your background, research arc, and current focus.]

### Positions

Entries come from `_data/positions.yml` — add, remove, or reorder items
there; no HTML needed.

{% include entry-list.html items=site.data.positions %}

### Education

Entries come from `_data/education.yml`.

{% include entry-list.html items=site.data.education %}
