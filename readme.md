# Flexbox-grid-helper

Simple and useful mixins to make flex grids in Sass.
A DRY way to achieve a basic layout I usually need in many projects.

It aims to achieve the common minimum that I usually need for a grid of cards,
using flexbox.

It's supposed to be used with [autoprefixer](https://github.com/postcss/autoprefixer),
a [postcss](https://github.com/postcss/postcss) plugin.

## How to use

* import the scss (_flexbox-grid-helper.scss) file into your project
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

![example-1](https://www.dropbox.com/s/sj52l3szihm734n/example1.png)

*The size of the blocks and background-color are not added by the mixin*

#### Example 2

```css
ul {
  @include flex-grid(2, 5px);
}
```

![example-2](https://www.dropbox.com/s/uumhebm35jx52fd/example2.png)

*A grid with two columns and 5px of margin between blocks*

*More examples will be added soon*
