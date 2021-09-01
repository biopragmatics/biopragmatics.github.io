---
layout: home
---
<p align="center">
  <img src="https://raw.githubusercontent.com/biopragmatics/biopragmatics.github.io/master/img/biopragmatics.png" height="150">
</p>

The Biopragmatics Stack is a collection of interlinked software packages that provide the
infrastructure for biomedical semantics and pragmatics.

{% for entry in site.data.software %}
<div style="padding-bottom: 10px;">
{% if entry contains "logo" %}
<img src="{{ entry.logo }}" alt="{{ entry.name }} Logo" style="float: left; max-height: 75px; max-width: 75px; margin-right: 15px" />
{% endif %}
<strong><a href="https://github.com/{{ entry.github }}">{{ entry.name }}</a></strong>
{% if entry contains "github" %}
      <a href="https://github.com/{{ entry.github }}">
      <img alt="GitHub logo" src="/img/github-icon.svg" width="16" height="16" />
      </a>
{% endif %}
{% if entry contains "wikidata" %}
    <a href="https://scholia.toolforge.org/topic/{{ entry.wikidata }}">
    <img alt="WikiData logo" src="/img/wikidata_logo.svg" height="16" />
    </a>
{% endif %}
<br />
{{ entry.description }}
<br />
{% if entry contains "url" %}
<a href="{{ entry.url }}">Website</a>&nbsp;&nbsp;
{% endif %}
{% if entry contains "api" %}
<a href="{{ entry.api }}">API</a>&nbsp;&nbsp;
{% endif %}
{% if entry contains "docs" %}
<a href="{{ entry.docs }}">Docs</a>&nbsp;&nbsp;
{% endif %}
</div>
{% endfor %}

## Acknowledgements

The Biopragmatics Stack is developed with ❤️ in 🇩🇪 and 🇺🇸 by
the [INDRA Lab](https://indralab.github.io) in the
[Laboratory of Systems Pharmacology](https://hits.harvard.edu/the-program/laboratory-of-systems-pharmacology)
and the [Harvard Program in Therapeutic Science (HiTS)](https://hits.harvard.edu) at
[Harvard Medical School](https://hms.harvard.edu).

It's funded by the DARPA Automating Scientific Knowledge Extraction (ASKE) program under award
HR00111990009 and the DARPA Young Faculty Award W911NF2010255 (PI: Benjamin M. Gyori).
