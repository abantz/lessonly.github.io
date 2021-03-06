---
title: Styleguide
layout: page
---

# Lessonly Coding Style

## .editorconfig

The app contains an [`.editorconfig`](https://github.com/lessonly/lessonly/blob/master/.editorconfig) file which specifies most of the syntax conventions (spacing, etc.) we use. Be sure you're using [an Editorconfig plugin](http://editorconfig.org/#download) with your preferred text editor to ensure your code conforms to these conventions.

## General Guidelines

- **Don't ship commented-out code.** It can be a distraction from the actually functional code. If code is obsolete or non-functional, delete it: we'll always have a record of it in Git.

## Language-Specific Styles

<ul class="post-list">
  {% for page in site.pages %}
    {% assign dir_depth = page.path | split: '/' | size %}
    {% if page.path contains "styleguide/"
      and dir_depth == 2
      and page.path != "styleguide/index.md" %}
      <li>
        <h2>
          <a class="post-link" href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a>
        </h2>
      </li>
    {% endif %}
  {% endfor %}
</ul>




