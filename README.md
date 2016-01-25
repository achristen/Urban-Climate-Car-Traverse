# Urban Climate Car Traverse System 

## Description

A labview-based software to run UBC's truck-mounted system that measures temperature and carbon dioxide as the truck traverses a city along with GPS information. This system is used in <a href="http://ibis.geog.ubc.ca/courses/geob401/">UBC's GEOB 401 "Urban Meteorology"</a> course.

## Content

### Directory "Source"

The subdirectory "Source" contains all LabView VIs to build and run the application.

#### traverse.vi

This is the top-level user interface. It displays GPS data, measured air temperature and measured CO2 data traces. It allows users to insert marker points and displays the system status. 

#### welcome.vi

This is the welcome screen the uses sees when opening the application. The user can choose the COM-ports for GPS and data logger signals.

#### new_File.vi

This sub-vi is creating a datafile with name based on start time and date.

#### teaching_extract_serial.vi

This sub-vi is used to read the serial data in form of a text-string from the COM-ports (GPS and Logger).

#### GPSmap76.vi

This sub-vi parses one line of a string from the Garmin GPS 76 module into its components (Time, Longitude, Latitude, Altitude, Horizontal Position Error, Status, Speed, Direction)

#### uv_md.vi

This sub-vi translates northing and easting from the GPS into direction and speed. Used during parsing in GPSmap76.vi to display heading and speed on the top level "traverse.vi".
