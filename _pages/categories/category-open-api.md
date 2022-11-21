---
title: "Open Api"
layout: archive
permalink: categories/Open-Api
author_profile: false
sidebar_main: true
sidebar :
    nav : "docs"
---

{% assign posts = site.categories['Open Api'] %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}