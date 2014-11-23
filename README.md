Sass Specificity
================

**Sass (SCSS) Specificity Calculator**
Utility to calculate (and display) specificity or specificity map of any valid simple/compound/complex selector via mixin or function. If given a [selector list](http://dev.w3.org/csswg/selectors4/#selector-list), the highest specificity map/value will be displayed.

## Usage
```scss
@include 'path/to/_specificity';

// As a mixin
figure .out > select.or[specificty] {
  @include specificity; // specificity: 0, 3, 2;
                        // specificity-value: 770;
}

// As a function
a ~ head #of + time {
  $this-specificity-map: specificity(&); // (a: 1, b: 0, c: 3)
  $this-specificity-value: specificity(&, true); // 65539
}
```
