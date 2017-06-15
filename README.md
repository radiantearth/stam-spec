## About

This repository aims to standardize imagery metadata to work with remotely-sensed imagery. It focuses on the core abstract metadata fields, as well as the simpler instantiations of those fields (json, embedded in geotiff tiff tags, etc). The abstract fields can also be used to define API responses. This spec aims to be a lowest common denominator of the minimal metadata to help machines and humans understand the source of imagery. Extension mechanisms will enable providers to add in more information if they so choose. 

This work started as the [Open Imagery Network Metadata](https://github.com/openimagerynetwork/oin-metadata-spec) spec, but is evolving to be more generic and flexible. Ideally the OIN metadata spec will simply be a compatible version of this metadata, with a constraint that data license must be a single, open data license.

## Contributing

All contributions should be done with pull requests, and should be informed by real, working software. This repository also contains a ['non-standard-implementations'](./non-standard-implementations) folder that gathers the existing implementations in the real world, so that everyone can see what others have done in the world so far.


## In this repo

[abstract-spec.md](abstract-spec.md) contains the core fields and their explanation. The [json folder](./json-spec) contains the json instantiation of the abstract spec.

# Using Radiant Imagery Metadata Schema v0.1

The use patterns are very much still evolving. But the first use is leveraging the [json imagery metadata](./json/json-spec.md) as a sidecar file to an image file. An image file is generally an RGB GeoTIFF (but could be multiband or single band data), in an online storage location. The recommended format is a [cloud-optimized GeoTIFF](https://trac.osgeo.org/gdal/wiki/CloudOptimizedGeoTIFF), stored on an object store that supports HTTP Range queries for efficient cloud access.
