# Use R-universe GitHub Actions workflow

Test the R-universe build workflow from your own GitHub repository

## Usage

``` r
use_universe_action(universe = NULL, path = ".")
```

## Arguments

- universe:

  Universe to set the context to, by default the owner of the
  repository. This affects where R package dependencies are downloaded
  from (besides the default repositories).

- path:

  Path to the local repository for which you want to use the workflow.

## Value

The path to the workflow

## Examples

``` r
if (FALSE) { # rlang::is_interactive()
temp_dir <- withr::local_tempdir()
workflow_path <- use_universe_action("maelle", temp_dir)
file.edit(workflow_path)
}
```
