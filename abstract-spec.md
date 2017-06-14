## About

These fields are the core fields that all remotely sensed imagery should make available about itself. All fields are required, 
unless marked as optional. For the abstract all fields should work as non-nested properties, since some instantiations may
only allow flat properties. 

*Type info* in the table below is not meant to be prescriptive, as different instantiations may not have the full range of options.

## Core Specification Description 

| element           | type info   | name                    | description                                                                                 | 
|-------------------|--------|-------------------------|---------------------------------------------------------------------------------------------| 
| uuid              | string of 16 octets | RFC 4122                | unique UUID v4                                                                              | 
| scene_id          | string, format defined by imagery provider | Scene id                | scene id from provider                                                                      |
| scene_title       | optional string | Title                   | scene title from provider of image. If not present then fall back to scene_id                                                      |                                           |
| projection        | projection information | Projection              | CRS of the datasource in full WKT format. Should be a projection in the EPSG database, so all software can read it.                                                   | 
| bbox              | pair of coordinates  | Bounding Box            | Pair of min and max coordinates in CRS units, (min_x, min_y, max_x, max_y)                  | 
| footprint         | A geometry | Datasource footprint    | Describing the actual footprint of the imagery                                  | 
| gsd               | number | Ground Sample Distance | Average ground sample distance (resolution) of the datasource imagery, expressed in meters. Is the distance between the centers of pixels on the ground. | 
| acquisition_start | date and time | Acquisition Date Start  | First acquisition in UTC (Combined date and time representation)                    | 
| acquisition_end   | date and time | Acquisition Date End    | Last acquisition in UTC (Combined date and time representation) (optional)          | 
| sensor            | string (limited list) | Sensor                  | sensor information and sensor class e.g. List of possible platform sources limited to satellite, aircraft, UAV, balloon, kite, helikite, pole, and rover                                                         | 
| provider          | string | Imagery Provider        | Provider/owner of the data                                                                  |
| license           | string (limited list) | Data license            | Data license name, must be one of the accepted licenses (TBD)                                                            | 
| properties        | extension | Properties              | Additional properties about the image (optional).                                            | 

