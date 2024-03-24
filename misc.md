---
layout: page
title: Miscellaneous
---

# Posts


{% assign notesByYear = site.blogposts | where_exp: "item", "item.status == 'published'" | sort: "date" | reverse | group_by_exp:"item", "item.date | date: '%Y'"%}

{% for year in notesByYear %}
      {% for post in year.items %}
- {{ post.date | date: "%Y-%m-%d"}} - <a href="{{ post.url }}">{{ post.title }}</a>
      {% endfor %}
{% endfor %}


# Random links

Interesting things I want more people to see.

- The [Amstat youtube channel](https://www.youtube.com/@AmstatVideos).

	This is a criminally under-viewed treasure trove of interviews with famous statisticians. For example, [A conversation with Herbert Robbins](https://www.youtube.com/watch?v=IIO2urt8jHI) moderated by Frank Anscombe in 1990 is a wonderful watch.

- [An interview with Kai Lai Chung](https://www.youtube.com/watch?v=9WOHUxJctbM) and [an interview with Joseph L. Doob](https://www.youtube.com/watch?v=EiYsvdLtdS4), both conducted by Eugene Dynkin at Cornell.

<br/>

<center><em>Website template gratefully stolen from <a href="https://benchugg.com">Ben Chugg</a>.</em></center>
