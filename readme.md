# Seafloor photo mapping

Jupyter notebook to combining a timelapse photos and gps track of the seafloor. 

Load gps track and series of photos, tie the two together based on the time recorded by gps and photos and save as a kml file. 

You can also apply a time correction in case the time on the gps device or camera was incorrect.

This notebook was developed to combine gopro timelapse photos of the seafloor of a hydrothermally active area at the coast of Guadeloupe with a gps track from a device that was towed along above water.


# Prerequisites

Python 3.x and the following Python modules:
numpy, matplotlib, geopandas, gpxpy, exifread, natsort, pytz, simplekml, rasterio

The most convenient way to install these modules and run the notebook is probably to use the Anaconda Python distribution (https://www.anaconda.com/distribution/):

```shell
conda install numpy matplotlib geopandas gpxpy exifread natsort pytz simplekml rasterio
```

or otherwise the packages can be installed using pip

```shell
pip install numpy matplotlib geopandas gpxpy exifread natsort pytz simplekml rasterio
```


# Usage

* Open the notebook with jupyter lab or notebook (https://jupyter.org/). 
* Adjust the filenames of the gps track, directory containing the photos, and the bathymetry file in the box `Filenames and parameters`
* Adjust other parameters like the photo angle, a reference photo and gps point (to correct time offsets between the two), UTM coordinate system (for calculaitng distances and direction between pts) and output file names
* Run the notebook
* And inspect the saved .kml and .kmz files in google earth. The output is saved as an overlay, where photos are draped on the surface, and as a series of pins, where clicking on each pin will open a photo
* In addition the notebook saves two .csv files in the directory output, one containing the photos for each gps point and a second file with the location for each photo.


# Author

Elco Luijendijk


# License

This project is licensed under the GNU lesser general public license (LGPL v3). See [LICENSE.txt](LICENSE.txt) for details.



 
