## About

This repository aims to standardize imagery metadata and associated API components to store and work with  remotely-sensed imagery. A number of software and data providers have been creating RESTful JSON-based image catalogs. These end up all looking fairly similar, but are still different enough that each needs custom-coded client libraries. A set of standardized API's should increase interoperability, enabling more imagery analysis and value-add product development. 

## Contributing

Anyone building software that catalogs imagery is welcome to collaborate. Our goal is to be a collaboration of developers, not [architecture astronauts](http://www.joelonsoftware.com/articles/fog0000000018.html). The first step to join the collaboration is to add a folder to the 'implementations' folder with an [OpenAPI Spec](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md) (v2.0) of your implementation, along with markdown document describing your implementation.

A first meeting (ideally in person) among those with implementations who are interested in standardizing will kick off a first version of specification, with each group iterating on their version of that common standard. From there the spec(s) will evolve according to open source principles, using github as the primary tooling (pull requests and reviews for all changes, etc).


## In this repo

@TODO

# Radiant Imagery Metadata Schema v1.0

Any data sources listed in the registry will need to follow a specification to enable valid indexing within a catalog instance. 
A metadata file is required for each image file or bundle in the storage location (S3 bucket, FTP, Dropbox, NFS etc). 
An image file is an RGB GeoTIFF.This repository contains the imagery metadata specification, implementation guide and sample.json.


## Sample file

See [sample.json](sample.json)

## Specification Description 

| element           | type   | name                    | description                                                                                 | 
|-------------------|--------|-------------------------|---------------------------------------------------------------------------------------------| 
| uuid              | string | RFC 4122                | unique UUID v4                                                                              | 
| scene_id          | string | Scene id                | scene id from provider                                                                      |
| scene_title       | string | Title                   | scene title from provider of generated                                                      |
| paths             | object | local and remote paths  | local and remote paths with related protocols                                               |
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
