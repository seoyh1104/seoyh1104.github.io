---
title: "Git"
layout: archive
permalink: categories/Git
author_profile: false
sidebar_main: true
sidebar :
    nav : "docs"
---

{% assign posts = site.categories.Git %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}