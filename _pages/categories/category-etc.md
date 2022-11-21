---
title: "ETC"
layout: archive
permalink: categories/ETC
author_profile: false
sidebar_main: true
sidebar :
    nav : "docs"
---

{% assign posts = site.categories.ETC %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}