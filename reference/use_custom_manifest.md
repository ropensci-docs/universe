# Create `packages.json` for existing universe

Create `packages.json` for existing universe

## Usage

``` r
use_custom_manifest(universe, path = "packages.json")
```

## Arguments

- universe:

  Name of the universe, e.g. "jeroen"

- path:

  Absolute path to which the JSON file could be saved.

## Value

The path to the JSON file it created.

## Examples

``` r
if (FALSE) { # rlang::is_interactive()
json_file <- withr::local_tempfile()
use_custom_manifest("jeroen", json_file)
file.edit(json_file)
}
```
