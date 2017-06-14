## About

These fields are the core fields that all remotely sensed imagery should make available about itself. All fields are required, 
unless marked as optional. For the abstract all fields should work as non-nested properties, since some instantiations may
only allow flat properties. 

*Type info* in the table below is not meant to be prescriptive, as different instantiations may not have the full range of options.

## Core Specification Description 

| element           | type info   | name                    | description                                                                                 | 
|-------------------|--------|-------------------------|---------------------------------------------------------------------------------------------| 
| uuid              | Universal Unique ID | ID                | unique ID, potentially link to file                                                                            | 
| title       | optional string | Title                   | scene title from provider of image. Can be the ID of the image provider                                                     |                                           |
| projection        | projection information | Projection              | CRS of the datasource in full WKT format. Should be a projection in the EPSG database, so all software can read it.                                                   | 
| bbox              | pair of coordinates  | Bounding Box            | Pair of min and max coordinates in CRS units, (min_x, min_y, max_x, max_y)                  | 
| footprint         | A geometry | Datasource footprint    | Describing the actual footprint of the imagery                                  | 
| gsd               | number | Ground Sample Distance | Average ground sample distance (resolution) of the datasource imagery, expressed in meters. Is the distance between the centers of pixels on the ground. | 
| acquisition_start | date and time | Acquisition Date Start  | First acquisition in UTC (Combined date and time representation)                    | 
| acquisition_end   | date and time | Acquisition Date End    | Last acquisition in UTC (Combined date and time representation) (optional)          | 
| platform            | string (limited list) | Sensor                  | sensor information and sensor class e.g. List of possible platform sources limited to satellite, aircraft, UAV, balloon, kite, helikite, pole, and rover                                                         | 
| provider          | string | Imagery Provider        | Provider/owner of the data                                                                  |
| license           | string (limited list) | Data license            | Data license name, must be one of the accepted licenses (TBD)                                                            | 
| version        | semantic versioning number | Spec Version              | The version of the imagery metadata fields, for testing/validation  | 


