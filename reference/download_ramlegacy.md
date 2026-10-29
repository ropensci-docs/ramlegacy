# Download RAM Legacy Excel Database

Downloads a specified version of RAM Legacy Stock Assessment Excel
Database and as an RDS object to a local directory specified by
[`ram_dir`](https://docs.ropensci.org/ramlegacy/reference/ram_dir.md).
The function will check if the version requested already exists on the
user's computer and if it does then it prompts the user to download it
again unless \`overwrite = TRUE\` in which case the function will
download the version without displaying the prompt. The function also
supports downloading all the older versions (1.0, 2.0, 2.5, 3.0, 4.3)
from \[a github repo\](www.github.com/kshtzgupta1/ramlegacy-assets)

## Usage

``` r
download_ramlegacy(version = NULL, ram_path = NULL,
  ram_url = "https://doi.org/10.5281/zenodo.2542918",
  overwrite = FALSE, quiet = FALSE)
```

## Arguments

- version:

  A character vector of length 1 specifying the version number of the
  database that should be downloaded. As of writing this package, the
  available versions are "1.0","2.0", "2.5", "3.0", "4.3", "4.40",
  "4.41", and "4.44". If the version argument is not specified then it
  defaults to latest version (currently latest version is "4.44").

- ram_path:

  A string specifying the path of the local directory where database
  will be downloaded. By default this path is set to the location
  provided by rappdirs package and can be viewed by calling
  [`ram_dir`](https://docs.ropensci.org/ramlegacy/reference/ram_dir.md).
  Although this is not the **recommended** approach `download_ramlegacy`
  supports downloading to a user-specified path.

- ram_url:

  A string. By default it is set to the Zenodo url of the database.
  Please **do not pass** in any other url to `ram_url`.

- overwrite:

  This argument is only relevant if you are trying to re-download a
  version that is already present locally in the rappdirs directory. If
  overwrite = TRUE then user will not encounter the interactive prompt
  that confirms whether to overwrite the version present locally.

- quiet:

  If TRUE, suppress status messages

## See also

Other ramlegacy functions:
[`load_ramlegacy`](https://docs.ropensci.org/ramlegacy/reference/load_ramlegacy.md),
[`ram_dir`](https://docs.ropensci.org/ramlegacy/reference/ram_dir.md)

## Examples

``` r
# \donttest{
# download version 4.44
download_ramlegacy(version = "4.44")
#> ★ Downloading...this may take a while
#> ★ Finished Downloading. Now unzipping it...
#> ★ Saving the unzipped database as RDS object...
#> ✔ Version 4.44 successfully downloaded.

# download version 1.0
download_ramlegacy(version = "1.0")
#> ★ Downloading...this may take a while
#> ★ Finished downloading v1.0. Saving the database as RDS object...
#> ✔ Version 1.0 successfully downloaded.
# If version not specified then default
# to latest version (currently 4.44)
download_ramlegacy()
#> ★ Downloading...this may take a while
#> ★ Finished Downloading. Now unzipping it...
#> ★ Saving the unzipped database as RDS object...
#> ✔ Version 4.44 successfully downloaded.
# }
```
