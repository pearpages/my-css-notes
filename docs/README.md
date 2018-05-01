# Mediaqueries

> What we call *responsive* web desigin it's *squishy* web design. 
> **Estelle Weyl**

## Mediatype

* print
* screen
* ...

## Screen

* wrist watch
* smart phone
* tablet
* laptop
* monitor
* tv

## Placement

* In your css
* In the link tag

```html
<link rel="stylesheet"
  media="screen and (min-width: 320px) and (max-width: 480px)" href="css/stylesheet2.css" />
```

## Breakpoints

We should define breakpoints for the aspect ratio not for the devices.

With texts using ems should be enough and we wouldn't have the need to use mediaqueries. If we say that a paragraph has a width of 60em means that it will never get bigger than 60 characters.

## Properties

* min/max-width: viewport width
* min/max-height: viewport height
* orientation: portrait | landscape
* min/max-aspect-ratio: width/height
* min-max-resolution: 72dpi | 100dpcm

## Resolution Units

### Savari v Everyone Else

```css
-webkit-min-device-pixel-ratio: 2
min-resolution: 2dppx
min-resolution: 192dpi
```

## Query Syntax/Punctuation

* "only" leaves out older browsers 
```css
media="only print and (color)"
```
* "and" both parts must be true
* "not" if untrue
* Comma separates selectors - any part can be true
```css
media="print, screen and (min-width: 480px)"
```

## @supports

```css
@supports (display: flex) {
  /* rules for browsers supporting flex box */
}

@supports (display: table-cell) {
  /* ... */
}

@supports (display: grid) {
  /* ... */
}
```

## Viewport

> Viewport should be in all the stylesheets. All files should start with this metatag.

```css
@viewport {
  width: device-width;
}
```

## Use Cases

### Hyphenations

We want hyphenations in small screens but not in big screens.

```css
@media screen and (max-width: 38em) {
  p {
    hyphens: auto;
  }
}
```

### Columns

We don't really need mediaqueries for columns. Because you already define what's the width for each column. So it won't add columns if they don't fit the minimum width.

* column-count
* column-width
* column-rule
* column-gap

### SVG

It uses the size of the svg container.