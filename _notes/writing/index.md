---
title: Writing
---

# Writing

A collection of my writing.

<ul>
  {% assign writing_notes = site.notes | where_exp: "note", "note.path contains 'writing'" | where_exp: "note", "note.title != 'Writing'" | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in writing_notes %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
