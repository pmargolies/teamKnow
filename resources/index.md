---
title: Resources
permalink: /resources/
layout: resources

---
{% assign grouped_resources = site.resources | group_by: 'category' %}
# Resources
{% for category in grouped_resources %}
  ## {{category.name}}
    {% for item in category.items %}
      <p>{{item.title}}</p>
    {% endfor %}    
{% endfor %}
