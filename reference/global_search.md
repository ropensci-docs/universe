# Search among all universes

Search among all universes

## Usage

``` r
global_search(query, limit = 100L)
```

## Arguments

- query:

  Query string. See [R-universe
  docs](https://docs.r-universe.dev/browse/search.html).

- limit:

  Number of results to return (integer of length 1)

## Value

A list with query results. The `total` field indicates the total number
of results and can be used as `limit` value in a second call.

## Examples

``` r
if (FALSE) { # interactive()
global_search(query = '"weather data"', limit = 1)
global_search(query = 'needs:httr2', limit = 1)
}
```
