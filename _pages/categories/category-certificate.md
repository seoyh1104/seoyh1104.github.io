---
title: "Certificate"
layout: archive
permalink: categories/Certificate
author_profile: false
sidebar_main: true
sidebar :
    nav : "docs"
---



{% assign posts = site.categories.Certificate %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}