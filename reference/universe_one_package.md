# Info on a single packages in an universe

Info on a single packages in an universe

## Usage

``` r
universe_one_package(universe, package)
```

## Arguments

- universe:

  Name of the universe (character of length 1)

- package:

  Name of the package (character of length 1)

## Value

A list with information on the package.

## See also

Other universe:
[`universe_all_packages()`](https://docs.ropensci.org/universe/reference/universe_all_packages.md),
[`universe_ls()`](https://docs.ropensci.org/universe/reference/universe_ls.md),
[`universe_search()`](https://docs.ropensci.org/universe/reference/universe_search.md)

## Examples

``` r
if (FALSE) { # interactive()
universe_one_package("jeroen", package = "curl")
}
```
