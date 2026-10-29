# Read-in dataframes from downloaded RAM Legacy Database

Returns a list of specific dataframes or a list of all the dataframes
present in the requested version of the database.

## Usage

``` r
load_ramlegacy(version = NULL, tables = NULL, ram_path = NULL)
```

## Arguments

- version:

  A character vector of length 1 specifying the version number of the
  database. As of writing this package, the available versions are
  "1.0", "2.0", "2.5", "3.0", "4.3", "4.40", "4.41" and "4.44". If
  version argument is not specified then it defaults to newest version
  (v4.44).

- tables:

  A character vector specifying the names of particular dataframes to
  load from a specified version. If not specified then a list containing
  all the dataframes within the requested version is returned. For a
  description of the different tables present in the database please see
  below.

- ram_path:

  path to the local directory where the specified version of the RAM
  Legacy Stock Excel Assessment Database was downloaded. By default this
  path is set to within the rappdirs directory and can be viewed using
  calling the function
  [`ram_dir`](https://docs.ropensci.org/ramlegacy/reference/ram_dir.md)
  and specifying the version number inside the function call. Although
  this is not the **recommended** approach `load_ramlegacy` supports
  reading in the database's dataframes from a user-specified path
  provided that the database is present at the specified path as an rds
  object.

## Description of the dataframes present in the database

- metadata: Table with summarized metadata (only available in newer
  versions starting from v4.40)

- stock: This stores the stock database table

- assessment: This stores the assessment database table

- taxonomy: This stores the taxonomy database table

- management: This stores the management database table

- assessor: This stores the assessor database table

- assessmetod: This stores the assessmetod database table

- area: This stores the area database table

- biometrics: This stores the biometrics database table

- tsmetrics: This stores the tsmetrics database table

- timeseries: The time series data is a matrix object with the following
  headers/columns: (1) assessid (2) stockid (3) stocklong (4) tsid (5)
  tsyear (6) tsvalue

- bioparams: The parameter data is a matrix object with the following
  headers/columns: (1) assessid (2) stockid (3) stocklong (4) bioid (5)
  biovalue (6) bioyear (7) bionotes

- timeseries_values_views: This stores the timeseries values with
  timeseries type along the columns and stocks along the rows

- timeseries_units_views: This stores the timeseries values with
  timeseries type along the columns and stocks along the rows

- timeseries_ids_views: This stores the timeseries IDs with timeseries
  type along the columns and stocks along the rows

- timeseries_assessments_views: This stores the timeseries assessments
  with timeseries type along the columns and stocks along the rows

- timeseries_notes_views: This stores the timeseries notes with
  timeseries type along the columns and stocks along the rows

- timeseries_sources_views: This stores the timeseries sources with
  timeseries type along the columns and stocks along the rows

- timeseries_years_views: This stores the timeseries years with
  timeseries type along the columns and stocks along the rows

- bioparams_values_views: This stores the reference point values, with
  reference point type along the columns and stocks along the rows

- bioparams_units_views: This stores the reference point units, with
  reference point type along the columns and stocks along the rows

- bioparams_ids_views: This stores the reference point IDs, with
  reference point type along the columns and stocks along the rows

- bioparams_assessments_views: This stores the reference point
  assessments, with reference point type along the columns and stocks
  along the rows

- bioparams_sources_views: This stores the reference point sources, with
  reference point type along the columns and stocks along the rows

- bioparams_notes_views: This stores the reference point notes, with
  reference point type along the columns and stocks along the rows

## Newer versions (v4.40 onwards) also contains tables of individual most-used time series

- tb.data: Total Biomass

- ssb.data: Spawning Stock Biomass

- tn.data: Total Abundance

- r.data: Recruits

- tc.data: Total Catch

- tl.data: Total Landings

- recc.data: Recreational Catch

- f.data: Fishing Mortality

- er.data: Exploitation Rate

- divtb.data: TB/TBmsy

- divssb.data: SSB/SSBmsy

- ivf.data: F/Fmsy

- diver.data: ER/ERmsy

- divbpref.data: B/Bmsypref

- divupref.data: U/Umsypref

- tbbest.data: TBbest

- tcbest.data: TCbest

- erbest.data: ERbest

- divtb.mgt.data: TB/TBmgt

- divssb.mgt.data: SSB/SSBmgt

- divf.mgt.data: F/Fmgt

- diver.mgt.data: ER/ERmgt

- divbpref.mgt.data: B/Bmgtpref

- divupref.mgt.data: U/Umgtpref

- cpair.data: Cpair

- tac.data: TAC

- cadv.data: Cadvised

- survb.data: survB

- cpue.data: CPUE

- effort.data: EFFORT

## See also

Other ramlegacy functions:
[`download_ramlegacy`](https://docs.ropensci.org/ramlegacy/reference/download_ramlegacy.md),
[`ram_dir`](https://docs.ropensci.org/ramlegacy/reference/ram_dir.md)

## Examples

``` r
# \donttest{
# first download version 4.44 of the database
download_ramlegacy(version = "4.44")
#> ★ Downloading...this may take a while
#> ★ Finished Downloading. Now unzipping it...
#> ★ Saving the unzipped database as RDS object...
#> ✔ Version 4.44 successfully downloaded.

# get a list containing area and bioparams tables
# from version 4.44 database
load_ramlegacy(version = "4.44", tables = c("area", "bioparams"))
#>  Number of tables:  2 
#> ====================================== 
#> 'area':  821 obs. of 6 variables 
#> 'bioparams':  16204 obs. of 7 variables 
# }
```
