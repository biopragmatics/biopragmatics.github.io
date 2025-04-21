---
layout: home
---

<img src="https://docs.google.com/drawings/d/e/2PACX-1vS3dvIX5EScSb9aIcjRmArJevZQEgKl2-mRbvcGwwmzAwyLUoBRltyKfTVYwsEMQOLMe3zHFxM3Ycfw/pub?w=2888&amp;h=1722">

The Biopragmatics Stack is a collection of interlinked software packages and
data resources that provide the infrastructure for biomedical semantics and
pragmatics.

Elements in dashed boxes are planned for future work or exist outside the
Biopragmatics stack.

## Software

{% for entry in site.data.software %}

<div style="padding-bottom: 20px;">
<img src="{% if entry contains "logo" %}{{ entry.logo }}{% else %}data:,{% endif %}" alt="{{ entry.name }} Logo" style="float: left; max-height: 85px; max-width: 85px; margin-right: 15px" />
<strong><a href="https://github.com/{{ entry.github }}">{{ entry.name }}</a>{% if entry contains "github" %}&nbsp;<img alt="GitHub logo" src="/img/github-icon.svg" width="16" height="16" />{% endif %}</strong>
{% if entry contains "wikidata" %}
    <a href="https://scholia.toolforge.org/topic/{{ entry.wikidata }}">
    <img alt="WikiData logo" src="/img/wikidata_logo.svg" height="16" />
    </a>
{% endif %}
<br />
{{ entry.description }}
<br />
<a href="https://github.com/{{ entry.github }}"><i class="fas fa-code"></i> Code</a>&nbsp;&nbsp;
{% if entry contains "pypi" %}
<a href="https://pypi.org/project/{{ entry.pypi }}"><i class="fas fa-dragon"></i> PyPI</a>&nbsp;&nbsp;
{% endif %}
{% if entry contains "url" %}
<a href="{{ entry.url }}"><i class="fas fa-network-wired"></i> Website</a>&nbsp;&nbsp;
{% endif %}
{% if entry contains "api" %}
<a href="{{ entry.api }}"><i class="fas fa-plane"></i> API</a>&nbsp;&nbsp;
{% endif %}
{% if entry contains "docs" %}
<a href="{{ entry.docs }}"><i class="fas fa-book"></i> Docs</a>&nbsp;&nbsp;
{% endif %}
{% if entry contains "docker" %}
<a href="https://hub.docker.com/r/{{ entry.docker }}"><i class="fab fa-docker"></i> Docker</a>&nbsp;&nbsp;
{% endif %}
</div>
{% endfor %}

### Links

- Our docker images can be found on <i class="fab fa-docker"></i>
  [DockerHub](https://hub.docker.com/r/biopragmatics)
- Our Python software can be found on [PyPI](https://pypi.org/org/biopragmatics)

## Data Resources

### Persistent URLs (PURLs)

The Biopragmatics Stack uses [https://w3id.org](https://w3id.org]) to create
persistent uniform resource locators (PURLs) for various resources. These are
configured on GitHub in the `.htaccess` file in
[https://github.com/perma-id/w3id.org](https://github.com/perma-id/w3id.org/tree/master/biopragmatics).
