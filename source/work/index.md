---
layout: default
title: Selected Works
slug: work
---

<section class="post-list">
<!-- Jekylls collections cannot do sorting in the include statement, need to assign ahead of time  -->
{% assign works = site.works | sort: 'date' | reverse %}
  {% for work in works   %}
    {% include work-page.html %}
  {% endfor %}
</section>
