---
title: "기록"
layout: archive
permalink: categories/Record
author_profile: false
sidebar_main: true
sidebar :
    nav : "docs"
---

{% assign posts = site.categories.Record %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}