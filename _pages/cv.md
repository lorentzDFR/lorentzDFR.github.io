---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 2
description: Curriculum vitae.
---

{% assign cv_path = "/assets/pdf/CV_Lorenzo_Di_Fruscia_May_26.pdf" %}
{% assign cv_file = site.static_files | where: "path", cv_path %}

{% if cv_file.size > 0 %}
<div class="cv-embed" style="width: 100%; min-height: 120vh; margin-top: 0.5rem;">
  <iframe
    src="{{ cv_path | relative_url }}"
    title="Curriculum Vitae"
    style="width: 100%; height: 120vh; min-height: 1200px; border: 1px solid rgba(0, 0, 0, 0.12); border-radius: 6px;"
  ></iframe>
</div>
<p style="margin-top: 0.75rem;">
  If the embedded PDF does not load, use this
  <a href="{{ cv_path | relative_url }}" target="_blank" rel="noopener">direct link</a>. *Last updated 2026-05-01*
</p>
{% else %}
CV coming soon.
{% endif %}
