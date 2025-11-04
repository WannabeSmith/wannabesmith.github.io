---
layout: page
title: Papers
description: Publications, preprints, and theses
image: /assets/images/manuscript.jpeg
---


<div class='papers'>
  {% assign pubs = site.papers | sort: "date" | reverse | uniq %}
  
  <h1>Selected papers </h1>
  
  (A full list can be found on <a href="https://scholar.google.com/citations?user=FnyNlFAAAAAJ">google scholar</a>.)
  
  <table class='papers-table'>
  {% for pub in pubs %}
  <tr>
  <td>
   <div class="pubtitle">{{ pub.title }}</div> 
    <div class="pubauthors">{{ pub.authors }}.</div>
    <a href='{{ pub.arxiv }}'>arXiv</a>
    {% if pub.journal != nil %}
		&middot;
		{% if pub.journallink != nil %}
		<em><a href="{{pub.journallink}}">{{ pub.journal }}</a>, </em> 
		{% else %}
		<em>{{ pub.journal }}, </em> 
		{% endif %}
    {% endif %}
    {% if pub.year != nil %}
		 {{ pub.year }}
    {% endif %}
    {% if pub.highlight != nil %} <span id='highlight'>({{ pub.highlight }})</span> {% endif %}
    {% if pub.code != nil %} 
       <a href='{{ pub.code }}'>code</a>
    {% endif %}
  </td> 
  <!-- <td>
    <div class="pubinfo">
        {{ pub.year }}
        <small id='highlight'>{% if pub.highlight != nil %} <br> {{ pub.highlight }}{% endif %}</small>
    </div>
  </td> -->
  </tr>
  {% endfor %}
  </table> 
  
 <sup><span class="alphabetical">αβ</span></sup><em>Alphabetical ordering.</em>
  
<!-- {% capture markdown_content %}
# Software 

Aside from the code associated with the papers above, here are some packages that I maintain. 

<span style="color: black; font-weight: bold">testing-by-betting</span>: A python package which implements various methods for sequential, nonparametric hypothesis testing using various tools from game-theoretic probability and statistics. [[github]()] [[pypi]()]

<span style="color: black; font-weight: bold">xbounds</span>: A lightweight python package for Extreme Bounds Analysis. Computes both Leamer and Sala-i-Martin robustness criteria. Handles fixed-effects and multiprocessing. [[github]()] [[pypi]()]

{% endcapture %}
{{ markdown_content | markdownify }} -->




