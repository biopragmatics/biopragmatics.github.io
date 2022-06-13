---
layout: home
---
<p align="center">
  <img src="https://raw.githubusercontent.com/biopragmatics/biopragmatics.github.io/master/img/biopragmatics.png" height="150">
</p>

The Biopragmatics Stack is a collection of interlinked software packages that provide the
infrastructure for biomedical semantics and pragmatics.

Our docker images can be found
on <i class="fab fa-docker"></i> [DockerHub](https://hub.docker.com/r/biopragmatics).

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
<a href="https://pypi.org/project/{{ entry.pypi }}"><i class="fas fa-dragon"></i> PyPI</a>&nbsp;&nbsp;
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

## Acknowledgements

The Biopragmatics Stack is developed with ❤️ by
the [INDRA Lab](https://indralab.github.io) in the
[Laboratory of Systems Pharmacology](https://hits.harvard.edu/the-program/laboratory-of-systems-pharmacology)
and the [Harvard Program in Therapeutic Science (HiTS)](https://hits.harvard.edu) at
[Harvard Medical School](https://hms.harvard.edu).

## Funding

The Biopragmatics Stack has been historically funded by the following awards:

<table>
  <tr>
    <td>Funding Body</td>
    <td>Name</td>
    <td>Grant #</td>
  </tr>
  {% for entry in site.data.funding %}
  <tr>
    <td>{{ entry.funder }}</td>
    <td>{{ entry.name }}{% if entry contains "pi" %}(PI: {{ entry.pi }}){% endif %}</td>
    <td>{{ entry.id }}</td>
  </tr>
  {% endfor %}
