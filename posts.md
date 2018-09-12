---
layout: default 
---

## Posts
{% for post in site.posts %}
### [{{post.title}}]({{post.url}})
<small><strong>{{ post.date | date "%B %e, %Y" }}</strong> . {{ post.category }} <a href="http://jeryanders.github.io/{{post.url}}"></a></small>
{{post.excerpt}}
{% endfor %}
