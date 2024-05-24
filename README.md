# Nature Dots Sample Project

A brief description of how this project made and how to use

Install the required packages using this command : pip install earthengine-api geopandas matplotlib

1 . Initialize Earth Engine: Ensure you have authenticated with GEE using ee.Initialize().

2 . Load GeoJSON: Function to load GeoJSON file.


3 . Get Water Extent Time Series:
    a) Convert the GeoJSON to an Earth Engine geometry object.
    b) Use the JRC Global Surface Water dataset to filter images by date and select the  
      'water' band.
    c) Calculate the water area for each image by masking permanent water (value 2) and    
    summing the pixel areas within the region of interest.

4 . Plot Time Series: 
    Use Matplotlib to plot the time series and save the plot as an image file.

Ensure to replace 'manasbol.geojson' with the actual path to your GeoJSON file. 
Also, make sure to handle authentication for Earth Engine appropriately if running this script for the first time.
In place of 'ee-naturedots-proj' used for initialization above, use a 'project name' that was registered in your earth engine account that you used for authentication.

