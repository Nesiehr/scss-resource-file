# SCSS Resource File

Config SCSS Partials for Web Projects

---

### Colors

---

The material color palette provides 10 variations for the following colors from the [google color palette](https://www.google.com/design/spec/style/color.html#color-color-palette):

- Amber
- Blue Grey
- Blue
- Brown
- Cyan
- Deep Orange
- Deep Purple
- Green
- Grey
- Indigo
- Light Blue
- Light Green
- Lime
- Orange
- Pink
- Purple
- Red
- Teal
- Yellow

Each of the above colors has its own partial containing predefined color variables in the following format:

```scss
$color-blue-50: #E3F2FD;
$color-blue-100: #BBDEFB;
$color-blue-200: #90CAF9;
$color-blue-300: #64B5F6;
$color-blue-400: #42A5F5;
$color-blue-500: #2196F3;
$color-blue-600: #1E88E5;
$color-blue-700: #1976D2;
$color-blue-800: #1565C0;
$color-blue-900: #0D47A1;

$colorBlue50: $color-blue-50;
$colorBlue100: $color-blue-100;
$colorBlue200: $color-blue-200;
$colorBlue300: $color-blue-300;
$colorBlue400: $color-blue-400;
$colorBlue500: $color-blue-500;
$colorBlue600: $color-blue-600;
$colorBlue700: $color-blue-700;
$colorBlue800: $color-blue-800;
$colorBlue900: $color-blue-900;
```

So color variables can be used with either hyphens or camel casing:

```scss
p {
	color: $color-blue-50;
}
```

or

```scss
p {
	color: $colorBlue50;
}
```

Using partials you can import only the colors you need or all of them.

```scss
@import 'config/color/material-color'; // Imports all of the material colors
@import 'config/color/material-color-grey'; // Imports only the grey material colors
```

---

###Mixins

---

Compatability mixins make it easier to ensure cross browser compatability by generating a style with -webkit, -moz, and -ms support.

Current compatability mixins:

- box-sizing
- align-items
- border-radius
- border-top-right-radius
- border-top-left-radius
- border-bottom-right-radius
- border-bottom-left-radius

Compatability mixins are simple to use:

```scss
div {
	@include box-sizing(border-box);
}
```

will generate

```css
div {
	-webkit-box-sizing: border-box;
	-moz-box-sizing: border-box;
	-ms-box-sizing: border-box;
	box-sizing: border-box;
}
```

Compatability mixins are, however, far from complete.

---

The breakpoint resource file lets you define styles by element for screen sizes mobile, tablet, desktop, and large desktop. For example this would auto-resize the width of this div for different window sizes.

```scss
div {
	@include breakpoint(mobile-only) {
        width: 100%;
    }
    @include breakpoint(tablet-range) {
    	width: 95%;
    }
    @include breakpoint(desktop-range) {
    	width: 90%;
    }
    @include breakpoint(large-desktop-range) {
    	width: 80%;
    }
}
```