---
title: "News"
layout: article
permalink: /allnews.html
---

{% for article in site.data.news.news %}
<p style="background-color: #f0f0f0;"><i><font color="gray">{{ article.date }}</font></i><br>
{{ article.headline }}</p>
{% endfor %}
