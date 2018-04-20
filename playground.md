---
layout: default
---

# Variables

<https://jekyllrb.com/docs/variables/>

## site.static_files
{% for sf in site.static_files %}
  * `{{ sf.path }}` - {{ sf.modified_time }}
{% endfor %}

## site.pages
{% for sf in site.pages %}
  * `{{ sf.path }}`
{% endfor %}









page.path = `{{ page.path }}`

site.theme = `{{ site.theme }}`




# More Tests

* [A post]({{ site.baseurl }}{% post_url 2018-04-18-ca-plane-pour-toi %}) <!-- old way -->
* [same post]({{ site.baseurl }}{% link _posts/2018-04-18-ca-plane-pour-toi.md %})
