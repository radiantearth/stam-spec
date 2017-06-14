## About

These fields are the core fields that all remotely sensed imagery should make available about itself. All fields are required, 
unless marked as optional. For the abstract all fields should work as non-nested properties, since some instantiations may
only allow flat properties. 

## Specification Description 

| element           | type   | name                    | description                                                                                 | 
|-------------------|--------|-------------------------|---------------------------------------------------------------------------------------------| 
| uuid              | string | RFC 4122                | unique UUID v4                                                                              | 
| scene_id          | string | Scene id                | scene id from provider                                                                      |
| scene_title       | string | Title                   | scene title from provider of generated                                                      |                                           |
| projection        | string | Projection              | CRS of the datasource in full WKT format                                                    | 
| bbox              | array  | Bounding Box            | Pair of min and max coordinates in CRS units, (min_x, min_y, max_x, max_y)                  | 
| footprint         | string | Datasource footprint    | WKT format, describing the actual footprint of the imagery                                  | 
| gsd               | object | Ground Spatial Distance | Average ground spatial distance (resolution) of the datasource imagery, expressed in meters | 
| file_size         | number | File Size               | File size on disk in bytes                                                                  | 
| acquisition_start | string | Acquisition Date Start  | First date of acquisition in UTC (Combined date and time representation)                    | 
| acquisition_end   | string | Acquisition Date End    | Last date of acquisition in UTC (Combined date and time representation) (optional)          | 
| sensor            | string | Sensor                  | sensor information and sensor class e.g. List of possible platform sources limited to satellite, aircraft, UAV, balloon, kite, helikite, pole, and rover                                                         | 
| provider          | object | Imagery Provider        | Provider/owner of the data                                                                  |
| license           | object | Data license            | Data license name, desc, and url                                                            | 
| properties        | object | Properties              | Additional properties about the image (optional)                                            | 
