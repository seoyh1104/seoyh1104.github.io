---
title: "Jenkins"
layout: archive
permalink: categories/Jenkins
author_profile: false
sidebar_main: true
sidebar :
    nav : "docs"
---

{% assign posts = site.categories.Jenkins %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}