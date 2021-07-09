# Hello SASS

## Setup in VS Code

- Step1: Install live scss compiler [link](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass#review-details)

- step2: Go to setting and search for sass and then edit the settings.json

```json
 "liveSassCompile.settings.formats": [
        {
            "format": "expanded",
            "extensionName": ".min.css",
            "savePath": "/dist/css"
        }
    ]
```

It will tells the editor to save compiled Css to '/dist/css' folder and our css file has extension of `.min.css`.

- In SCSS any valid CSS is right.

## Variables

- In Normal Css

```css
:root {
  --primary-color: #123def;
  --secondary-color: #456eff;
  --text-color: #789acb;
}
```

- In SCSS

```SCSS
$primary-color: #123def;
$secondary-color: #456eff;
$text-color: #789acb;
```

## Map In SASS

```SCSS
$font-weight: (
  "regular": 400,
  "medium": 500,
  "bold": 700,
  "extra-bold": 1000,
);
```

- to apply one of the font-weight

```SCSS
font-weight:map-get($font-weight, bold);
```

# Nesting

- if You want full path of classes then

```SCSS
.main{
&_para{
    font-size:30px;
}
}
```

- output css will be

```CSS
.main_para{
    font-size:30px;
}
```

- but we dont want that

```SCSS
.main{
#{&}_para{
    font-size:30px;
}
}
```

- Here the output css will be

```CSS
.main .main_para {
    font-size:30px;
}
```

- Select parent using &

```SCSS
.main{
#{&}_para{
    font-size:30px;
    /*if we want to add hover on paragraph with class .main_para*/
    &:hover{
        color:$sendary-color;
    }
}
}
```

## Partials

- Paritals make our SCSS file modular

- Partial are declared with `_`

- We can import Partial and use it as the code is inside main

## Functions

```SCSS
@function weight($weight-name) {
  @return map-get($font-weight, $weight-name);
}
```

## Mixins

```SCSS
/*changing theme using scss*/
@mixin theme($light-theme: true) {
  @if $light-theme {
    background-color: lighten($color: #abcdef, $amount: 100%);
    color: darken($color: #000000, $amount: 100%);
  }
}

```
