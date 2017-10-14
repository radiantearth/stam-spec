## Intro

This document specifies the JSON instantiation of the [imagery metadata abstract spec](../abstract-spec.md). 

## Specification Description 

| element           | type   | name                    | description                                                                                 | 
|-------------------|--------|-------------------------|---------------------------------------------------------------------------------------------| 
| uuid              | string | File                    | unique URI to file                                                                          | 
| projection        | string | Projection              | CRS of the datasource in full WKT format                                                    | 
| bbox              | array  | Bounding Box            | Pair of min and max coordinates in CRS units, (min_x, min_y, max_x, max_y)                  | 
| footprint         | string | Datasource footprint    | WKT format, describing the actual footprint of the imagery                                  | 
| gsd               | number | Ground Sample Distance | Average ground sample distance (resolution) of the datasource imagery, expressed in meters | 
| acquisition_start | string | Acquisition Date Start  | First date of acquisition in UTC (Combined date and time representation)                    | 
| acquisition_end   | string | Acquisition Date End    | Last date of acquisition in UTC (Combined date and time representation) (optional)          | 
| title             | string | Title                   | Human friendly title of the image                                                           | 
| platform          | string | Type of imagery         | List of possible platform sources limited to satellite, aircraft, UAV, balloon, kite, helikite, pole, and rover       | 
| provider          | string | Imagery Provider        | Provider/owner of the OIN bucket                                                            | 
| contact           | string | Contact                 | Name and email address of the data provider                                                 | 
| license           | string (limited list) | Data license            | Data license name, must be one of the accepted licenses (TBD) 
| version        | semantic versioning number | Spec Version              | The version of the imagery metadata fields, for testing/validation  | 
| properties        | object | Properties              | Additional properties about the image (optional)                                            | 
