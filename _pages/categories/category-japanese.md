---
title: "Japanese"
layout: archive
permalink: categories/Japanese
author_profile: false
sidebar_main: true
sidebar :
    nav : "docs"
---

{% assign posts = site.categories.Japanese %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}