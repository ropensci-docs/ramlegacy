# Output OS-independent path to the rappdirs directory on user's computer where the RAM Legacy database is downloaded by default

Provides the download location for
[`download_ramlegacy`](https://docs.ropensci.org/ramlegacy/reference/download_ramlegacy.md)
in an OS independent manner. This is also the location from where
[`load_ramlegacy`](https://docs.ropensci.org/ramlegacy/reference/load_ramlegacy.md)
loads the database from.

## Usage

``` r
ram_dir(vers = NULL)
```

## Arguments

- vers:

  character, version number of the database. As of writing this package,
  the available versions are "1.0", "2.0", "2.5", "3.0", "4.3","4.40",
  "4.41", and "4.44". If version is not specified the `ram_dir()`
  returns the path to the rappdirs top-level directory which stores all
  the version subdirectories.

## See also

Other ramlegacy functions:
[`download_ramlegacy`](https://docs.ropensci.org/ramlegacy/reference/download_ramlegacy.md),
[`load_ramlegacy`](https://docs.ropensci.org/ramlegacy/reference/load_ramlegacy.md)

## Examples

``` r
# return the path to the rappdirs directory where
# all version subdirectories are stored
ram_dir()
#> [1] "/tmp/RtmpljIUxJ/file596968df66"

# Returns the path of the subdirectory where v4.3
# of the database is downloaded to and read from.
ram_dir(vers = "4.3")
#> [1] "/tmp/RtmpljIUxJ/file596968df66"
```
