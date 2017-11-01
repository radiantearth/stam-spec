## About

These fields are the core fields that all remotely sensed imagery should make available about itself. All fields are required, 
unless marked as optional. For the abstract all fields should work as non-nested properties, since some instantiations may
only allow flat properties. 

*Type info* in the table below is not meant to be prescriptive, as different instantiations may not have the full range of options.

## Core Specification Description 

| element              | type info              | name                            | description                                                                                 | 
|-----------------------|------------------------|--------------------------------|---------------------------------------------------------------------------------------------| 
| id                        | string                   | Provider ID                   | Provider ID for that item                                                                            | 
| geometry            | geometry               | Bounding Box + Footprint | in lat/long (4326)
| start_date           | date and time      | Date Start                     | First date/time in UTC (Combined date and time representation)    | 
| end_date            | date and time      | Date End                      | Last date/time in UTC (Combined date and time representation)          | 
| provider              | string                   | Provider  (optional)       | Provider name and contact. Keys: [name, url]
| license                | string                   | Data license (optional)  | Data license name based on SPDX License List | SPDX doesn't contain all
| links                    | dict                      | Resource links              | Dictionary of links to resources, could be download or other URLs (self and thumbnail required) |


This specification will be extended by various community profiles and vendors. And there are two fields that need to be
revisited:

revisit later in version 2:
| version                | semantic versioning number | Product Version | The version of the imagery metadata fields, for testing/validation  | 

Removed for now:
| product_type      | string                   | Product Type                 | Product types: [eo, sar, model, point-cloud, video] | 



