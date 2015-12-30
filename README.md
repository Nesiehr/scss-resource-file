# scss-resource-file

Config SCSS Partials for Web Projects

---

### Colors

The material color palette provides 10 variations for the following:

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
$color-blue-50, $colorBlue50: #E3F2FD;

$color-blue-100, $colorBlue100: #BBDEFB;

$color-blue-200, $colorBlue200: #90CAF9;

$color-blue-300, $colorBlue300: #64B5F6;

$color-blue-400, $colorBlue400: #42A5F5;

$color-blue-500, $colorBlue500: #2196F3;

$color-blue-600, $colorBlue600: #1E88E5;

$color-blue-700, $colorBlue700: #1976D2;

$color-blue-800, $colorBlue800: #1565C0;

$color-blue-900, $colorBlue900: #0D47A1;
```

So color variables can be used with either hyphens or camel casing:

```scss
$color-blue-50
```

or

```scss
- $colorBlue50
```

Using partials you can import only the colors you need or all of them.

```scss
@import 'config/color/material-color' // Imports all of the material colors
@import 'config/color/material-color-grey' // Imports only the grey material colors
```