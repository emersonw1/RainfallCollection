<h1>Rainfall Collection and Household Water Usage</h1>
GitHub Repository: https://github.com/emersonw1/RainfallCollection<br>
Team members: Emerson Wachelka, Sam Gartrell

<h2>Summary and Objectives</h2>
<p>The purpose of the project is to assess Arizona households' potential for living off of rainwater captured by their roofs.</p> 

<p>How many households in Arizona would have been able to live solely off of rainfall over the past decade? The answer here is likely extremely low. However, precipitation varies across months, so perhaps there are certain times of the year when households would be able to meet their water requirements for that month.</p>

<h2>Datasets</h2>
Shapefile of building footprints in Arizona (Download Link) - The geojson file must be in your python environment folder.<br>
https://usbuildingdata.blob.core.windows.net/usbuildings-v2/Arizona.geojson.zip<br><br>
Raster of precipitation for each month in Arizona over the past decade<br>
https://climate.copernicus.eu/climate-reanalysis

## Python Packages
- jupyter
- matplotlib
- geopandas
- pandas
- numpy
- xarray
- rasterio

## Setting up
Clone this repository:
```
git clone https://github.com/emersonw1/RainfallCollection
cd RainfallCollection
```

Clone and set up the conda environment
```
conda env create -n rainfall --file environment.yml
conda activate rainfall
```

<h2>Planned Methods/Approach</h2>
<p>Firstly, we would need to define a threshold of area to separate houses from commercial buildings since we are looking at household water usage.</p>

<p>The next step would be to intersect the precipitation data with the house footprints so that each house could have an associated amount of annual precipitation that lands on top of it.</p>

<h2>Expected Outcomes</h2>
<p>We should be able to find out how many households in Arizona would be able to meet their water needs given that they capture all of the rainfall landing on their roof. We should also be able to tell, for the households that don't meet their needs, how close they are getting. For example: how many households are meeting 90% of their requirements, how many are meeting 80%, etc. We could also map the locations of houses meeting their water supply needs vs those that are not, as well as look at how this changes month-to-month.</p>

<h2>Relavent Information</h2>
Arizona residents use more water than those of most other states at 146 gallons per day in 2015 compared to the US average of 83 (University of Arizona). This translates to 10,950 gallons per month for the average household of 2.5 (Duffin).

<h2>References</h2>
Duffin, E., &amp; 12, D. (2022, December 12). Average size of households in the U.S. 2022. Statista. Retrieved February 16, 2023, from https://www.statista.com/statistics/183648/average-size-of-households-in-the-us/#:~:text=The%20average%20American%20household%20consisted%20of%202.5%20people%20in%202022.<br><br>

University of Arizona. (n.d.). Residential water use. MAP AZ Dashboard. Retrieved February 16, 2023, from https://mapazdashboard.arizona.edu/infrastructure/residential-water-use<br>

The building footprint shapefile comes from this page:<br>
https://github.com/microsoft/USBuildingFootprints
