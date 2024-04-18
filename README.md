# Group-3-Project-3
Group 3 Project 3 - Huang, Potter, Bhardwaj, Robertson

Link to the interactive dashboard:

https://kaihuang17.github.io/Project3-Group3/

!['20 year GDP'](Clean_Data_Visualisation/choropleth_map.png)

## Analysis

The intention of this project was to take CO2 emissions data and measure it against certain economic markers to generate a snapshot of a countries environmental impact vs economic efficiency for first two decades at the turn of the millenium. 

Data was accessed from Gapminder, a publicly available database of information containing historic and projected social, economic & environmental datasets. A sample of 15 countries were selected to create a global summary. Groups of five countries were selected to represent a selection from three distinct market classifications:

- Developed
  - Australia
  - USA
  - Sweden
  - Switzerland
  - Japan
  - 
- Underdeveloped
  - Brazil
  - Egypt
  - Greece
  - India
  - South Africa
  
- Developing
  - Bangladesh
  - Afghanistan
  - Cambodia
  - Senegal
  - Ethiopia

We analysed 2 emissions data metrics:

  #### Annual CO2 Emissions Total (Millions of Tonnes)
![20_year_total_Emissions](Clean_Data_Visualisation/Cleaned_Data/Tonnes_Per_Millions.png)

  #### Annual CO2 Emissions Per Capita (Tonnes)
![20_year_Emissions_per_Capita](Clean_Data_Visualisation/Analysis_Visuals/Carbon_Emissions_per_Capita.png)

And 3 economic markers:

  #### Population
  !['20 year Population'](Clean_Data_Visualisation/Cleaned_Data/Population_table.png )

  #### Average Daily income ($USD)
  !['20 year Average Daily Income'](Clean_Data_Visualisation/Cleaned_Data/Average_Income.png)

  #### Country GDP (Millions of $USD)
  !['20 year GDP'](Clean_Data_Visualisation/Cleaned_Data/Average_Income.png)

Data was accessed and cleaned from the source to be stored in a PostgreSQL database. Attention had to be put into the GDP and Population figures as they were not represented in integer format. Ultimately the resulting table was created for each metric, as well as additional identifying tables:
- Countries
- Country IDs
- Classifications
- Coutnry Class

![ERD](sqlDatabase/country_emissions_erd.png)

## Interesting Trends

From an an analysis of the data two interesting trends have emerged.

The first compares carbon emissions per capita. From the visualisation below, we can clearly see a significantly larger emissions output from nations with higher GDP. Second to this a majority of countries considered developed have trended down in their CO2 emissions output over the two decades measured. This could be attributed to a number of causes including but not limited to:
- Investment in green energy manufacturing
- Reduction in waste consumption
- A shift in attitudes favouring environmental preservation
- Export of heavy emissions manufacturing to less developed nations.

![Carbon emissions per GDP](Clean_Data_Visualisation/Analysis_Visuals/Carbon_Emissions_per_GDP_Visual_and_table.png)

In direct contrast to this CO2 emissions have seen a rise in developing and underdeveloped nations for almost the exact opposite reason. Significant social inequalities and growing populations bring about a unique set of economic circumstances where the production of mass quantities of product or manufacturing of goods and services is required to sustain the population. Generally this relies on cheap available technologies and processes which do not favour sustainability or environmentally friendly practices. 

The above points go match the second major trend revealed in the data. Countries considered more developed nations (i.e higher GDP) output less emissions per GDP and are overwhelmingly trending down as the two decades progressed. As mentioned above to sustain growing populations, countries with lower GDP and increasing populations generally rely on cheaper less environmentally friendly manufacturing and production processes contributing to increased and elevated CO2 emissions.

![Carbon Emissions Per Capita](Clean_Data_Visualisation/Analysis_Visuals/Carbon_Emissions_per_Capita_Visual_and_table.png)

## Ethical Considerations

When collecting data one must consider a variety of ethical implications at all stages of the analytical process including collection, processing, analysis and presentation of data. Some of the key points to take into consideration include:

- Privacy concerns
- Inherent bias or prejudice
- Transparency
- Data security
- Consideration of outcomes
  
In this project we explored free, publicly available country data for emissions, gdp, population and economic strength. These types of information are widely considered unbias and pose little ethical risk as they are an objective point of information compiled for a variety of domestic and international reporting.

The purpose for colecting, analysing and visualising the information was to investigate countries classified as developed, developing or underveloped and generate a preview of their CO2 emissions against economic markers. This preview would give us insight into the economic efficiency vs environmental impact and the carbon intensity of each country relative to GDP of each classification. 

The risk you run with presenting data in this manner is that that out of context conclusions could be drawn. A countries relationship between it's economic output and emissions levels are open to so many other contributing factors that it would be impossible to draw any real meanngful conclusion to infulence decision making. One reliable metric which could be gathered from this data are countries which would benefit from foreign investment into greener manufacturing and production projects or countries. This could improve domestic econimic measures and assist in reducing the growth in CO2 emissions moving forward.

## References

- *How To Create a Top Navigation Bar*, (1999 - 2024) W3Schools, https://www.w3schools.com/howto/howto_js_topnav.asp
- *MSCI Market Classification: Assessing and categorizing equity markets according to common characteristics*, MSCI, https://www.msci.com/our-solutions/indexes/market-classification
- *Global Carbon Budget (2023); Population based on various sources (2023) – with major processing by Our World in Data. “Per capita CO₂ emissions – GCB” [dataset]*. Global Carbon Project, “Global Carbon Budget”; Various sources, “Population” [original data].  https://ourworldindata.org/grapher/co-emissions-per-capita
- *CO2 emissions per capita Consumption based, tonnes per capita* & *GDP per capita (Price and inflations adjusted, in PPP$2017)* & *Population* & *Consumption CO2 emissions, million tonnes* & *Average daily income, $/person/day, inflation - & price adjusted*, https://www.gapminder.org/data/
- *Natural Earth   &raquo; 1:10m Cultural Vectors - Free vector and raster map data at 1:10m, 1:50m, and 1:110m scales*, 2009 - 2024. Natural Earth https://www.naturalearthdata.com/downloads/10m-cultural-vectors/
- Gillies S *shapely.MultiPolygon &#8212; Shapely 2.1.0.dev0 documentation*, Shapely https://shapely.readthedocs.io/en/latest/reference/shapely.MultiPolygon.html
- GeoPandas developers *User Guide*, GeoPandas 2013–2022 https://geopandas.org/en/stable/docs/user_guide.html
- *Human Development Index (HDI),© 2024* United Nations Development Programme - https://hdr.undp.org/data-center/human-development-index#/indicies/HDI
- *Top 25 Developed and Developing Countries, December 17, 2023* - https://www.investopedia.com/updates/top-developing-countries/
- *Ethiopia Looks to Tap Its Massive Renewable Energy Potential, Feb 18, 2024* - https://oilprice.com/Alternative-Energy/Renewable-Energy/Ethiopia-Looks-to-Tap-Its-Massive-Renewable-Energy-Potential