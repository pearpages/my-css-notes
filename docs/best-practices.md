# Sass Best Practices

* File Organization
* Import Strategies

---

## File Organization

One example could be:

```
base
  project
  utils
components
  button
  tabs
specifics
  popins
vendor
```

By type

* Globals
* Components
* Sections
* Utils
* main.scss

### Globals

site-wide like typography, colors, and grids

### Components

buttons, tables or input fields

### Sections

dedicated to specific pages or areas on a pages

### Utils

third-party utilities that can be updated dynamically with tools like *bower*.

### main.scss

The primary file that imports everything

---

## Import Strategies

The best place to start is with a globals sheet containing imports, variables and mixins together. Many developers prefer to separate variables and mixins but this comes down to semantics.

> When building an import structure just remember to follow the concepts of **DRY** coding (Don’t Repeat Yourself).