# Enable a package repository from r-universe

Adds r-universe package repositories to your `options("repos")` such
that they are used by default in
[`install.packages()`](https://rdrr.io/r/utils/install.packages.html).
If the universe was already enabled, it will not be added again, hence
it is harmless to call this function multiple times.

## Usage

``` r
add(universe = "ropensci")

remove(universe)
```

## Arguments

- universe:

  vector with name(s) of the universe(s), i.e. the subdomain part of
  `https://ropensci.r-universe.dev`.

## Value

the updated list of repositories

## Details

Note that changes to your options are not permanent. To automatically
enable a repository for every R session, you can call this function in
your [`~/.Rprofile`](https://rdrr.io/r/base/Startup.html) script.

## Examples

``` r
if (FALSE) { # interactive()
add("ropensci")
}
```
