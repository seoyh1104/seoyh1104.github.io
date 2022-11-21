---
title: "Code Review"
layout: archive
permalink: categories/Code-Review
author_profile: false
sidebar_main: true
sidebar :
    nav : "docs"
---

{% assign posts = site.categories['Code Review'] %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}