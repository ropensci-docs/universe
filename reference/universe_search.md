# Search within a single universe

Search within a single universe

## Usage

``` r
universe_search(universe, query, limit = 100L)
```

## Arguments

- universe:

  Name of the universe (character of length 1)

- query:

  Query string. See [R-universe
  docs](https://docs.r-universe.dev/browse/search.html).

- limit:

  Number of results to return (integer of length 1)

## Value

A list with query results. The `total` field indicates the total number
of results and can be used as `limit` value in a second call.

## See also

Other universe:
[`universe_all_packages()`](https://docs.ropensci.org/universe/reference/universe_all_packages.md),
[`universe_ls()`](https://docs.ropensci.org/universe/reference/universe_ls.md),
[`universe_one_package()`](https://docs.ropensci.org/universe/reference/universe_one_package.md)

## Examples

``` r
if (FALSE) { # interactive()
universe_search("ropensci", query = '"weather data"')
universe_search("ropensci", query = 'needs:httr2')
}
```
