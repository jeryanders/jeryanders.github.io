---
permalink: /
layout: index
---
## Latest Posts

{% for post in site.posts  %}
### [{{post.title}}]({{post.url}})
<small><strong>{{ post.date | date_to_long_string }}</strong> . {{ post.category }} <a href="http://jeryanders.github.io/{{post.url}}"></a></small>
{% endfor %}


