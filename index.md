---
layout: default
---

{% for post in site.posts %}

{% assign d = post.date | date: "%-d"  %}{{ post.date | date: "%B" }} {% case d %}{% when '1' or '21' or '31' %}{{ d }}st{% when '2' or '22' %}{{ d }}nd{% when '3' or '23' %}{{ d }}rd{% else %}{{ d }}th{% endcase %}, {{ post.date | date: "%Y" }}
## [{{ post.title }}]({{ post.url }})

{{ post.content }}
* * *

{% endfor %}
