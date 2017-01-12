
# Flexbox Layout

The Flexbox Layout (Flexible Box) module (currently a W3C Last Call Working Draft) aims at providing a more efficient way to lay out, align and distribute space among items in a container, even when their size is unknown and/or dynamic (thus the word "flex").

## Properties for the Parent (flex container)

### Display

Defines a flex container. It enables a flex context for all its direct children.

| Code  | Description |
| ------------- | ------------- |
| `display: flex;`  |  block  |
| `display: inline-flex;`  | inline  |

### flex-direction

Establishes the main-axis, thus defining the direction flex items are placed in the flex container.

| Code  | Description |
| ------------- | ------------- |
| `flex-direction: row;`  |  (default) left to right in `ltr`; right to left in `rtl`  |
| `flex-direction: row-reverse;`  | right to left in `ltr`; left to right in `rtl`  |
| `flex-direction: column;`  | same as `row` but top to bottom  |
| `flex-direction: column-reverse;`  | same as `row-reverse` but bottom to top  |

### flex-wrap

By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property. Direction also plays a role here, determining the direction new lines are stacked in.

| Code  | Description |
| ------------- | ------------- |
| `flex-wrap: nowrap;`  | (default) single-line / left to right in `ltr`; right to left in `rtl`  |
| `flex-wrap: wrap;`  | multi-line / left to right in `ltr`; right to left in `rtl`  |
| `flex-wrap: wrap-reverse;`  | multi-line / right to left in `ltr`; left to right in `rtl`  |

### flex-flow

Shorthand `flex-direction` and `flex-wrap` properties, which together define the flex container's main and cross axes. Default is `row nowrap`.

`flex-flow: <'flex-direction'> || <'flex-wrap'>`

### justify-content

Defines the alignment along the main axis.

| Code  | Description |
| ------------- | ------------- |
| `justify-content: flex-start;`  | (default) items are packed toward the start line  |
| `justify-content: center;`  | items are centered along the line |
| `justify-content: flex-end;`  | items are packed toward to end line |
| `justify-content: space-between;`  | items are evenly distributed in the line; first item is on the start line, last item on the end line  |
| `justify-content: space-around;`  | items are evenly distributed in the line with equal space around them  |

### align-items

Defines the default behaviour for how flex items are laid out along the cross axis on the current line

| Code  | Description |
| ------------- | ------------- |
| `align-items: flex-start;`  | cross-start margin edge of the items is placed on the cross-start line  |
| `align-items: center;`  | items are centered in the cross-axis  |
| `align-items: flex-end;`  | cross-end margin edge of the items is placed on the cross-end line  |
| `align-items: stretch;`  | (default) stretch to fill the container (still respect min-width/max-width)  |
| `align-items: baseline;`  | items are aligned such as their baselines align  |

### align-content

Aligns a flex container's lines within when there is extra space in the cross-axis.

| Code  | Description |
| ------------- | ------------- |
| `align-content: flex-start;`  | lines packed to the start of the container  |
| `align-content: center;`  | lines packed to the center of the container  |
| `align-content: flex-end;`  | lines packed to the end of the container  |
| `align-content: space-between;`  | lines evenly distributed; the first line is at the start of the container while the last one is at the end  |
| `align-content: space-around;`  | lines evenly distributed with equal space around each line  |
| `align-content: stretch;`  | (default) lines stretch to take up the remaining space  |

## Properties for the Children (flex items)

### order

### flex-grow

### flex-shrink

### flex-basis

### flex

### align-self
