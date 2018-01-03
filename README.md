
presidential\_election\_county\_results\_2016
=============================================

presidential\_election\_county\_results\_2016

tidy election results updated 11/13/2016

the two files are identical. different names provided for continuity.

***UPDATED JAN 3, 2018***

Data
----

Find the most up-to-date version of the data as a CSV or RDS (R data file) in the data directory.

### Long format

[Long format as .csv](data/pres.elect16.results.2018.csv): ./data/pres.elect16.results.2018.csv

``` r
## long format CSV
readr::read_csv("data/pres.elect16.results.2018.csv")
Parsed with column specification:
cols(
  county = col_character(),
  fips = col_character(),
  cand = col_character(),
  st = col_character(),
  pct_report = col_integer(),
  votes = col_integer(),
  total_votes = col_integer(),
  lead = col_character(),
  pct = col_double(),
  state.name = col_character()
)
# A tibble: 18,351 x 10
   county  fips                     cand    st pct_report    votes
    <chr> <chr>                    <chr> <chr>      <int>    <int>
 1   <NA>    US             Donald Trump    US          1 62984825
 2   <NA>    US          Hillary Clinton    US          1 65853516
 3   <NA>    US             Gary Johnson    US          1  4489221
 4   <NA>    US               Jill Stein    US          1  1429596
 5   <NA>    US            Evan McMullin    US          1   510002
 6   <NA>    US           Darrell Castle    US          1   186545
 7   <NA>    US           Gloria La Riva    US          1    74117
 8   <NA>    US       Rocky De La Fuente    US          1    33010
 9   <NA>    US None of these candidates    US          1    28863
10   <NA>    US           Richard Duncan    US          1    24235
# ... with 18,341 more rows, and 4 more variables: total_votes <int>,
#   lead <chr>, pct <dbl>, state.name <chr>
```

[Long format as .rds](data/pres.elect16.results.2018.rds): ./data/pres.elect16.results.2018.rds

``` r
## wide vote share data RDS
readr::read_rds("data/pres.elect16.results.2018.rds")
                           county  fips                      cand st
1                            <NA>    US              Donald Trump US
2                            <NA>    US           Hillary Clinton US
3                            <NA>    US              Gary Johnson US
4                            <NA>    US                Jill Stein US
5                            <NA>    US             Evan McMullin US
6                            <NA>    US            Darrell Castle US
7                            <NA>    US            Gloria La Riva US
8                            <NA>    US        Rocky De La Fuente US
9                            <NA>    US  None of these candidates US
10                           <NA>    US            Richard Duncan US
      pct_report    votes total_votes            lead         pct
1              1 62984825   135691978    Donald Trump 0.464175008
2              1 65853516   135691978    Donald Trump 0.485316206
3              1  4489221   135691978    Donald Trump 0.033083909
4              1  1429596   135691978    Donald Trump 0.010535597
5              1   510002   135691978    Donald Trump 0.003758527
6              1   186545   135691978    Donald Trump 0.001374768
7              1    74117   135691978    Donald Trump 0.000546215
8              1    33010   135691978    Donald Trump 0.000243272
9              1    28863   135691978    Donald Trump 0.000212710
10             1    24235   135691978    Donald Trump 0.000178603
          state.name
1               <NA>
2               <NA>
3               <NA>
4               <NA>
5               <NA>
6               <NA>
7               <NA>
8               <NA>
9               <NA>
10              <NA>
 [ reached getOption("max.print") -- omitted 18341 rows ]
```

Wide format - vote share
------------------------

[Wide format vote share in .csv](data/pres.elect16.results.wide.pct.2018.csv): ./data/pres.elect16.results.wide.pct.2018.csv

``` r
## wide vote share data CSV
readr::read_csv("data/pres.elect16.results.wide.pct.2018.csv")
Parsed with column specification:
cols(
  .default = col_double(),
  county = col_character(),
  fips = col_character(),
  st = col_character(),
  pct_report = col_integer(),
  total_votes = col_integer(),
  lead = col_character(),
  state.name = col_character()
)
See spec(...) for full column specifications.
# A tibble: 3,165 x 39
   county  fips    st pct_report total_votes            lead
    <chr> <chr> <chr>      <int>       <int>           <chr>
 1   <NA>    US    US          1   135691978    Donald Trump
 2   <NA>    CA    CA          1    14060856 Hillary Clinton
 3   <NA>    FL    FL          1     9419886    Donald Trump
 4   <NA>    TX    TX          1     8917965    Donald Trump
 5   <NA>    NY    NY          1     7660190 Hillary Clinton
 6   <NA>    PA    PA          1     6115402    Donald Trump
 7   <NA>    IL    IL          1     5523142 Hillary Clinton
 8   <NA>    OH    OH          1     5480173    Donald Trump
 9   <NA>    MI    MI          1     4790329    Donald Trump
10   <NA>    NC    NC          1     4682073    Donald Trump
# ... with 3,155 more rows, and 33 more variables: state.name <chr>, `None
#   of these candidates` <dbl>, `Alyson Kennedy` <dbl>, `Bradford
#   Lyttle` <dbl>, `Chris Keniston` <dbl>, `Dan Vacek` <dbl>, `Darrell
#   Castle` <dbl>, `Donald Trump` <dbl>, `Emidio Soltysik` <dbl>, `Evan
#   McMullin` <dbl>, `Frank Atwood` <dbl>, `Gary Johnson` <dbl>, `Gloria
#   La Riva` <dbl>, `Hillary Clinton` <dbl>, `Jerry White` <dbl>, `Jill
#   Stein` <dbl>, `Jim Hedges` <dbl>, `Joseph Maldonado` <dbl>, `Kyle
#   Kopitke` <dbl>, `Laurence Kotlikoff` <dbl>, `Lynn Kahn` <dbl>,
#   `Michael Maturen` <dbl>, `Mike Smith` <dbl>, `Monica Moorehead` <dbl>,
#   `Peter Skewes` <dbl>, `Princess Jacob` <dbl>, `Richard Duncan` <dbl>,
#   `Rocky De La Fuente` <dbl>, `Rocky Giordani` <dbl>, `Rod Silva` <dbl>,
#   `Ryan Scott` <dbl>, `Scott Copeland` <dbl>, `Tom Hoefling` <dbl>
```

[Wide format vote share in .rds](data/pres.elect16.results.wide.pct.2018.rds): ./data/pres.elect16.results.wide.pct.2018.rds

``` r
## wide vote share data RDS
readr::read_rds("data/pres.elect16.results.wide.pct.2018.rds")
# A tibble: 3,165 x 39
   county  fips    st pct_report total_votes            lead
 *  <chr> <chr> <chr>      <dbl>       <int>           <chr>
 1   <NA>    US    US          1   135691978    Donald Trump
 2   <NA>    CA    CA          1    14060856 Hillary Clinton
 3   <NA>    FL    FL          1     9419886    Donald Trump
 4   <NA>    TX    TX          1     8917965    Donald Trump
 5   <NA>    NY    NY          1     7660190 Hillary Clinton
 6   <NA>    PA    PA          1     6115402    Donald Trump
 7   <NA>    IL    IL          1     5523142 Hillary Clinton
 8   <NA>    OH    OH          1     5480173    Donald Trump
 9   <NA>    MI    MI          1     4790329    Donald Trump
10   <NA>    NC    NC          1     4682073    Donald Trump
# ... with 3,155 more rows, and 33 more variables: state.name <chr>, `
#   None of these candidates` <dbl>, `Alyson Kennedy` <dbl>, `Bradford
#   Lyttle` <dbl>, `Chris Keniston` <dbl>, `Dan Vacek` <dbl>, `Darrell
#   Castle` <dbl>, `Donald Trump` <dbl>, `Emidio Soltysik` <dbl>, `Evan
#   McMullin` <dbl>, `Frank Atwood` <dbl>, `Gary Johnson` <dbl>, `Gloria
#   La Riva` <dbl>, `Hillary Clinton` <dbl>, `Jerry White` <dbl>, `Jill
#   Stein` <dbl>, `Jim Hedges` <dbl>, `Joseph Maldonado` <dbl>, `Kyle
#   Kopitke` <dbl>, `Laurence Kotlikoff` <dbl>, `Lynn Kahn` <dbl>,
#   `Michael Maturen` <dbl>, `Mike Smith` <dbl>, `Monica Moorehead` <dbl>,
#   `Peter Skewes` <dbl>, `Princess Jacob` <dbl>, `Richard Duncan` <dbl>,
#   `Rocky De La Fuente` <dbl>, `Rocky Giordani` <dbl>, `Rod Silva` <dbl>,
#   `Ryan Scott` <dbl>, `Scott Copeland` <dbl>, `Tom Hoefling` <dbl>
```

Wide Format - total votes
-------------------------

[Wide format total votes in .csv](data/pres.elect16.results.wide.votes.2018.csv): ./data/pres.elect16.results.wide.pct.2018.csv

``` r
## wide vote totals data CSV
readr::read_csv("data/pres.elect16.results.wide.votes.2018.csv")
Parsed with column specification:
cols(
  .default = col_integer(),
  county = col_character(),
  fips = col_character(),
  st = col_character(),
  lead = col_character(),
  state.name = col_character()
)
See spec(...) for full column specifications.
# A tibble: 3,165 x 39
   county  fips    st pct_report total_votes            lead
    <chr> <chr> <chr>      <int>       <int>           <chr>
 1   <NA>    US    US          1   135691978    Donald Trump
 2   <NA>    CA    CA          1    14060856 Hillary Clinton
 3   <NA>    FL    FL          1     9419886    Donald Trump
 4   <NA>    TX    TX          1     8917965    Donald Trump
 5   <NA>    NY    NY          1     7660190 Hillary Clinton
 6   <NA>    PA    PA          1     6115402    Donald Trump
 7   <NA>    IL    IL          1     5523142 Hillary Clinton
 8   <NA>    OH    OH          1     5480173    Donald Trump
 9   <NA>    MI    MI          1     4790329    Donald Trump
10   <NA>    NC    NC          1     4682073    Donald Trump
# ... with 3,155 more rows, and 33 more variables: state.name <chr>, `None
#   of these candidates` <int>, `Alyson Kennedy` <int>, `Bradford
#   Lyttle` <int>, `Chris Keniston` <int>, `Dan Vacek` <int>, `Darrell
#   Castle` <int>, `Donald Trump` <int>, `Emidio Soltysik` <int>, `Evan
#   McMullin` <int>, `Frank Atwood` <int>, `Gary Johnson` <int>, `Gloria
#   La Riva` <int>, `Hillary Clinton` <int>, `Jerry White` <int>, `Jill
#   Stein` <int>, `Jim Hedges` <int>, `Joseph Maldonado` <int>, `Kyle
#   Kopitke` <int>, `Laurence Kotlikoff` <int>, `Lynn Kahn` <int>,
#   `Michael Maturen` <int>, `Mike Smith` <int>, `Monica Moorehead` <int>,
#   `Peter Skewes` <int>, `Princess Jacob` <int>, `Richard Duncan` <int>,
#   `Rocky De La Fuente` <int>, `Rocky Giordani` <int>, `Rod Silva` <int>,
#   `Ryan Scott` <int>, `Scott Copeland` <int>, `Tom Hoefling` <int>
```

[Wide format total votes in .rds](data/pres.elect16.results.wide.votes.2018.rds): ./data/pres.elect16.results.wide.pct.2018.rds

``` r
## wide vote share data RDS
readr::read_rds("data/pres.elect16.results.wide.votes.2018.rds")
# A tibble: 3,165 x 39
   county  fips    st pct_report total_votes            lead
 *  <chr> <chr> <chr>      <dbl>       <int>           <chr>
 1   <NA>    US    US          1   135691978    Donald Trump
 2   <NA>    CA    CA          1    14060856 Hillary Clinton
 3   <NA>    FL    FL          1     9419886    Donald Trump
 4   <NA>    TX    TX          1     8917965    Donald Trump
 5   <NA>    NY    NY          1     7660190 Hillary Clinton
 6   <NA>    PA    PA          1     6115402    Donald Trump
 7   <NA>    IL    IL          1     5523142 Hillary Clinton
 8   <NA>    OH    OH          1     5480173    Donald Trump
 9   <NA>    MI    MI          1     4790329    Donald Trump
10   <NA>    NC    NC          1     4682073    Donald Trump
# ... with 3,155 more rows, and 33 more variables: state.name <chr>, `
#   None of these candidates` <int>, `Alyson Kennedy` <int>, `Bradford
#   Lyttle` <int>, `Chris Keniston` <int>, `Dan Vacek` <int>, `Darrell
#   Castle` <int>, `Donald Trump` <int>, `Emidio Soltysik` <int>, `Evan
#   McMullin` <int>, `Frank Atwood` <int>, `Gary Johnson` <int>, `Gloria
#   La Riva` <int>, `Hillary Clinton` <int>, `Jerry White` <int>, `Jill
#   Stein` <int>, `Jim Hedges` <int>, `Joseph Maldonado` <int>, `Kyle
#   Kopitke` <int>, `Laurence Kotlikoff` <int>, `Lynn Kahn` <int>,
#   `Michael Maturen` <int>, `Mike Smith` <int>, `Monica Moorehead` <int>,
#   `Peter Skewes` <int>, `Princess Jacob` <int>, `Richard Duncan` <int>,
#   `Rocky De La Fuente` <int>, `Rocky Giordani` <int>, `Rod Silva` <int>,
#   `Ryan Scott` <int>, `Scott Copeland` <int>, `Tom Hoefling` <int>
```
