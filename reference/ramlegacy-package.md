# ramlegacy: download, cache and read RAM Legacy Stock Assessment Database

ramlegacy contains functions to download, cache and read in specified
tables from the excel version of the RAM Legacy Stock Assessment
Database, an online compilation of stock assessment results for
commercially exploited marine populations from around the world. More
information about the database can be found at
\<https://ramlegacy.org/\>.

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

## References

Ricard, D., Minto, C., Jensen, O.P. and Baum, J.K. (2012) Evaluating the
knowledge base and status of commercially exploited marine species with
the RAM Legacy Stock Assessment Database. Fish and Fisheries 13 (4)
380-398. \<doi:10.1111/j.1467-2979.2011.00435.x\>

## See also

[www.ramlegacy.org](https://docs.ropensci.org/ramlegacy/reference/www.ramlegacy.org)

[www.github.com/ropensci/ramlegacy](https://docs.ropensci.org/ramlegacy/reference/www.github.com/ropensci/ramlegacy)

[www.github.com/ropensci/ramlegacy/issues](https://docs.ropensci.org/ramlegacy/reference/www.github.com/ropensci/ramlegacy/issues)

## Author

**Maintainer**: Kshitiz Gupta <kshtzgupta1@berkeley.edu> \[copyright
holder\]

Authors:

- Carl Boettiger <cboettig@gmail.com>
  (http://orcid.org/0000-0002-1642-628X) \[copyright holder\]

Other contributors:

- Sam Albers <sam.albers@gmail.com>
  (https://orcid.org/0000-0002-9270-7884) \[reviewer\]

- Jamie Afflerbach <afflerbach@nceas.ucsb.edu>
  (https://orcid.org/0000-0002-5215-9342) \[reviewer\]

- RAM Legacy Stock Assessment Database \[data contributor\]
