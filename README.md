
<!-- README.md is generated from README.Rmd. Please edit that file -->

# xaringanthemer

Easily style your [xaringan](https://github.com/yihui/xaringan) slides
with **xaringanthemer**

## Installation

Currently, this is a work in progress. Try it yourself:

``` r
devtools::install_github("gadenbuie/xaringanthemer")
```

## Make it work

To make it work, add `css: xaringan-themed.css` to your xaringan slides
YAML header under `xaringan::moonreader:`

``` yaml
output:
  xaringan::moon_reader:
    lib_dir: libs
    css: xaringan-themed.css
```

Then, in the first knitr chunk, try this:

```` markdown
```{r setup}
options(htmltools.dir.version = FALSE)
library(xaringanthemer)
mono_light(
  base_color = "#1c5253",
  header_font_google = google_font("Josefin Sans"),
  text_font_google = google_font("Montserrat", "300", "300i"),
  code_font_google = google_font("Droid Mono")
)
```
````

![](docs/example_mono_light_1c5253.png)

## Monotone Themes

Use these functions to automatically create a consistent color palette
for your slides, based around a single color.

  - `mono_light()`: A light theme based around a single color

  - `mono_dark()`: A dark theme based around a single color

  - `mono_accent()`: The default xaringan theme with a single color used
    for color accents on select elements (headers, bold text, etc.)

  - `mono_accent_inverse()`: An “inverted” default xaringan theme with a
    single color used for color accents on select elements (headers,
    bold text, etc.)
