## What is a CSS Preprocessor?

We use preprocessors so we can get our CSS programmatically using variables, loops and functions.

Reasons why?

+ Speed
+ Organization
+ Modification
+ Minification
+ Error notification

Common Preporcessors

+ Sass
+ Less
+ Stylus

### Versions

+ .sass (Introduced in version 1)
+ .scss (Introduced in version 3)

```sass
// variables
$primary-color: hotpink;

.my-element {
    color: $primary-color;
    width: 100%;
}
```

### CSS Preprocessor Engine

+ Ruby
+ Javascript
+ PHP
+ Node js
+ Compass

#### Koala

> Koala is a GUI application for Less, Sass, Compass and CoffeeScript compilation, to help web developers to use them more efficiently. Koala can run in windows, linux and mac.

[http://koala-app.com/](http://koala-app.com/)

## Introduction

+ Partials an imports
+ Variables
+ Nesting
+ Mixins
+ Extend or Inheritance
+ Math Oeprations
+ Control Directives

### Partials an imports

The **_** underscore is used to identify a *partial*. When we see the *stylescss* file means the merge of them.

```bash
_variables.scss
_reset.scss
_phone-default.scss
_tablet.scss
_desktop.scss
_mobilemenu.scss
```

We render the files in the folder css/style.css.

```sass
@charset "UTF-8"

@import "reset";
@import "variables";
@import "phone-default";
@import "tablet";
@import "desktop";
@import "mobilemenu";
```

### Variables

Bad practice

```sass
$orange: #f15b2a;
```

Good practice

```sass
$primary-color: #f15b2a;
```


```sass
/* COLORS */
$red: #FF6666;
$blue: #0000FF;

$page-title-color: $red;
$link-color: $red;
$menu-background: $red;
$footer-background: $blue;

/* FONT WEIGHT */
$normal: 400;
$hearvy: 700;

/* GUTTER */
$gutter: 2%;
```

### Nesting

```sass
nav {
    ul {
        list-style: none;
    }
    li {
        float: left;
    }
    a {
        display: block;
        padding: .5em 1em;
        text-decoration: none;
    }
}
```

### Mixins

A mixin is like a function in a programming language.

```sass
@mixin its-name($variable1) {
    property: value;
    property: $variable1;
    property: value;
}
```

Example:

```sass
/* SCSS COLOR ASSIGNMENTS */
$brown: #86461e;
$orange: #ecbc4d;

@mixin button($color,$background) {
    border-radius: 20px;
    border: 1px solid #000;
    width: 10em;
    padding: .5em;
    box-shadow: 2px 2px 10px #999;
    text-align: center;
    color: $color;
    background-color: $background;
}
```

```sass
.button1 {
    @include button($brown, $orange);
}

.button2 {
    @include button($orange, $brown);
}
```

### Extend or Inheritance

### Math Oeprations

### Control Directives


## Setting up a project

## Example

### Header

### Main Rows and Columns

### Tabbed Navigation

### Style Lists

### Style columns

### Using loop
