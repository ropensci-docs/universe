# Download snapshot

Downloads a full copy (snapshot) of an R package repository.

## Usage

``` r
repo_snapshot(
  repo,
  destdir = NULL,
  types = c("src", "win", "mac", "linux", "wasm", "docs"),
  bin_versions = r_version(),
  verbose = interactive()
)

r_version()
```

## Arguments

- repo:

  url of the cran-like repository to snapshot

- destdir:

  path to directory where to save the snapshots

- types:

  which files to include. Must be subset of "src", "win", "mac",
  "linux", "wasm", "docs".

- bin_versions:

  vector with versions of R to download binary packages. Set to NULL to
  download all binaries available.

- verbose:

  print some progress

## Value

None, used for its side-effects.

## Examples

``` r
if (FALSE) { # interactive()
repo_snapshot("https://jeroen.r-universe.dev")
}
```
