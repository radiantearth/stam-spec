## About

This repository aims to standardize imagery metadata to work with remotely-sensed imagery. It focuses on the core abstract metadata fields, as well as the simpler instantiations of those fields (json, embedded in geotiff tiff tags, etc). The abstract fields can also be used to define API responses. This spec aims to be a lowest common denominator of the minimal metadata to help machines and humans understand the source of imagery. Extension mechanisms will enable providers to add in more information if they so choose. 


## Contributing

All contributions should be done with pull requests, and should be informed by real, working software. This repository also contains a 'non-standard-implementations' folder that gathers the existing implementations in the real world, so that everyone can see what others have done in the world so far.


## In this repo

abstract-spec.md contains the core fields and their explanation. The 'implementations' folder will evolve json and tiff tag manifestations of the abstract specification. 

# Radiant Imagery Metadata Schema v0.1

A metadata file is required for each image file or bundle in the storage location (S3 bucket, FTP, Dropbox, NFS etc). 
An image file is an RGB GeoTIFF.This repository contains the imagery metadata specification, implementation guide and sample.json.


