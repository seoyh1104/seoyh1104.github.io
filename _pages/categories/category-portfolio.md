---
title: "Portfolio"
layout: archive
permalink: categories/portfolio
author_profile: true
sidebar_main: true
---

{% assign posts = site.categories.Portfolio %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}