# Lab: Spatial data visualization (3/26)

Today, we are using the `nc_health_2` dataset, which contains county-level data 
from the Robert Wood Johnson Foundation and contains the following variables:
- `name`: County name
- `uninsured`: Percentage of adults who are uninsured
- `obesity`: Percentage of adults who are obese
- `hs`: Percentage of adults who have graduated high school
- `mhhi`: Median household income in thousands
- `rural`: Rurality of the county, measured by the percentage of residents who
live in rural areas as defined by the Census Bureau.

# Activities

Our goal is to construct a regression model that aims to predict obesity rate
based on high school graduation rate, median household income, and rurality.

For all spatial models, use a row-standardized binary weight matrix (option "W"
in the `spdep` package code).

1. Create a linear regression model (STA 210 style) using these predictors as
main effects. What do you notice?
2. Is there evidence of spatial dependence in your regression model? Formally
evaluate this hypothesis.
3. Think about whether a spatial error model or spatial lag model might be
most appropriate (without performing any data analysis; also, ignore SARMA 
models for now). Why do you make this choice?
4. Use a Lagrange multiplier test (and perhaps robust versions) to evaluate which
model should be fit.
5. Regardless of your answers to (3) and (4), fit a spatial error regression
model on these data. How do your regression coefficients compare to your model
in (1)?
6. Regardless of your answers to (3) and (4), fit a spatial lag model on these 
data. What do you notice? Evaluate the direct, indirect, and total effects.
