Texas schools geocoding project
===============================

This is a class project by:

    Univeristy of Texas at Austin
    School of Journalism
    Data Visualization
    Spring 2015
    Instructor: Christian McDonald

We will create a geocoded list of every school in Texas that can be merged with data files from the Texas Education Agency for easy mapping.

As of this writing (3/14/2015) we have not yet started the project. I'll post here when we are done ... should be by the end of the month.

The students will be following [this guide](https://docs.google.com/document/d/16_reBIxOvRJvfiuTN5bdGpFFq0JH39pmE5kCOv8xaCM/edit?usp=sharing) for the work.

## Files list

* `schoolsraw.csv` is the file downloaded on 3/14/2015 from the [Texas Education Agency AskTED](http://mansfield.tea.state.tx.us/tea.askted.web/Forms/Home.aspx). It is called: School and District File with Site Address.
* `csv_splitter` is a python script used to split the raw file into pieces so each student in the class could have a batch of files to geocode.
* the `output` folder contains those raw files -- 18 of the them with about 520 records each.

## Geocoding

We are using [Texas A&M Geoservices](http://geoservices.tamu.edu/) to batch geocode the files. It is a wonderful service that not only provides latitudes and longitudes for addresses, but gives a quality index of how the points were arrived at. This is essential to be sure that an address was found at street point instead of a city or zip code centroid. Their service is free for up to 2500 addresses a month. Or something like that. Check with them.

[Geo-stuff provided by Texas A&M University GeoServices](http://geoservices.tamu.edu/)

## The plan

Students will geocode their batch, clean up any zip/city level results and submit them for class credit. I will then combine all the files and post them to this repo.

## class_files

Files back from students with the manual fixex before I process them into the single file. Some notes:

* `output_01_la_geocoding.xlsx` output from geociding service, but maybe not updated
* `output_11_am_geocoding.xlsx` couldn't find 17 of list, they're highlighted
* `output_14_et_geocoding.xlsx` yellow highlights couldn't be found. Record 28 fix "KING"
* `output_07_dg_geocoding.xls` Some of them I skipped, because they could not be found on the map. One school in particular does not open until the fall.
* `output_10_wm_geocoding.xlsx` The schools I left without updating had problems either in that they were closed, the address was incorrect, or the address belonged to a different business.
* `output_16_bw_geocoding.xlsx` Addresses could not be found for lines 256, 473, 487, 488, and 492.

