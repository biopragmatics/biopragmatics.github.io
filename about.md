---
layout: home
permalink: /about
---

## History

The Biopragmatics Stack was created by [Charles Tapley Hoyt](https://cthoyt.com)
in 2019 while at Fraunhofer SCAI. Its first component was
[PyOBO](https://github.com/biopragmatics/pyobo), which initially supported the
generation of
[Biological Expression Language (BEL)](https://biological-expression-language.github.io)
namespace files. The [Bioregistry](https://github.com/biopragmatics/bioregistry)
was initially developed as a component of PyOBO and was spun out into its own
repository in 2020.

Since, the Biopragmatics Stack has added several additional components that
support a wider and more generic set of data standardization and integration
problems in the life and natural sciences.

## Contact

<img src="https://gravatar.com/avatar/c273141237471c14342e9f9eb77044a0?size=256" alt="Charles Tapley Hoyt" align="left" style="margin-right: 10px; border-radius: 50%; height: 6em"/>
<strong>Dr. Charles Tapley Hoyt</strong><br />
<a href="mailto:cthoyt+biopragmatics@gmail.com">cthoyt@gmail.com</a><br />
<a href="https://orcid.org/0000-0003-4423-4370">
  <img alt="ORCID logo" src="/img/orcid-icon.svg" width="16" height="16" /> 0000-0003-4423-4370</a><br />
<a href="https://github.com/cthoyt">
  <img alt="GitHub logo" src="/img/github-icon.svg" width="16" height="16" /> @cthoyt</a>

## Acknowledgements

The Biopragmatics Stack is developed in part by the
[Gyori Lab for Computational Biomedicine](https://gyorilab.github.io) at
[Northeastern University](https://northeastern.edu) (previously a part of the
[Laboratory of Systems Pharmacology](https://hits.harvard.edu/the-program/laboratory-of-systems-pharmacology)
and the
[Harvard Program in Therapeutic Science (HiTS)](https://hits.harvard.edu) at
[Harvard Medical School](https://hms.harvard.edu)).

## Funding

The Biopragmatics Stack has been historically funded by the following awards:

<table>
<thead>
  <tr>
    <th>Funding Body</th>
    <th>Name</th>
    <th>Grant #</th>
  </tr>
</thead>
<tbody>
  {% for entry in site.data.funding %}
  <tr>
    <td>{{ entry.funder }}</td>
    <td>{{ entry.name }}{% if entry contains "pi" %} (PI: {{ entry.pi }}){% endif %}</td>
    <td><a href="{{ entry.link }}">{{ entry.id }}</a></td>
  </tr>
  {% endfor %}
</tbody>
</table>
