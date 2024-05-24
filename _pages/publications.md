---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<!-- {% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %} -->


## Journal Publications

<!-- {% assign sorted_journal_publications = site.publications.journals reversed %} -->

{% for publication in site.publications reversed %}
{% if publication.type == '3' %}
   [{{ publication.title }}]({{ publication.link }}){:target="_blank"}  
   {{ publication.authors }}  
   _{{ publication.journal }}_, {{ publication.year }}  
   conference version: _{{ publication.conference }}_ ({{ publication.acronym }}), {{publication.conferenceyear}}
{% endif %}
{% if publication.type == '2' %}
   [{{ publication.title }}]({{ publication.link }}){:target="_blank"}  
   {{ publication.authors }}  
   _{{ publication.journal }}_, {{ publication.year }}
{% endif %}
{% endfor %}


## Conference Publications
{% for publication in site.publications reversed %}
{% if publication.type == '1' %}
   [{{ publication.title }}]({{ publication.link }}){:target="_blank"}  
   {{ publication.authors }}  
   _{{ publication.conference }}_ ({{ publication.acronym }}), {{ publication.year }}
{% endif %}
{% endfor %}
