# Flexbox-grid-helper

Simple and useful mixins to make flex grids in Sass.
A DRY way to achieve a basic layout I usually need in many projects.

It aims to achieve the common minimum that I usually need for a grid of cards,
using flexbox.

It's supposed to be used with [autoprefixer](https://github.com/postcss/autoprefixer),
a [postcss](https://github.com/postcss/postcss) plugin.

### How to install

You can clone this project, or use npm:

```
npm install flexbox-grid-helper
```

## How to use

* import the *_flexbox-grid-helper.scss* file, inside dist folder, into your project
* use the provided mixins in the flex container to generate the styles

### Examples

Given the below html:
```html
<ul>
  <li>
    <div class="inner"></div>
  </li>
  <li>
    <div class="inner"></div>
  </li>
  <li>
    <div class="inner"></div>
  </li>
  <li>
    <div class="inner"></div>
  </li>
  <li>
    <div class="inner"></div>
  </li>
  <li>
    <div class="inner"></div>
  </li>
  <li>
    <div class="inner"></div>
  </li>
  <li>
    <div class="inner"></div>
  </li>
</ul>
```

#### Example 1

```css
ul {
  @include flex-grid();
}
```

This will generate the layout with all the defaults, provided by the sass
variables.
Like so:

![example-1](https://raw.githubusercontent.com/vascocsilva/flexbox-grid-helper/master/images/example1.png)

*The size of the blocks and background-color are not added by the mixin.*

#### Example 2

```css
ul {
  @include flex-grid(2, 5px);
}
```

![example-2](https://raw.githubusercontent.com/vascocsilva/flexbox-grid-helper/master/images/example2.png)

*A grid with two columns and 5px of margin between blocks.*

#### Example 3

```css
@include flex-grid-cols(20px);
```

![example-3](https://raw.githubusercontent.com/vascocsilva/flexbox-grid-helper/master/images/example3.png)

*A grid with column direction and a 20px margin between blocks.*

#### Example 4

Making a responsive grid is also very easy.
Given the html above, you can put this code inside the flex container:

```css
@include flex-grid(6, 2px);

@media (max-width: 600px) {
  li {
    flex-basis: flex-calc-size(2);
  }
}
```

![example-4](https://raw.githubusercontent.com/vascocsilva/flexbox-grid-helper/master/images/example4.gif)

*A grid with 6 columns and 2px margin, that become 2 columns in <= 600px screen size.*

*More examples will be added soon*
