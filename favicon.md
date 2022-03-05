# Favorite Icon (Favicon)

<!--
https://github.com/tailwindlabs/tailwindcss.com/tree/master/public/favicons
-->

## Tools

- [favicon.io](https://favicon.io/)
- [Favicon checker](https://realfavicongenerator.net/favicon_checker)

## Markup HTML

```html
<!-- Icon -->
<link rel="icon" type="image/x-icon"  href="/favicon.ico" />

<!-- PNG: https://caniuse.com/link-icon-png  -->
<link rel="icon" type="image/png" href="/favicon.png" />

<!-- Prefers Color Scheme -->
<link rel="shortcut icon" type="image/png" href="/favicon-dark.png" media="(prefers-color-scheme: dark)" />
<link rel="shortcut icon" type="image/png" href="/favicon-light.png" media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)" />
```

## Tips

### PNG to ICO

**Dependencies:** [ImageMagick](/imagemagick.md)

```sh
convert \
  -resize x32 \
  -gravity center \
  -crop 32x32+0+0 \
  ./favicon.png \
  -flatten \
  -colors 256 \
  -background transparent \
  ./favicon.ico

convert ./favicon.png \
  -background white \
  \( -clone 0 -resize 32x32 -extent 32x32 \) \
  -delete 0 \
  -alpha off \
  -colors 16 \
  ./favicon.ico
```
