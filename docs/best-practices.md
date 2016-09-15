# Sass Best Practices

* File Organization
* Import Strategies
* Naming Conventions
* Nesting and Looping
* Modularization

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

--- 

## Naming Conventions

> When naming anything in Sass it’s recommended to use all lowercase letters with dashes for separation.

- two (2) spaces indents, no tabs
- ideally, 80-characters wide lines or less
- meaningful use of whitespace
- use comments to explain CSS operations

When organizing your variables and mixins it’s recommended to split them up by category, then list them in alphabetical order. This makes editing a whole lot easier because you know exactly where to find something.

--- 

## Nesting and Looping

+ Never go more than 3 levels deep.
+ Ensure the CSS output is clean and reusable.
+ Use nesting when it makes sense, not as a default option.

Loops should not be used to duplicate selectors or properties for a selector; that’s what mixins are for.

```css
/* Sass code */
@for $i from 1 through 8 {
    $width: percentage(1 / $i)
 
    .col-#{$i} {
        width: $width;
    }
}
```

--- 

## Modularization

A CSS Module is a CSS file in which all class names and animation names are scoped locally by default. All URLs (url(...)) and @imports are in module request format (./xxx and ../xxx means relative, xxx and xxx/yyy means in modules folder, i. e. in node_modules).

When importing the CSS Module from a JS Module, it exports an object with all mappings from local names to global names.

```javascript
import styles from "./style.css";
// import { className } from "./style.css";

element.innerHTML = '<div class="' + styles.className + '">';
```