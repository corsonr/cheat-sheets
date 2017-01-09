# Using SCSS

- Website: http://sass-lang.com/
- Docs: http://sass-lang.com/guide

## Global Setup

Install on OS X: `sudo gem install sass`

## CLI Usage

| Action | Command |
| --- | --- |
| Version info | `sass -v` |
| Compile | `sass styles.scss styles.css` |
| Auto-Compile for single files | `sass --watch styles.scss:styles.css` |
| Auto-Compile for folders | `sass --watch .` |
| Auto-Compile for folders without sourcemap | `sass --sourcemap=none --style compressed --watch [from_folder]:[to_folder]` |

## Variables
Reusable color definition

```scss
$color: black;

p {
  color: $color;
}
```

## Mixins
Reusable blocks of definitions. Use `@include` to apply mixins to elements.

```
@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
          border-radius: $radius;
}

.box { @include border-radius(10px); }
```

## Import
Load code from external files. Convention naming: start partials filenames by an underscore.

```
@import 'reset'; // will import content from _reset.scss
```

## Color Functions

### Create Color Dynamically
| SCSS Code | Description |
| --- | --- |
| `rgb(100, 120, 140)` | Creates color from given values |
| `rgba(100, 120, 140, .5)` | Creates color from given values |
| `rgba($color, .5)` | Creates color from given values with given alpha |

### Modify HSLA Colors
| SCSS Code | Description |
| --- | --- |
| `darken($color, 5%)` | Darkens color by given % |
| `lighten($color, 5%)` | Lightens color by given % |
| `grayscale($color)` | Greyscales color |
| `saturate($color, 5%)` | Saturates color by given % |
| `desaturate($color, 5%)` | Desaturates color by given % |
| `invert($color)` | Inverts color |
| `fade-in($color, .5)` | Sets opacity to given % |
| `fade-out($color, .5)` | Halves opacity to given % |

## Numbers & Maths
| SCSS Code | Description |
| --- | --- |
| `floor(3.5)` | Round fractions down |
| `ceil(3.5)` | Round fractions up |
| `round(3.5)` | Rounds a float |
| `abs(3.5)` | Absolute value |
| `min(1, 2, 3)` | Find lowest value |
| `max(1, 2, 3)` | Find highest value |
| `percentage(.5)` | Gets corresponding percantge (50%) |
| `random(30)` |Returns random value between 1 and given value  |

## Comments
| SCSS Code | Description |
| --- | --- |
| `// SCSS comments` | not visible in CSS |
| `/* CSS comments */` | visible in CSS |
