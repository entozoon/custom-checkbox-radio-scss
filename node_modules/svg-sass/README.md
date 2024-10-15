# SVG Sass

SVG inline encoding for your SCSS content or background-image attributes.

## Install

```bash
npm i svg-sass
```

## Include

```scss
// With a suitable path
@import "./node_modules/svg-sass";

// Or with webpack:
@import "~svg-sass";
```

## Usage

Encode your SVG XML into as CSS-friendly format, like so:

```scss
.foo {
  content: svg('<svg xmlns="http://www.w3.org/2000/svg" width="100%" viewBox="0 0 160 160">
    <circle cx="80" cy="80" r="80" fill="red" />
  </svg>'
);
```

Similarly, with a background image:

```scss
.foo {
  background-image: svg('<svg xmlns="http://www.w3.org/2000/svg" width="100%" viewBox="0 0 160 160">
    <circle cx="80" cy="80" r="80" fill="red" />
  </svg>'
);
```

Or if you prefer the mixin style:

```scss
.foo {
  @include svg('<svg xmlns="http://www.w3.org/2000/svg" width="100%" viewBox="0 0 160 160">
    <circle cx="80" cy="80" r="80" fill="red" />
  </svg>', background-image);
```

## Features

- Minifies SVG content
- Scraps newlines where possible

## Troubleshooting

Strange encoding issues? Try upgrading your node-sass version and encoding your files with LF EOLs.
