---
layout: page
title: Projects
permalink: /projects
---

# Projects

A collection of my projects.

<ul>
  {% assign project_notes = site.notes | where_exp: "note", "note.path contains 'projects'" | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in project_notes %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
