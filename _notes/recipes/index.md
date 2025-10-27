---
title: Recipes
---

# Recipes

A collection of my recipes.

<ul>
  {% assign recipe_notes = site.notes | where_exp: "note", "note.path contains 'recipes'" | where_exp: "note", "note.title != 'Recipes'" | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recipe_notes %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
