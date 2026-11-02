---
redirect_from:
  - /code.html
seo_title: "Open-Source Code and Datasets"
seo_description: "Open-source code and datasets from WCSNG at UC San Diego, including EdgeRIC, C-Shenron, GreenMO, and mmFlexible."
layout: page
permalink: code/
---
<h2>Code</h2>
<ul>
{% for article in site.posts %}
  {% if article.github %}
    <li> 
      <a href="{{ article.github }}">{{ article.title }}</a> 
      {% if article.osd %}
        <p>{{ article.osd }}</p>
      {% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>

<h2>Datasets</h2>
<ul>
{% for article in site.posts %}
  {% if article.dataset %}
    <li> 
      <a href="{{ article.dataset }}">{{ article.title }}</a> 
      {% if article.osd %}
        <p>{{ article.osd }}</p>
      {% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>
  

{% assign _sep = "" %}
{% assign _seen = "" %}
<script type="application/ld+json">
[{% for article in site.posts %}{% if article.dataset and article.osd %}{% unless _seen contains article.dataset %}{% assign _seen = _seen | append: article.dataset | append: " " %}{{ _sep }}{
  "@context": "https://schema.org",
  "@type": "Dataset",
  "name": {{ article.short_title | default: article.title | append: " dataset" | jsonify }},
  "description": {{ article.osd | strip_html | normalize_whitespace | jsonify }},
  "url": {{ article.url | absolute_url | jsonify }},
  "sameAs": {{ article.dataset | jsonify }},
  "creator": { "@type": "Organization", "name": "WCSNG, UC San Diego", "url": "https://wcsng.ucsd.edu/" }
}{% assign _sep = "," %}{% endunless %}{% endif %}{% endfor %}]
</script>
