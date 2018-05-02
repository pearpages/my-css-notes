# Transition

```css
a {
  color: green;
  transition: 1s;
}
a:hover {
  color: orange;
}
```

```css
code {
  color: black;
  font-size: 85%;
  background-color: rgba(255, 255, 255, 0.9);
  transition: all 2s ease-in 50ms;
}

code:hover {
  color: red;
  font-size: 120%;
  background-color: rgba(255, 255, 255, 0.8);
}

/*
 * Equivalent to:
 * 
code {
  transition:
    color, font-size, background-color 2s ease-in 50ms;
}
*/
```

```css
code {
  color: black;
  font-size: 85%;
  background-color: rgba(255, 255, 255, 0.9);
  transition: all 2s ease-in 50ms;
}

code:hover {
  color: red;
  transform: scale(1.4);
  transform-origin: 0 0;
  background-color: rgba(255, 255, 255, 0.8);
}

/*
 * Equivalent to:
 * 
code {
  transition:
    transform 2s ease-in 50ms;
}
*/
```

## Properties

* transition
  * transition-property
  * transition-duration
  * transition-timing-function
  * transition-delay

## Animatable Properties

Anything that has intermediate values:

e.g.: Opacity YES, display NO

## Transition Features or Limitations

* Where you write your transition (order in the stylesheet) matters
* Single iteration
* No granular control
* Limited methods of initiation
* Can't force them to finish

## Events & Transition Examples

* Event thrown only when transition completes
* *transitionend* for EVERY property
* *transitionend* for each long-hand property within a shorthand

### transitionend

It launche an specific transitionend event for each property that changes.

// TODO: WIP