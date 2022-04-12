# CO2-Emissions-
Sequential Color Schemes to visualize annual greenhouse gas emisssions from facilities across Canada.
Spatial files to outline detailed boundaries of specific regions of interest. Outline points, lines in a very detailed and specific way.

DATA GATHERING:
I gathered the dataset by going under Google Canda, www.google.ca. The website that I used was https://open.canada.ca/en/open-data. I was able to filter out a csv file that was particularly called Greenhouse Gas Reporting Program Facility Greenhouse Gas Data (GHGRP). This dataset records data anually from facilities across Canada. 
I had a London CO2 Emissions by Bourough and then I was able to grab the London Bourough Dataset from the Tableau website via sample dataset. The filename is called CO2 Emissions by London Borough. 
Then, I would INNER JOIN the dataset from the London Borough Dataset and the CO2 Emissions by London Borough .shp file by GSS Code 

DATA VISUALIZATION PREP: 
First, I've created a calculated Field called Postal Code 3. This calculated field was made so that it would only include the first three characters of the Postal Code Column of the dataset. Therefore, I used the LEFT({Postal Code}, 3). Then I changed the type of from a String type to Postal Code, so that Tableau recognizes the column as Postal Code. 
I used Postal Code 3 to ToolTip so that Tableau was able to recognize the data as a Postal Code data set.
Then, I dragged the Longitude field to Columns and the Latitude Field to Rows and changed the marks to Map. 
Then, I would drag the Total Emissions measure into the color field to distinguish the data into Tableau,and changed the emissions color to Orange. The darker the Orange color, showed more Co2 emissions while lighter Orange colors showed less Co2 emissions. 
Then, I wanted to create an animation to show the trend over time on a annual basis. Therefore, I grabbed the Year column and changed the data type to Date. Furthermore, I would grab the Year column and drag it over to Pages. 

The Geometry field is treated as a geophraphical field and a measure as it is aggregated by the COLLECT Function. 
Then, I added the Name field under Details and the Hecteres field into color. 
