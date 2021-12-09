
#### README
-----------------
# Spec-Spex

by Annelise Holverstott

DSI 927
<br><br>

-----------------
## Problem Statement


This project identifies characteristics of a house or the lot itself that building professionals should emphasize in order to increase the sale price of new homes.

<br><br>
-----------------
## Data Dictionary


Please refer to this [data dictionary](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt) from the original study. 

<br><br>
-----------------
## Analysis


The linear regression model that includes features of the house outperforms the baseline model based on features of the lot alone. The RidgeCV model reduced the variance by a very small amount, but its RMSE scores are slightly higher than either the Improved OLS or the LASSO CV model. All of the models have similar RMSE and R$^2$ scores. All are improvements over the baseline model. 

Because some degree of transparency is required for this model, I recommend sticking with the improved OLS model. Building tradespeople need to be able to interpret the coefficients easily to understand what kind of decisions can move the needle on sale price. 

|Model|Metric|Dataset|Value|
|---|---|---|---|
|Baseline OLS|RMSE|Train|\$48,276.45|
|Baseline OLS|RMSE|Test|\$43,997.25|
|Baseline OLS|R$^2$|Train|0.645|
|Baseline OLS|R$^2$|Test|0.641|
|Improved OLS|RMSE|Train|\$29698.51|
|Improved OLS|RMSE|Test|\$26858.26|
|Improved OLS|R$^2$|Train|0.866|
|Improved OLS|R$^2$|Test|0.866|
|LASSO CV|RMSE|Train|\$29698.55|
|LASSO CV|RMSE|Test|\$26858.67|
|LASSO CV|R$^2$|Train|0.866|
|LASSO CV|R$^2$|Test|0.866|
|Ridge CV|RMSE|Train|\$29,845.06|
|Ridge CV|RMSE|Test|\$27,021.10|
|Ridge CV|R$^2$|Train|.864|
|Ridge CV|R$^2$|Test|.864|

<br><br>
-----------------
## Conclusions
-----------------

Based on my exploration of the data, I have a few recommendations for building professionals looking to undertake spec projects.

- **Location** <br>
If you don't already have a plot of land, consider purchasing land in a low- or medium-density zone. High-density zoning is associated with lower prices. Some neighborhoods are also more desirable: Northridge Heights, Northridge, and Somerset tend to have higher home prices while Edwards, North Ames, and Sawyer have lower prices. 
- **Layout is less important than living area** <br>
Large lots *are* associated with more expensive homes, but much more important is the livable area of the house (expect to increase sale price by \$39.93/sf), the area of the garage (\$27.59/sf), the area of the deck or porch (\$22.76/sf), and the area of the basement (\$21.78/sf). Lot size, by contrast, we only expect to see an increase of \$.90/sf. <br>
Also, while number of bathrooms does increase the house price by about $6373 per bathroom, the model does not predict any particular layout will be higher priced than another. Rooms above and below grade, how many stories the house has, etc are all dwarfed by the importance of square footage. 
- **Materials Matter** <br>
In general, the overall quality of materials used is one of the very most important factors in sale price. For every unit a house moves up on the quality ranking scale, we expect to see a \$14,495 increase in sale price. Roofing materials in particular can drive a home price up or down -- consider composite shingles, wood shingles, or wood shakes. Masonry instead of siding also raises home price. The type of foundation can also have an impact -- if you can do poured concrete, I would expect it to increase the sale price around \$4,900. 
- **Always put in a fireplace** <br>
A fireplace is associated with a \$6363 increase in the sale price. There's no good reason not to build one in. 
