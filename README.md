## WebSharks™ Icon Font (Sharkicons)

Font containing WebSharks logos/icons + many others; including FontAwesome! See: [**DEMO**](http://websharks.github.io/sharkicons/demo.html)

_Contains over 750 icons. Total file size: 212kb (compare to stand-alone FontAwesome @ 136kb)._

[![](https://img.shields.io/github/license/websharks/sharkicons.svg)](https://github.com/websharks/sharkicons/blob/HEAD/LICENSE.txt)
[![](https://img.shields.io/badge/made-w%2F_100%25_pure_awesome_sauce-AB815F.svg?label=made)](http://websharks-inc.com/)
[![](https://img.shields.io/badge/by-WebSharks_Inc.-656598.svg?label=by)](http://www.websharks-inc.com/team/)
[![](https://img.shields.io/github/release/websharks/sharkicons.svg?label=latest)](https://github.com/websharks/sharkicons/releases)
[![](https://img.shields.io/packagist/v/websharks/sharkicons.svg?label=packagist)](https://packagist.org/packages/websharks/sharkicons)
[![](https://img.shields.io/github/issues/websharks/sharkicons.svg?label=issues)](https://github.com/websharks/sharkicons/issues)
[![](https://img.shields.io/github/forks/websharks/sharkicons.svg?label=forks)](https://github.com/websharks/sharkicons/network)
[![](https://img.shields.io/github/stars/websharks/sharkicons.svg?label=stars)](https://github.com/websharks/sharkicons/stargazers)
[![](https://img.shields.io/github/downloads/websharks/sharkicons/latest/total.svg?label=downloads)](https://github.com/websharks/sharkicons/releases)
[![](https://img.shields.io/packagist/dt/websharks/sharkicons.svg?label=packagist)](https://packagist.org/packages/websharks/sharkicons)

---

![](assets/screenshot.png)

---

## Using Icons in HTML Markup

Include the Sharkicon CSS classes (long or short).

```html
<link rel="stylesheet" type="text/css" href="/path/to/sharkicons/src/long-classes.min.css" />
```

Construct an icon via HTML markup w/ this syntax.

```html
<i class="sharkicon sharkicon-websharks"></i>
```

i.e., `<i class="sharkicon sharkicon-[icon]"></i>`

### Short Classes (Less Markup; i.e., `.si-` vs. `.sharkicon-`)

```html
<link rel="stylesheet" type="text/css" href="/path/to/sharkicons/src/short-classes.min.css" />
```

```html
<i class="si si-websharks"></i>
```

---

## Importing/Including Icons via SCSS

```scss
@import '/path/to/sharkicons/src/sharkicons';
@include sharkicons-font('/path/to/sharkicons/src');
@include sharkicon-classes;
```

---

## Creating an Icon via SCSS

_Note: you can do this without including the `sharkicon-classes` if you like._

```scss
@import '/path/to/sharkicons/src/sharkicons';
@include sharkicons-font('/path/to/sharkicons/src');
// @include sharkicon-classes;

.my-class {
  @include sharkicon(websharks);
}
```

Equivalent to:

```css
.my-class::before {
  content:                    '\e004';
  font:                       normal normal normal 14px/1 sharkicons;
  text-rendering:             optimizeLegibility;
  -webkit-font-smoothing:     antialiased;
  font-smoothing:             antialiased;
  display:                    inline-block;
  font-size:                  inherit;
  text-decoration:            inherit;
  text-transform:             none;
}
```

Alternatively, you can pass a second argument to `sharkicon()` to set the before/after specification. The default value is `before`. You might want to change it to `after` in some special case.

```scss
@import '/path/to/sharkicons/src/sharkicons';
@include sharkicons-font('/path/to/sharkicons/src');
// @include sharkicon-classes;

.my-class {
  @include sharkicon(websharks, after);
}
```

Equivalent to:

```css
.my-class::after {
  content:                    '\e004';
  font:                       normal normal normal 14px/1 sharkicons;
  text-rendering:             optimizeLegibility;
  -webkit-font-smoothing:     antialiased;
  font-smoothing:             antialiased;
  display:                    inline-block;
  font-size:                  inherit;
  text-decoration:            inherit;
  text-transform:             none;
}
```
