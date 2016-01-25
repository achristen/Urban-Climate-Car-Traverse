# Urban Climate Car Traverse System 

## Description

A labview-based software to run UBC's truck-mounted system that measures temperature and carbon dioxide as the truck traverses a city along with GPS information. This system is used in <a href="http://ibis.geog.ubc.ca/courses/geob401/">UBC's GEOB 401 "Urban Meteorology"</a> course.

![](Image-System-Photo.jpg)

## Content

### Directory "Source"

The subdirectory "Source" contains all LabView VIs to build and run the application.

#### traverse.vi

This is the top-level user interface. It displays GPS data, measured air temperature and measured CO2 data traces. It allows users to insert marker points and displays the system status. 

![](Image-Screen.gif)

#### welcome.vi

This is the welcome screen the uses sees when opening the application. The user can choose the COM-ports for GPS and data logger signals.

#### new_file.vi

This sub-vi is creating a datafile with name based on start time and date.

#### teaching_serial.vi and teaching_logger.vi

This sub-vi is used to read the serial data in form of a text-string from the COM-ports (GPS and Logger).

#### teaching_extract_serial.vi

This sub-vi is used to parse the logger data from the Campbell Scientific 21X logger into fields. 
<<<<<<< Updated upstream

#### writespreadsheetstring.vi

this is a generic vi that appends a spreadsheet line (string) to an existing file. 

#### GPSmap76.vi

This sub-vi parses one line of a string from the Garmin GPS 76 module into its components (Time, Longitude, Latitude, Altitude, Horizontal Position Error, Status, Speed, Direction). <a href="images/GPS_Signal.png">Here is a description of the raw GPS signal string</a> from the Garmin GPS 76 model.

#### writespreadsheetstring.vi

this is a generic vi that appends a spreadsheet line (string) to an existing file. 

#### GPSmap76.vi

This sub-vi parses one line of a string from the Garmin GPS 76 module into its components (Time, Longitude, Latitude, Altitude, Horizontal Position Error, Status, Speed, Direction). <a href="images/GPS_Signal.png">Here is a description of the raw GPS signal string</a> from the Garmin GPS 76 model.

#### uv_md.vi

This sub-vi translates northing and easting from the GPS into direction and speed. Used during parsing in GPSmap76.vi to display heading and speed on the top level "traverse.vi".

### Directory "Logger_Program"

This directory contains the logger program for the Campbell Scientific 21X data logger.

### Directory "Documentation"

This directory contains the operating instructions (for students) of the entire system in form of a word file.
