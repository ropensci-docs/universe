# universe

> Tools for Working with [R-universe](https://r-universe.dev) and its
> APIs.

## Installation and docs

You can install the development version of universe from r-universe:

``` r

install.packages("universe", repos = "https://ropensci.r-universe.dev")
```

Or the development version of universe from
[GitHub](https://github.com/) with:

``` r

# install.packages("pak")
pak::pak("ropensci/universe")
```

Documentation is available on <https://docs.ropensci.org/universe>.

## Enable a repository

Use `runiverse::add()` to opt-in to a package repository (this will
modify your `options('repos')` list).

``` r

# Install a package from r-universe
universe::add("ropensci")
install.packages("magick")
```

For more details see the documentation for
[runiverse::add()](https://docs.ropensci.org/universe/reference/add.html).

## Get data from the APIs

### All packages in an universe

``` r

library(universe)
#> 
#> Attaching package: 'universe'
#> The following object is masked from 'package:base':
#> 
#>     remove
universe_ls("jeroen")
#>  [1] "RAppArmor" "V8"        "badgen"    "base64"    "bcrypt"    "brotli"   
#>  [7] "curl"      "js"        "jsonlite"  "maketools" "mongolite" "openssl"  
#> [13] "protolite" "rjade"     "sys"       "unix"      "webp"      "webutils"
```

### Info on all packages in an universe

``` r

universe_all_packages("jeroen", limit = 1) |>
  str(max.level = 2)
#> List of 1
#>  $ :List of 74
#>   ..$ Package                : chr "curl"
#>   ..$ Type                   : chr "Package"
#>   ..$ Title                  : chr "A Modern and Flexible Web Client for R"
#>   ..$ Version                : chr "8.2.0"
#>   ..$ Authors@R              : chr "c(\nperson(\"Jeroen\", \"Ooms\", role = c(\"aut\", \"cre\"), email = \"jeroenooms@gmail.com\",\ncomment = c(ORC"| __truncated__
#>   ..$ Description            : chr "Bindings to 'libcurl' <https://curl.se/libcurl/> for\nperforming fully configurable HTTP/FTP requests where res"| __truncated__
#>   ..$ License                : chr "MIT + file LICENSE"
#>   ..$ SystemRequirements     : chr "libcurl (>= 7.73): libcurl-devel (rpm) or\nlibcurl4-openssl-dev (deb)"
#>   ..$ URL                    : chr "https://jeroen.r-universe.dev/curl"
#>   ..$ BugReports             : chr "https://github.com/jeroen/curl/issues"
#>   ..$ VignetteBuilder        : chr "knitr"
#>   ..$ Encoding               : chr "UTF-8"
#>   ..$ Language               : chr "en-US"
#>   ..$ Roxygen                : chr "list(load = \"installed\", markdown = TRUE)"
#>   ..$ Config/roxygen2/version: chr "8.0.0"
#>   ..$ Config/pak/sysreqs     : chr "libssl-dev"
#>   ..$ Repository             : chr "https://jeroen.r-universe.dev"
#>   ..$ Date/Publication       : chr "2026-11-18 19:38:38 UTC"
#>   ..$ RemoteUrl              : chr "https://github.com/jeroen/curl"
#>   ..$ RemoteRef              : chr "HEAD"
#>   ..$ RemoteSha              : chr "548570f7d7ec84a362048e047354fe7b1a1ed00f"
#>   ..$ NeedsCompilation       : chr "yes"
#>   ..$ Packaged               :List of 2
#>   ..$ Author                 : chr "Jeroen Ooms [aut, cre] (ORCID: <https://orcid.org/0000-0002-4035-0289>),\nHadley Wickham [ctb],\nPosit Software, PBC [cph]"
#>   ..$ Maintainer             : chr "Jeroen Ooms <jeroenooms@gmail.com>"
#>   ..$ _user                  : chr "jeroen"
#>   ..$ _type                  : chr "src"
#>   ..$ _file                  : chr "curl_8.2.0.tar.gz"
#>   ..$ _fileid                : chr "https://r2.ropensci.org/c22fa87b938003f6b84d717531e36752d702f752edaaa43cb78c43871392cf7c"
#>   ..$ _filesize              : int 375634
#>   ..$ _sha256                : chr "c22fa87b938003f6b84d717531e36752d702f752edaaa43cb78c43871392cf7c"
#>   ..$ _expires               : chr "2027-02-26T21:31:24.000Z"
#>   ..$ _created               : chr "2026-11-18T21:19:20.000Z"
#>   ..$ _published             : chr "2026-11-18T21:31:26.913Z"
#>   ..$ _upstream              : chr "https://github.com/jeroen/curl"
#>   ..$ _status                : chr "success"
#>   ..$ _maintainer            :List of 8
#>   ..$ _jobs                  :List of 15
#>   ..$ _buildurl              : chr "https://github.com/r-universe/jeroen/actions/runs/44399719212"
#>   ..$ _commit                :List of 5
#>   ..$ _distro                : chr "resolute"
#>   ..$ _host                  : chr "GitHub-Actions"
#>   ..$ _registered            : logi TRUE
#>   ..$ _dependencies          :List of 9
#>   ..$ _owner                 : chr "jeroen"
#>   ..$ _selfowned             : logi TRUE
#>   ..$ _usedby                : int 6735
#>   ..$ _updates               :List of 12
#>   ..$ _tags                  : list()
#>   ..$ _stars                 : int 235
#>   ..$ _contributors          :List of 24
#>   ..$ _userbio               :List of 5
#>   ..$ _downloads             :List of 2
#>   ..$ _mentions              : int 21
#>   ..$ _devurl                : chr "https://github.com/jeroen/curl"
#>   ..$ _topics                :List of 1
#>   ..$ _rbuild                : chr "4.6.2"
#>   ..$ _assets                :List of 12
#>   ..$ _homeurl               : chr "https://github.com/jeroen/curl"
#>   ..$ _realowner             : chr "jeroen"
#>   ..$ _cranurl               : logi TRUE
#>   ..$ _releases              :List of 59
#>   ..$ _exports               :List of 149
#>   ..$ _help                  :List of 19
#>   ..$ _readme                : chr "https://github.com/jeroen/curl/raw/HEAD/README.md"
#>   ..$ _rundeps               : list()
#>   ..$ _sysdeps               :List of 1
#>   ..$ _vignettes             :List of 2
#>   ..$ _score                 : num 17.2
#>   ..$ _indexed               : logi TRUE
#>   ..$ _nocasepkg             : chr "curl"
#>   ..$ _universes             :List of 1
#>   ..$ _previous              : chr "8.1.0"
#>   ..$ _binaries              :List of 14
```

### Info on a single package in an universe

``` r

universe_one_package("jeroen", package = "curl") |>
  str(max.level = 1)
#> List of 75
#>  $ _id                    : chr "6afe192f5d9675f71838ac56"
#>  $ Package                : chr "curl"
#>  $ Type                   : chr "Package"
#>  $ Title                  : chr "A Modern and Flexible Web Client for R"
#>  $ Version                : chr "8.2.0"
#>  $ Authors@R              : chr "c(\nperson(\"Jeroen\", \"Ooms\", role = c(\"aut\", \"cre\"), email = \"jeroenooms@gmail.com\",\ncomment = c(ORC"| __truncated__
#>  $ Description            : chr "Bindings to 'libcurl' <https://curl.se/libcurl/> for\nperforming fully configurable HTTP/FTP requests where res"| __truncated__
#>  $ License                : chr "MIT + file LICENSE"
#>  $ SystemRequirements     : chr "libcurl (>= 7.73): libcurl-devel (rpm) or\nlibcurl4-openssl-dev (deb)"
#>  $ URL                    : chr "https://jeroen.r-universe.dev/curl"
#>  $ BugReports             : chr "https://github.com/jeroen/curl/issues"
#>  $ VignetteBuilder        : chr "knitr"
#>  $ Encoding               : chr "UTF-8"
#>  $ Language               : chr "en-US"
#>  $ Roxygen                : chr "list(load = \"installed\", markdown = TRUE)"
#>  $ Config/roxygen2/version: chr "8.0.0"
#>  $ Config/pak/sysreqs     : chr "libssl-dev"
#>  $ Repository             : chr "https://jeroen.r-universe.dev"
#>  $ Date/Publication       : chr "2026-11-18 19:38:38 UTC"
#>  $ RemoteUrl              : chr "https://github.com/jeroen/curl"
#>  $ RemoteRef              : chr "HEAD"
#>  $ RemoteSha              : chr "548570f7d7ec84a362048e047354fe7b1a1ed00f"
#>  $ NeedsCompilation       : chr "yes"
#>  $ Packaged               :List of 2
#>  $ Author                 : chr "Jeroen Ooms [aut, cre] (ORCID: <https://orcid.org/0000-0002-4035-0289>),\nHadley Wickham [ctb],\nPosit Software, PBC [cph]"
#>  $ Maintainer             : chr "Jeroen Ooms <jeroenooms@gmail.com>"
#>  $ _user                  : chr "jeroen"
#>  $ _type                  : chr "src"
#>  $ _file                  : chr "curl_8.2.0.tar.gz"
#>  $ _fileid                : chr "https://r2.ropensci.org/c22fa87b938003f6b84d717531e36752d702f752edaaa43cb78c43871392cf7c"
#>  $ _filesize              : int 375634
#>  $ _sha256                : chr "c22fa87b938003f6b84d717531e36752d702f752edaaa43cb78c43871392cf7c"
#>  $ _expires               : chr "2027-02-26T21:31:24.000Z"
#>  $ _created               : chr "2026-11-18T21:19:20.000Z"
#>  $ _published             : chr "2026-11-18T21:31:26.913Z"
#>  $ _upstream              : chr "https://github.com/jeroen/curl"
#>  $ _status                : chr "success"
#>  $ _maintainer            :List of 8
#>  $ _jobs                  :List of 15
#>  $ _buildurl              : chr "https://github.com/r-universe/jeroen/actions/runs/44399719212"
#>  $ _commit                :List of 5
#>  $ _distro                : chr "resolute"
#>  $ _host                  : chr "GitHub-Actions"
#>  $ _registered            : logi TRUE
#>  $ _dependencies          :List of 9
#>  $ _owner                 : chr "jeroen"
#>  $ _selfowned             : logi TRUE
#>  $ _usedby                : int 6735
#>  $ _updates               :List of 12
#>  $ _tags                  : list()
#>  $ _stars                 : int 235
#>  $ _contributors          :List of 24
#>  $ _userbio               :List of 5
#>  $ _downloads             :List of 2
#>  $ _mentions              : int 21
#>  $ _devurl                : chr "https://github.com/jeroen/curl"
#>  $ _topics                :List of 1
#>  $ _rbuild                : chr "4.6.2"
#>  $ _assets                :List of 12
#>  $ _homeurl               : chr "https://github.com/jeroen/curl"
#>  $ _realowner             : chr "jeroen"
#>  $ _cranurl               : logi TRUE
#>  $ _releases              :List of 59
#>  $ _exports               :List of 149
#>  $ _help                  :List of 19
#>  $ _readme                : chr "https://github.com/jeroen/curl/raw/HEAD/README.md"
#>  $ _rundeps               : list()
#>  $ _sysdeps               :List of 1
#>  $ _vignettes             :List of 2
#>  $ _score                 : num 17.2
#>  $ _indexed               : logi TRUE
#>  $ _nocasepkg             : chr "curl"
#>  $ _universes             :List of 1
#>  $ _previous              : chr "8.1.0"
#>  $ _binaries              :List of 14
```

### Search within a single universe

``` r

universe_search("ropensci", query = 'needs:httr2', limit = 1) |>
  str(max.level = 2)
#> List of 5
#>  $ results:List of 1
#>   ..$ :List of 14
#>  $ query  :List of 2
#>   ..$ _universes: chr "ropensci"
#>   ..$ _rundeps  : chr "httr2"
#>  $ skip   : int 0
#>  $ limit  : int 1
#>  $ total  : int 55
```

### Search among all universes

``` r

global_search(query = '"weather data"', limit = 1) |>
  str(max.level = 2)
#> List of 5
#>  $ results:List of 1
#>   ..$ :List of 14
#>  $ query  :List of 1
#>   ..$ $text:List of 2
#>  $ skip   : int 0
#>  $ limit  : int 1
#>  $ total  : int 100
```
