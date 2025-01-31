
<!-- README.md is generated from README.Rmd. Please edit that file -->

# rogtemplate <a href='https://ropengov.github.io/rogtemplate/'><img src='man/figures/logo.png' align="right" height="139" /></a>

<!-- badges: start -->

[![rOG-badge](https://ropengov.github.io/rogtemplate//reference/figures/ropengov-badge.svg)](https://ropengov.org/)
[![R build
status](https://github.com/ropengov/rogtemplate/workflows/R-CMD-check/badge.svg)](https://github.com/rOpenGov/rogtemplate/actions)
[![r-universe](https://ropengov.r-universe.dev/badges/rogtemplate)](https://ropengov.r-universe.dev/)
[![lifecycle](https://lifecycle.r-lib.org/articles/figures/lifecycle-experimental.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
<!-- badges: end -->

This package is a **pkgdown** template adapted to
[rOpenGov](https://ropengov.org/) site.

This is a private template for use by core rOpenGov packages. Please
don’t use it for your own code.

## Using rogtemplate

It is possible to deploy your **pkgdown** site along with
**rogtemplate** via CI (GitHub Actions) or locally, that provides more
control but it is not automatic.

### Option A: Deploy using GitHub Actions

It is not necessary to install **rogtemplate** itself. First copy [this
file](https://github.com/rOpenGov/rogtemplate/blob/main/inst/yaml/rogtemplate-gh-pages.yaml)
into your `.github/workflows/` folder.

Next go to *YOUR_GITHUB_REPO>Settings>GitHub Pages* and create a branch named `gh-pages`.  
**rogtemplate** needs to be deployed from this branch.

### Option B: Deploy installing rogtemplate

You can install **rogtemplate** using the
[r-universe](https://ropengov.r-universe.dev/ui):

``` r
# Enable this universe
options(repos = c(
  ropengov = "https://ropengov.r-universe.dev",
  CRAN = "https://cloud.r-project.org"
))

# Install some packages
install.packages("rogtemplate")
```

You can use also the **remotes** package:

``` r
library(remotes)
install_github("ropengov/rogtemplate", dependencies = TRUE)
```

You can use `rog_actions_pkgdown_branch()` for setting up the action
described before but the deployment would be still performed by a GitHub
action.

For building locally your package into your `docs` folder use:

``` r
rogtemplate::rog_build()

# or you can use also

rogtemplate::rog_add_template_pkgdown()
pkgdown::build_site()
```

Note that `rogtemplate::rog_add_template_pkgdown()` creates a
`_pkgdown.yml` file (or modify an existing one) with the following
lines:

``` yaml
template:
  package: rogtemplate
```

These lines tells **pkgdown** to use **rogtemplate**.

## Commit to GitHub and deploy

Last step is commit to GitHub, wait until the GitHub action ends (in the
case you chose to deploy in that way) and deploy the website via
*YOUR_GITHUB_REPO>Settings>GitHub Pages*.

Please note: after you commit, it may take 24 hours or more until your website is updated. 

## Extras

We provide also some additional extra functions for creating badges and
logos, see
[Extras](https://ropengov.github.io/rogtemplate/reference/index.html)
for more info.
