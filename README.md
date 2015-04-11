Texas schools geocoding project
===============================

This is a class project by:

    Univeristy of Texas at Austin
    School of Journalism
    Data Visualization
    Spring 2015
    Instructor: Christian McDonald

STATUS: Testing and Cleanup. All addresses have been geocoded ... now we're spot-checking them on maps.

We are creating a geocoded list of every school in Texas that can be merged with data files from the Texas Education Agency for easy mapping. The files are available for free use. If you do use, them, I'd love to know at christian.mcdonald@utexas.edu.

The work was completed in April 2015.

The students followed [this guide](https://docs.google.com/document/d/16_reBIxOvRJvfiuTN5bdGpFFq0JH39pmE5kCOv8xaCM/edit?usp=sharing) for the work.

## Files list

* `texas-schools-geocoded.csv` is a csv file of geocoded schools.
* `texas-schools-geocoded.xlsx` is the same file as Excel. (I might kill this.)
* `schoolsraw.csv` is the origial file the project started from. It is called School and District File with Site Address, and was downloaded from the [Texas Education Agency AskTED](http://mansfield.tea.state.tx.us/tea.askted.web/Forms/Home.aspx) on 3/14/2015.
* `csv_splitter` is a python script used to split the raw file into pieces so each student in the class could have a batch of files to geocode. Someone might find that useful some day.

## GeocodeQualityType

If a geocoding result was not AddressRangeInterpolation or ExactParcelCentroidPoint, the location was manually checked, and the GeocodeQualityType field changed to Manual. Other fields from the geocoding process have been removed for clarity.

## How we geocoded

We used [Texas A&M Geoservices](http://geoservices.tamu.edu/) to batch geocode the files. It is a wonderful service that not only provides latitudes and longitudes for addresses, but gives a quality index of how the points were found. This is essential to be sure that an address was found at street point instead of a city or zip code centroid. Their service is free for up to 2500 addresses a month, or something like that. Check with them ... they are good people.

[Geo-stuff provided by Texas A&M University GeoServices](http://geoservices.tamu.edu/)

## Caveats

There are some known issues with the file, which are outlined here. They shouldn't keep them from use in most cases.

* Latitudes and Longitudes can only be as good as the address they start from. This will be particularly true for alternative schools, which can be ambiguous.
* Manually-found locations are based off Google Maps, and subject to errors there, not that I know of any. In many cases, the manual locations were verified through Street View photos.
* In some cases we just couldn't find the school. Those have blank Lat/Longs.

## Corrections

If you have any corrections to offer, send them to christian.mcdonald@utexas.edu.

## Contributors

The following students from the University of Texas at Austin School of Journalism, Spring 2015 Data Visualization course contributed to this project:

* LUQMAN ADENIYI
* JOSEPH BAUCUM
* NICOLE COBLER
* TAYLOR ELLIS
* LAUREN FLORENCE
* TRACY FRYDBERG
* DANIEL GOODWIN
* SEBASTIAN HERRERA
* GABRIEL MACIAS
* WESLEY MARTIN
* RENEE MORENO
* ALEXIS SCHRUBBE
* PHILLIP TRACY
* BRYAN WINTER
* MANZHI WU

Also contributing:

* CHRISTIAN MCDONALD
* ANDRE MONTEIRO
* EDWARD TIMMS

Many thanks to all who helped. Enjoy.
