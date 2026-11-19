# Info on all packages in an universe

Info on all packages in an universe

## Usage

``` r
universe_all_packages(universe, limit = 100L)
```

## Arguments

- universe:

  Name of the universe (character of length 1)

- limit:

  Number of results to return (integer of length 1)

## Value

A list with information on all packages in the universe.

## See also

Other universe:
[`universe_ls()`](https://docs.ropensci.org/universe/reference/universe_ls.md),
[`universe_one_package()`](https://docs.ropensci.org/universe/reference/universe_one_package.md),
[`universe_search()`](https://docs.ropensci.org/universe/reference/universe_search.md)

## Examples

``` r
if (FALSE) { # interactive()
universe_all_packages("jeroen")
universe_all_packages("ropensci")
}
```
