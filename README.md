
<!-- README.md is generated from README.Rmd. Please edit that file -->

# rogtemplate

<!-- badges: start -->

[![lifecycle](https://lifecycle.r-lib.org/articles/figures/lifecycle-experimental.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
<!-- badges: end -->

This package is a `pkgdown` template adapted to
[rOpenGov](http://ropengov.org/) site.

This is a private template for use by core rOpenGov packages. Please
don’t use it for your own code.

## Setup

Add a `_pkgdown.yml` file that contains at least these lines:

``` yaml
template:
  package: rogtemplate
```

Also, add a `.Rbuildignore` file on the root of your repo with these
lines:

    ^\.github$
    ^docs$
    ^_pkgdown\.yml$

## Using `rogtemplate`

It is possible to deploy your `pkgdown` site along with `rogtemplate`
via CI (GitHub Actions) or locally, that provides more control but it is
not automatic.

…
