# Sass Best Practices

* Folder Structure

## Folder Structure

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

