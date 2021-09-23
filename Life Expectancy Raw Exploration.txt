> life_expectancy<-read.csv("D:\\Life Expectancy Data.csv", header=TRUE)

> View(life_expectancy)

> head(life_expectancy)
      Country Year     Status Life.expectancy Adult.Mortality
1 Afghanistan 2015 Developing            65.0             263
2 Afghanistan 2014 Developing            59.9             271
3 Afghanistan 2013 Developing            59.9             268
4 Afghanistan 2012 Developing            59.5             272
5 Afghanistan 2011 Developing            59.2             275
6 Afghanistan 2010 Developing            58.8             279
  infant.deaths Alcohol percentage.expenditure Hepatitis.B
1            62    0.01              71.279624          65
2            64    0.01              73.523582          62
3            66    0.01              73.219243          64
4            69    0.01              78.184215          67
5            71    0.01               7.097109          68
6            74    0.01              79.679367          66
  Measles  BMI under.five.deaths Polio Total.expenditure
1    1154 19.1                83     6              8.16
2     492 18.6                86    58              8.18
3     430 18.1                89    62              8.13
4    2787 17.6                93    67              8.52
5    3013 17.2                97    68              7.87
6    1989 16.7               102    66              9.20
  Diphtheria HIV.AIDS       GDP Population thinness..1.19.years
1         65      0.1 584.25921   33736494                 17.2
2         62      0.1 612.69651     327582                 17.5
3         64      0.1 631.74498   31731688                 17.7
4         67      0.1 669.95900    3696958                 17.9
5         68      0.1  63.53723    2978599                 18.2
6         66      0.1 553.32894    2883167                 18.4
  thinness.5.9.years Income.composition.of.resources Schooling
1               17.3                           0.479      10.1
2               17.5                           0.476      10.0
3               17.7                           0.470       9.9
4               18.0                           0.463       9.8
5               18.2                           0.454       9.5
6               18.4                           0.448       9.2

> tail(life_expectancy)
      Country Year     Status Life.expectancy Adult.Mortality
2933 Zimbabwe 2005 Developing            44.6             717
2934 Zimbabwe 2004 Developing            44.3             723
2935 Zimbabwe 2003 Developing            44.5             715
2936 Zimbabwe 2002 Developing            44.8              73
2937 Zimbabwe 2001 Developing            45.3             686
2938 Zimbabwe 2000 Developing            46.0             665
     infant.deaths Alcohol percentage.expenditure Hepatitis.B
2933            28    4.14               8.717409          65
2934            27    4.36               0.000000          68
2935            26    4.06               0.000000           7
2936            25    4.43               0.000000          73
2937            25    1.72               0.000000          76
2938            24    1.68               0.000000          79
     Measles  BMI under.five.deaths Polio Total.expenditure
2933     420 27.5                43    69              6.44
2934      31 27.1                42    67              7.13
2935     998 26.7                41     7              6.52
2936     304 26.3                40    73              6.53
2937     529 25.9                39    76              6.16
2938    1483 25.5                39    78              7.10
     Diphtheria HIV.AIDS       GDP Population
2933         68     30.3 444.76575     129432
2934         65     33.6 454.36665   12777511
2935         68     36.7 453.35116   12633897
2936         71     39.8  57.34834     125525
2937         75     42.1 548.58731   12366165
2938         78     43.5 547.35888   12222251
     thinness..1.19.years thinness.5.9.years
2933                  9.0                9.0
2934                  9.4                9.4
2935                  9.8                9.9
2936                  1.2                1.3
2937                  1.6                1.7
2938                 11.0               11.2
     Income.composition.of.resources Schooling
2933                           0.406       9.3
2934                           0.407       9.2
2935                           0.418       9.5
2936                           0.427      10.0
2937                           0.427       9.8
2938                           0.434       9.8

> class(life_expectancy)
[1] "data.frame"

> length(life_expectancy)
[1] 22

> ncol(life_expectancy)
[1] 22

> names(life_expectancy)
 [1] "Country"                        
 [2] "Year"                           
 [3] "Status"                         
 [4] "Life.expectancy"                
 [5] "Adult.Mortality"                
 [6] "infant.deaths"                  
 [7] "Alcohol"                        
 [8] "percentage.expenditure"         
 [9] "Hepatitis.B"                    
[10] "Measles"                        
[11] "BMI"                            
[12] "under.five.deaths"              
[13] "Polio"                          
[14] "Total.expenditure"              
[15] "Diphtheria"                     
[16] "HIV.AIDS"                       
[17] "GDP"                            
[18] "Population"                     
[19] "thinness..1.19.years"           
[20] "thinness.5.9.years"             
[21] "Income.composition.of.resources"
[22] "Schooling"                      

> length(life_expectancy[ ,1])
[1] 2938

> nrow(life_expectancy)
[1] 2938

> ncol(life_expectancy[ ,1])
NULL

> length(life_expectancy[ ,1]/15)
Error in life_expectancy[, 1]/15 : 
  non-numeric argument to binary operator

> length(life_expectancy["Albania" ,"Year"])
[1] 1
> length(life_expectancy[ ,"Year"])
[1] 2938
> length(life_expectancy["Afghanistan",])
[1] 22
> length(life_expectancy["Afghanistan",])
[1] 22

> str(life_expectancy)
'data.frame':	2938 obs. of  22 variables:
 $ Country                        : chr  "Afghanistan" "Afghanistan" "Afghanistan" "Afghanistan" ...
 $ Year                           : int  2015 2014 2013 2012 2011 2010 2009 2008 2007 2006 ...
 $ Status                         : chr  "Developing" "Developing" "Developing" "Developing" ...
 $ Life.expectancy                : num  65 59.9 59.9 59.5 59.2 58.8 58.6 58.1 57.5 57.3 ...
 $ Adult.Mortality                : int  263 271 268 272 275 279 281 287 295 295 ...
 $ infant.deaths                  : int  62 64 66 69 71 74 77 80 82 84 ...
 $ Alcohol                        : num  0.01 0.01 0.01 0.01 0.01 0.01 0.01 0.03 0.02 0.03 ...
 $ percentage.expenditure         : num  71.3 73.5 73.2 78.2 7.1 ...
 $ Hepatitis.B                    : int  65 62 64 67 68 66 63 64 63 64 ...
 $ Measles                        : int  1154 492 430 2787 3013 1989 2861 1599 1141 1990 ...
 $ BMI                            : num  19.1 18.6 18.1 17.6 17.2 16.7 16.2 15.7 15.2 14.7 ...
 $ under.five.deaths              : int  83 86 89 93 97 102 106 110 113 116 ...
 $ Polio                          : int  6 58 62 67 68 66 63 64 63 58 ...
 $ Total.expenditure              : num  8.16 8.18 8.13 8.52 7.87 9.2 9.42 8.33 6.73 7.43 ...
 $ Diphtheria                     : int  65 62 64 67 68 66 63 64 63 58 ...
 $ HIV.AIDS                       : num  0.1 0.1 0.1 0.1 0.1 0.1 0.1 0.1 0.1 0.1 ...
 $ GDP                            : num  584.3 612.7 631.7 670 63.5 ...
 $ Population                     : num  33736494 327582 31731688 3696958 2978599 ...
 $ thinness..1.19.years           : num  17.2 17.5 17.7 17.9 18.2 18.4 18.6 18.8 19 19.2 ...
 $ thinness.5.9.years             : num  17.3 17.5 17.7 18 18.2 18.4 18.7 18.9 19.1 19.3 ...
 $ Income.composition.of.resources: num  0.479 0.476 0.47 0.463 0.454 0.448 0.434 0.433 0.415 0.405 ...
 $ Schooling                      : num  10.1 10 9.9 9.8 9.5 9.2 8.9 8.7 8.4 8.1 ...

> dplyr::glimpse(life_expectancy)
Error in loadNamespace(x) : there is no package called ‘dplyr’

> install.packages("dplyr")
WARNING: Rtools is required to build R packages but is not currently installed. Please download and install the appropriate version of Rtools before proceeding:

https://cran.rstudio.com/bin/windows/Rtools/
Installing package into ‘C:/Users/doome/Documents/R/win-library/4.1’
(as ‘lib’ is unspecified)
also installing the dependencies ‘purrr’, ‘generics’, ‘tidyselect’

trying URL 'https://cran.rstudio.com/bin/windows/contrib/4.1/purrr_0.3.4.zip'
Content type 'application/zip' length 430327 bytes (420 KB)
downloaded 420 KB

trying URL 'https://cran.rstudio.com/bin/windows/contrib/4.1/generics_0.1.0.zip'
Content type 'application/zip' length 71581 bytes (69 KB)
downloaded 69 KB

trying URL 'https://cran.rstudio.com/bin/windows/contrib/4.1/tidyselect_1.1.1.zip'
Content type 'application/zip' length 204470 bytes (199 KB)
downloaded 199 KB

trying URL 'https://cran.rstudio.com/bin/windows/contrib/4.1/dplyr_1.0.7.zip'
Content type 'application/zip' length 1345680 bytes (1.3 MB)
downloaded 1.3 MB

package ‘purrr’ successfully unpacked and MD5 sums checked
package ‘generics’ successfully unpacked and MD5 sums checked
package ‘tidyselect’ successfully unpacked and MD5 sums checked
package ‘dplyr’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\doome\AppData\Local\Temp\RtmpuW9PEE\downloaded_packages
> library(dplyr)

Attaching package: ‘dplyr’

The following objects are masked from ‘package:stats’:

    filter, lag

The following objects are masked from ‘package:base’:

    intersect, setdiff, setequal, union

Warning message:
package ‘dplyr’ was built under R version 4.1.1 

> glimpse(life_expectancy)
Rows: 2,938
Columns: 22
$ Country                         <chr> "Afghanistan", "Afghanistan", "Afghanistan", "Afghanistan"~
$ Year                            <int> 2015, 2014, 2013, 2012, 2011, 2010, 2009, 2008, 2007, 2006~
$ Status                          <chr> "Developing", "Developing", "Developing", "Developing", "D~
$ Life.expectancy                 <dbl> 65.0, 59.9, 59.9, 59.5, 59.2, 58.8, 58.6, 58.1, 57.5, 57.3~
$ Adult.Mortality                 <int> 263, 271, 268, 272, 275, 279, 281, 287, 295, 295, 291, 293~
$ infant.deaths                   <int> 62, 64, 66, 69, 71, 74, 77, 80, 82, 84, 85, 87, 87, 88, 88~
$ Alcohol                         <dbl> 0.01, 0.01, 0.01, 0.01, 0.01, 0.01, 0.01, 0.03, 0.02, 0.03~
$ percentage.expenditure          <dbl> 71.279624, 73.523582, 73.219243, 78.184215, 7.097109, 79.6~
$ Hepatitis.B                     <int> 65, 62, 64, 67, 68, 66, 63, 64, 63, 64, 66, 67, 65, 64, 63~
$ Measles                         <int> 1154, 492, 430, 2787, 3013, 1989, 2861, 1599, 1141, 1990, ~
$ BMI                             <dbl> 19.1, 18.6, 18.1, 17.6, 17.2, 16.7, 16.2, 15.7, 15.2, 14.7~
$ under.five.deaths               <int> 83, 86, 89, 93, 97, 102, 106, 110, 113, 116, 118, 120, 122~
$ Polio                           <int> 6, 58, 62, 67, 68, 66, 63, 64, 63, 58, 58, 5, 41, 36, 35, ~
$ Total.expenditure               <dbl> 8.16, 8.18, 8.13, 8.52, 7.87, 9.20, 9.42, 8.33, 6.73, 7.43~
$ Diphtheria                      <int> 65, 62, 64, 67, 68, 66, 63, 64, 63, 58, 58, 5, 41, 36, 33,~
$ HIV.AIDS                        <dbl> 0.1, 0.1, 0.1, 0.1, 0.1, 0.1, 0.1, 0.1, 0.1, 0.1, 0.1, 0.1~
$ GDP                             <dbl> 584.25921, 612.69651, 631.74498, 669.95900, 63.53723, 553.~
$ Population                      <dbl> 33736494, 327582, 31731688, 3696958, 2978599, 2883167, 284~
$ thinness..1.19.years            <dbl> 17.2, 17.5, 17.7, 17.9, 18.2, 18.4, 18.6, 18.8, 19.0, 19.2~
$ thinness.5.9.years              <dbl> 17.3, 17.5, 17.7, 18.0, 18.2, 18.4, 18.7, 18.9, 19.1, 19.3~
$ Income.composition.of.resources <dbl> 0.479, 0.476, 0.470, 0.463, 0.454, 0.448, 0.434, 0.433, 0.~
$ Schooling                       <dbl> 10.1, 10.0, 9.9, 9.8, 9.5, 9.2, 8.9, 8.7, 8.4, 8.1, 7.9, 6~
> plot(life_expectancy$Life.expectancy,life_expectancy$Year)

> idx<-identify(life_expectancy$Life.expectancy,life_expectancy$Year)

> idx<-identify(life_expectancy$Life.expectancy,life_expectancy$Country)
Warning message:
In xy.coords(x, y, setLab = FALSE) : NAs introduced by coercion

> idx<-identify(life_expectancy$Life.expectancy,life_expectancy$Country)
Error in identify.default(life_expectancy$Life.expectancy, life_expectancy$Country) : 
  plot.new has not been called yet
In addition: Warning message:
In xy.coords(x, y, setLab = FALSE) : NAs introduced by coercion


> plot(life_expectancy$Life.expectancy,life_expectancy$Year, xlab = "Life Expectancy", ylab = "Per year", main = "Life Expectancy Per Year plot")
> plot(life_expectancy$Life.expectancy,life_expectancy$Year, xlab = "Life Expectancy", ylab = "Per year", main = "Life Expectancy Per Year plot", col = "blue")

> plot(life_expectancy$Life.expectancy,life_expectancy$Year, xlab = "Life Expectancy", ylab = "Per year", main = "Life Expectancy Per Year plot", col = "blue")
> barplot(life_expectancy$Life.expectancy,life_expectancy$Year)
> barplot(life_expectancy$Life.expectancy,life_expectancy$Year, xlab = "Life Expectancy", ylab = "Per year", main = "Life Expectancy Per Year plot", col = "blue")

> summary(life_expectancy)
   Country               Year         Status          Life.expectancy Adult.Mortality
 Length:2938        Min.   :2000   Length:2938        Min.   :36.30   Min.   :  1.0  
 Class :character   1st Qu.:2004   Class :character   1st Qu.:63.10   1st Qu.: 74.0  
 Mode  :character   Median :2008   Mode  :character   Median :72.10   Median :144.0  
                    Mean   :2008                      Mean   :69.22   Mean   :164.8  
                    3rd Qu.:2012                      3rd Qu.:75.70   3rd Qu.:228.0  
                    Max.   :2015                      Max.   :89.00   Max.   :723.0  
                                                      NA's   :10      NA's   :10     
 infant.deaths       Alcohol        percentage.expenditure  Hepatitis.B   
 Min.   :   0.0   Min.   : 0.0100   Min.   :    0.000      Min.   : 1.00  
 1st Qu.:   0.0   1st Qu.: 0.8775   1st Qu.:    4.685      1st Qu.:77.00  
 Median :   3.0   Median : 3.7550   Median :   64.913      Median :92.00  
 Mean   :  30.3   Mean   : 4.6029   Mean   :  738.251      Mean   :80.94  
 3rd Qu.:  22.0   3rd Qu.: 7.7025   3rd Qu.:  441.534      3rd Qu.:97.00  
 Max.   :1800.0   Max.   :17.8700   Max.   :19479.912      Max.   :99.00  
                  NA's   :194                              NA's   :553    
    Measles              BMI        under.five.deaths     Polio       Total.expenditure
 Min.   :     0.0   Min.   : 1.00   Min.   :   0.00   Min.   : 3.00   Min.   : 0.370   
 1st Qu.:     0.0   1st Qu.:19.30   1st Qu.:   0.00   1st Qu.:78.00   1st Qu.: 4.260   
 Median :    17.0   Median :43.50   Median :   4.00   Median :93.00   Median : 5.755   
 Mean   :  2419.6   Mean   :38.32   Mean   :  42.04   Mean   :82.55   Mean   : 5.938   
 3rd Qu.:   360.2   3rd Qu.:56.20   3rd Qu.:  28.00   3rd Qu.:97.00   3rd Qu.: 7.492   
 Max.   :212183.0   Max.   :87.30   Max.   :2500.00   Max.   :99.00   Max.   :17.600   
                    NA's   :34                        NA's   :19      NA's   :226      
   Diphtheria       HIV.AIDS           GDP              Population       
 Min.   : 2.00   Min.   : 0.100   Min.   :     1.68   Min.   :3.400e+01  
 1st Qu.:78.00   1st Qu.: 0.100   1st Qu.:   463.94   1st Qu.:1.958e+05  
 Median :93.00   Median : 0.100   Median :  1766.95   Median :1.387e+06  
 Mean   :82.32   Mean   : 1.742   Mean   :  7483.16   Mean   :1.275e+07  
 3rd Qu.:97.00   3rd Qu.: 0.800   3rd Qu.:  5910.81   3rd Qu.:7.420e+06  
 Max.   :99.00   Max.   :50.600   Max.   :119172.74   Max.   :1.294e+09  
 NA's   :19                       NA's   :448         NA's   :652        
 thinness..1.19.years thinness.5.9.years Income.composition.of.resources   Schooling    
 Min.   : 0.10        Min.   : 0.10      Min.   :0.0000                  Min.   : 0.00  
 1st Qu.: 1.60        1st Qu.: 1.50      1st Qu.:0.4930                  1st Qu.:10.10  
 Median : 3.30        Median : 3.30      Median :0.6770                  Median :12.30  
 Mean   : 4.84        Mean   : 4.87      Mean   :0.6276                  Mean   :11.99  
 3rd Qu.: 7.20        3rd Qu.: 7.20      3rd Qu.:0.7790                  3rd Qu.:14.30  
 Max.   :27.70        Max.   :28.60      Max.   :0.9480                  Max.   :20.70  
 NA's   :34           NA's   :34         NA's   :167                     NA's   :163 
 
 > life_expectancy$ProminentDiseaseDeathsperPopulation<-(life_expectancy$Hepatitis.B+life_expectancy$Measles+life_expectancy$Measles)/life_expectancy$Population
 
 > write.table(life_expectancy,"Life Expectancy Modified.txt", sep="\t", row.names = FALSE)
 
 > life_expectancy
       Country Year     Status Life.expectancy Adult.Mortality infant.deaths Alcohol
1  Afghanistan 2015 Developing            65.0             263            62    0.01
2  Afghanistan 2014 Developing            59.9             271            64    0.01
3  Afghanistan 2013 Developing            59.9             268            66    0.01
4  Afghanistan 2012 Developing            59.5             272            69    0.01
5  Afghanistan 2011 Developing            59.2             275            71    0.01
6  Afghanistan 2010 Developing            58.8             279            74    0.01
7  Afghanistan 2009 Developing            58.6             281            77    0.01
8  Afghanistan 2008 Developing            58.1             287            80    0.03
9  Afghanistan 2007 Developing            57.5             295            82    0.02
10 Afghanistan 2006 Developing            57.3             295            84    0.03
11 Afghanistan 2005 Developing            57.3             291            85    0.02
12 Afghanistan 2004 Developing            57.0             293            87    0.02
13 Afghanistan 2003 Developing            56.7             295            87    0.01
14 Afghanistan 2002 Developing            56.2               3            88    0.01
15 Afghanistan 2001 Developing            55.3             316            88    0.01
16 Afghanistan 2000 Developing            54.8             321            88    0.01
17     Albania 2015 Developing            77.8              74             0    4.60
18     Albania 2014 Developing            77.5               8             0    4.51
19     Albania 2013 Developing            77.2              84             0    4.76
20     Albania 2012 Developing            76.9              86             0    5.14
21     Albania 2011 Developing            76.6              88             0    5.37
22     Albania 2010 Developing            76.2              91             1    5.28
23     Albania 2009 Developing            76.1              91             1    5.79
24     Albania 2008 Developing            75.3               1             1    5.61
25     Albania 2007 Developing            75.9               9             1    5.58
26     Albania 2006 Developing            74.2              99             1    5.31
27     Albania 2005 Developing            73.5              15             1    5.16
28     Albania 2004 Developing            73.0              17             1    4.54
29     Albania 2003 Developing            72.8              18             1    4.29
30     Albania 2002 Developing            73.3              15             1    3.73
31     Albania 2001 Developing            73.6              14             1    4.25
32     Albania 2000 Developing            72.6              11             1    3.66
33     Algeria 2015 Developing            75.6              19            21      NA
34     Algeria 2014 Developing            75.4              11            21    0.01
35     Algeria 2013 Developing            75.3             112            21    0.53
36     Algeria 2012 Developing            75.1             113            21    0.66
37     Algeria 2011 Developing            74.9             116            21    0.56
38     Algeria 2010 Developing            74.7             119            21    0.45
39     Algeria 2009 Developing            74.4             123            20    0.50
40     Algeria 2008 Developing            74.1             126            20    0.46
41     Algeria 2007 Developing            73.8             129            20    0.44
42     Algeria 2006 Developing            73.4             132            20    0.36
43     Algeria 2005 Developing            72.9             136            19    0.50
   percentage.expenditure Hepatitis.B Measles  BMI under.five.deaths Polio
1               71.279624          65    1154 19.1                83     6
2               73.523582          62     492 18.6                86    58
3               73.219243          64     430 18.1                89    62
4               78.184215          67    2787 17.6                93    67
5                7.097109          68    3013 17.2                97    68
6               79.679367          66    1989 16.7               102    66
7               56.762217          63    2861 16.2               106    63
8               25.873925          64    1599 15.7               110    64
9               10.910156          63    1141 15.2               113    63
10              17.171518          64    1990 14.7               116    58
11               1.388648          66    1296 14.2               118    58
12              15.296066          67     466 13.8               120     5
13              11.089053          65     798 13.4               122    41
14              16.887351          64    2486 13.0               122    36
15              10.574728          63    8762 12.6               122    35
16              10.424960          62    6532 12.2               122    24
17             364.975229          99       0 58.0                 0    99
18             428.749067          98       0 57.2                 1    98
19             430.876979          99       0 56.5                 1    99
20             412.443356          99       9 55.8                 1    99
21             437.062100          99      28 55.1                 1    99
22              41.822757          99      10 54.3                 1    99
23             348.055952          98       0 53.5                 1    98
24              36.622068          99       0 52.6                 1    99
25              32.246552          98      22 51.7                 1    99
26               3.302154          98      68  5.8                 1    97
27              26.993121          98       6 49.9                 1    97
28             221.842800          99       7 48.9                 1    98
29              14.719289          97       8 47.9                 1    97
30             104.516916          96      16 46.9                 1    98
31              96.205571          96      18 46.0                 1    97
32              91.711541          96     662 45.0                 1    97
33               0.000000          95      63 59.5                24    95
34              54.237318          95       0 58.4                24    95
35             544.450743          95      25 57.2                24    95
36             555.926083          95      18 56.1                24    95
37             509.002041          95     112 55.0                24    95
38             430.717586          95     103 53.9                24    95
39             352.063642          94     107 52.8                23    94
40              43.087173          91     217 51.8                23    92
41             320.323924           9       0  5.8                23    95
42             270.240196           8     944 49.8                23    95
43               2.548923          83    2302 48.9                22    88
   Total.expenditure Diphtheria HIV.AIDS        GDP Population thinness..1.19.years
1               8.16         65      0.1  584.25921   33736494                 17.2
2               8.18         62      0.1  612.69651     327582                 17.5
3               8.13         64      0.1  631.74498   31731688                 17.7
4               8.52         67      0.1  669.95900    3696958                 17.9
5               7.87         68      0.1   63.53723    2978599                 18.2
6               9.20         66      0.1  553.32894    2883167                 18.4
7               9.42         63      0.1  445.89330     284331                 18.6
8               8.33         64      0.1  373.36112    2729431                 18.8
9               6.73         63      0.1  369.83580   26616792                 19.0
10              7.43         58      0.1  272.56377    2589345                 19.2
11              8.70         58      0.1   25.29413     257798                 19.3
12              8.79          5      0.1  219.14135   24118979                 19.5
13              8.82         41      0.1  198.72854    2364851                 19.7
14              7.76         36      0.1  187.84595   21979923                 19.9
15              7.80         33      0.1  117.49698    2966463                  2.1
16              8.20         24      0.1  114.56000     293756                  2.3
17              6.00         99      0.1 3954.22783      28873                  1.2
18              5.88         98      0.1 4575.76379     288914                  1.2
19              5.66         99      0.1 4414.72314     289592                  1.3
20              5.59         99      0.1 4247.61438       2941                  1.3
21              5.71         99      0.1 4437.17868     295195                  1.4
22              5.34         99      0.1  494.35883     291321                  1.4
23              5.79         98      0.1 4114.13655    2927519                  1.5
24              5.87         99      0.1  437.53965    2947314                  1.6
25              6.10         98      0.1  363.13685      29717                  1.6
26              5.86         97      0.1   35.12930    2992547                  1.7
27              6.12         98      0.1  279.14293     311487                  1.8
28              6.38         97      0.1 2416.58824     326939                  1.8
29              6.27         97      0.1  189.68156     339616                  1.9
30              6.30         98      0.1 1453.64278       3511                  2.0
31              6.00         97      0.1 1326.97339      36173                  2.1
32              6.26         97      0.1 1175.78898      38927                  2.1
33                NA         95      0.1 4132.76292   39871528                  6.0
34              7.21         95      0.1  547.85170   39113313                  6.0
35              7.12         95      0.1 5471.86677   38338562                  5.9
36              6.14         95      0.1 5564.82566   37565847                  5.9
37              5.29         95      0.1 5432.25230   36819558                  5.9
38              5.12         95      0.1 4463.39467   36117637                  5.9
39              5.36         95      0.1 3868.83123    3546576                  6.0
40              4.20         93      0.1  495.25487    3486715                  6.0
41              3.82         95      0.1 3935.18334      34376                  6.0
42              3.36         95      0.1 3464.61790   33777915                  6.1
43              3.24         88      0.1   31.12238   33288437                  6.1
   thinness.5.9.years Income.composition.of.resources Schooling
1                17.3                           0.479      10.1
2                17.5                           0.476      10.0
3                17.7                           0.470       9.9
4                18.0                           0.463       9.8
5                18.2                           0.454       9.5
6                18.4                           0.448       9.2
7                18.7                           0.434       8.9
8                18.9                           0.433       8.7
9                19.1                           0.415       8.4
10               19.3                           0.405       8.1
11               19.5                           0.396       7.9
12               19.7                           0.381       6.8
13               19.9                           0.373       6.5
14                2.2                           0.341       6.2
15                2.4                           0.340       5.9
16                2.5                           0.338       5.5
17                1.3                           0.762      14.2
18                1.3                           0.761      14.2
19                1.4                           0.759      14.2
20                1.4                           0.752      14.2
21                1.5                           0.738      13.3
22                1.5                           0.725      12.5
23                1.6                           0.721      12.2
24                1.6                           0.713      12.0
25                1.7                           0.703      11.6
26                1.8                           0.696      11.4
27                1.8                           0.685      10.8
28                1.9                           0.681      10.9
29                2.0                           0.674      10.7
30                2.1                           0.670      10.7
31                2.1                           0.662      10.6
32                2.2                           0.656      10.7
33                5.8                           0.743      14.4
34                5.8                           0.741      14.4
35                5.8                           0.737      14.4
36                5.8                           0.732      14.4
37                5.8                           0.724      14.0
38                5.8                           0.714      13.6
39                5.9                           0.705      13.1
40                5.9                           0.697      12.6
41                5.9                           0.690      12.3
42                6.0                           0.686      12.3
43                6.0                           0.680      12.0
   ProminentDiseaseDeathsperPopulation
1                         7.033926e-05
2                         3.193094e-03
3                         2.911916e-05
4                         1.525849e-03
5                         2.045928e-03
6                         1.402624e-03
7                         2.034601e-02
8                         1.195121e-03
9                         8.810228e-05
10                        1.561785e-03
11                        1.031040e-02
12                        4.141966e-05
13                        7.023698e-04
14                        2.291182e-04
15                        5.928609e-03
16                        4.468334e-02
17                        3.428809e-03
18                        3.392013e-04
19                        3.418603e-04
20                        3.978239e-02
21                        5.250766e-04
22                        4.084841e-04
23                        3.347544e-05
24                        3.358991e-05
25                        4.778410e-03
26                        7.819426e-05
27                        3.531448e-04
28                        3.456302e-04
29                        3.327287e-04
30                        3.645685e-02
31                        3.649131e-03
32                        3.647854e-02
33                        5.542802e-06
34                        2.428841e-06
35                        3.782093e-06
36                        3.487210e-06
37                        8.663874e-06
38                        8.333879e-06
39                        8.684433e-05
40                        1.505715e-04
41                        2.618106e-04
42                        5.613135e-05
43                        1.407996e-04
 [ reached 'max' / getOption("max.print") -- omitted 2895 rows ]


is.na(life_expectancy$Year)
   [1] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [15] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [29] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [43] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [57] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [71] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [85] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [99] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [113] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [127] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [141] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [155] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [169] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [183] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [197] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [211] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [225] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [239] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [253] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [267] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [281] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [295] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [309] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [323] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [337] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [351] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [365] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [379] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [393] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [407] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [421] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [435] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [449] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [463] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [477] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [491] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [505] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [519] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [533] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [547] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [561] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [575] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [589] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [603] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [617] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [631] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [645] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [659] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [673] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [687] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [701] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [715] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [729] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [743] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [757] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [771] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [785] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [799] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [813] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [827] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [841] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [855] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [869] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [883] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [897] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [911] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [925] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [939] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [953] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [967] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [981] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [995] FALSE FALSE FALSE FALSE FALSE FALSE
 [ reached getOption("max.print") -- omitted 1938 entries ]
> is.na(life_expectancy$Life.expectancy)
   [1] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [15] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [29] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [43] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [57] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [71] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [85] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
  [99] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [113] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [127] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [141] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [155] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [169] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [183] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [197] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [211] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [225] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [239] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [253] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [267] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [281] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [295] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [309] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [323] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [337] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [351] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [365] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [379] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [393] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [407] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [421] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [435] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [449] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [463] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [477] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [491] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [505] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [519] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [533] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [547] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [561] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [575] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [589] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [603] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [617] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE FALSE
 [631] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [645] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [659] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [673] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [687] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [701] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [715] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [729] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [743] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [757] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE  TRUE
 [771] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [785] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [799] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [813] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [827] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [841] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [855] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [869] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [883] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [897] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [911] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [925] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [939] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [953] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [967] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [981] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
 [995] FALSE FALSE FALSE FALSE FALSE FALSE
 [ reached getOption("max.print") -- omitted 1938 entries ]
> y<-na.omit(life_expectancy$Life.expectancy)
> length(y)
[1] 2928
