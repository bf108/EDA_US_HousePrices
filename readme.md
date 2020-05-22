# HousePrice Data Exploration

## Dataset

The data consists of information regarding 1460 properties sold in Ames Iowa
with 79 explanatory variables describing (almost) every aspect of residence.

The dataset can be found on:
[Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)

Feature documentation available:
[Ames Housing Data](http://web.stanford.edu/class/stats191/data/amesdoc.txt).


## Summary of Findings

During the exploration of the data I was able to deduce that Sales Price was
not normally distributed due to a number of expensive properties skewing
the data to the right. This was resolved by applying a logarithmic transform
to the SalePrice data. Once transformed, the SalePrice then closely followed a
normal distribution.

I found strong a positive correlation between logarithmic SalePrice and
GrdLivArea (available living area in the property). There were similar, yet
weaker, correlations between total number of rooms, bathrooms, and car spaces.
These are all expected results because they indicate that as house size
increases the value also increases. Larger homes demand a higher sales price.

A note on bathrooms. The original dataset had four different features for
bathrooms which consisted of full and half bathrooms and basement and above
grade bathrooms. These were amalgamated into one feature of Total Bathrooms.

In terms of categorical variables, Overall Quality (ordinal) had the strongest
correlation with logarithmic SalePrice. Once again this is intuitive, as
it is common to pay proportionally more for higher quality.

There were also obvious correlations between Building Material and Neighbourhood.
The more expensive homes tended to be build from Vinyl, mid range homes were
more often wood, whilst low end homes tended to have a higher proportion of
metal, asbestos and asphalt. Some data tidying was done to group these
materials into five classes.

The dataset consisted of 25 Neighbourhoods. The price of homes did vary
considerably in some neighbourhoods, but there was certainly a correlation
between neighbourhood and house price. Some neighbourhoods only contained
properties at the lower end of the price scale, such as Meadow Village, whilst
others contained a substantial percentage in the upper price band, such as
Northridge.

## Key Insights for Presentation

For the presentation, I will focus on the correlation between between SalePrice
and Overall Liveable Grid Area (Sq Feet). I will show the impact of categorical
features by overlaying them in multivariate plots.
