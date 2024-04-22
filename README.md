The 'estimating-digital-trade.ipynb' includes the code needed to generate the estimates for trade in digital products described in "Estimating Digital Product Trade through Corporate Revenue Data" by Viktor Stojkoski, Philipp Koch, Eva Coll, and César A. Hidalgo.

The code was initially run in Python 3.9.13 and requires the following libraries:

* pandas version: 1.4.4
* numpy version: 1.21.5
* xgboost version: 1.7.6
* statsmodels version: 0.14.0
* scikit-learn version: 1.0.2
* scipy version: 1.9.1
* matplotlib version: 3.5.2
* seaborn version: 0.11.2


The code requires the following data files in order to be executed properly:

* data.csv

This file has the data required for the machine learning model. This file has sensitive information, and therefore we do not provide it. The data file has the following columns:

'firm' - name of the parent firm (ordered alphabetically)
'year' - the year of the observation
'category' - the category of the firm
'iso_o' - the origin country of the headquarters of the firm-category pair
'iso_d' - the consumption destination country 
'contig' - Dummy variable for the contiguity between the country of origin of the parent company and the country where the product is consumed
'comlang_off' - Dummy variable for common official language between the country of origin of the headquarters and the country where the product is consumed
'comlang_ethno' - Dummy variable for common unofficial language (spoken by at least 9% of the population) between the country of origin of the headquarters and the country where the product is consumed
'colony' - Dummy variable describing whether the country of origin of the headquarters and the country where the product is consumed were ever in a colonial relationship
'comcol' - Dummy variable describing whether the country of origin of the headquarters and the country where the product is consumed shared a common colonizer post 1945
'curcol' - Dummy variable describing whether the country of origin of the headquarters and the country where the product is consumed are currently in a colonial relationship
'col45' - Dummy variable describing whether the country of origin of the headquarters and the country where the product is consumed were in colonial relationship post 1945
'smctry' - Dummy variable describing whether the country of origin of the headquarters and the country where the product is consumed were ever part of the same country
'dist' - Geographic distance (in km) between the most populated cities of the country of origin of the headquarters and the country where the product is consumed
'iso_o_gdp' - GDP in current USD of the country of origin of the headquarters 
'iso_d_gdp' - GDP in current USD of the country where the product is consumed
'trade_value' - Consumption of iso_d in the category of firm (in USD)
'total_export_value' - Total revenues of a parent company in a digital sector (in USD)
'total_category_value' - Total world revenues of the digital sector (in USD)
'iso_o_fixed_broadband' - Fixed broadband connections as a share of population for the country of origin of the headquarters
'iso_d_fixed_broadband' - Fixed broadband connections as a share of population for the country where the product is consumed
'iso_o_mobile_broadband' - Mobile broadband connections as a share of population for the country of origin of the headquarters
'iso_d_mobile_broadband' - Mobile broadband connections as a share of population for the country where the product is consumed
'iso_o_ict' - ICT exports of the country of origin of the headquarters (not used in the analysis due to lack of data)
'iso_d_ict' - ICT imports of the country where the product is consumed (not used in the analysis due to lack of data)
'iso_o_internet' - Internet users as a share of population for the country of origin of the headquarters
'iso_d_internet' - Internet users as a share of population for the country where the product is consumed
'iso_o_loc' - World region of the country of origin of the headquarters (as defined by United Nations geoscheme)
'iso_d_loc' - World region of the country where the product is consumed (as defined by United Nations geoscheme)

* firms_revenue_subsidiary.csv

This file include information on the total revenues of each firm and subsidiary. We provide this document but mute the column 'value' as it consists of data gathered from other sources. The data file has the following columns:

'firm' - name of the firm
'iso_o' - country location of the firm
'year' - the year of the observation
'category' - the category of the firm
'value', - the total revenues of the firm in the category
'parent' - name of the parent company
'is_subsidiary' - yes if it is a subsidiary, no otherwise

* firm-revenue-share.xlsx. This is an excel document containing the regional shares of the parent companies and the countries included in each region. We provide this document.

* dist_data.xlsx. This is an excel document containing the geographical distance between countries. We provide this document.


 
