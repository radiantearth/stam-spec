## About

The Spatio-Temporal Asset Metadata aims to standardize common fields to search remotely-sensed imagery and other geospatial assets. It is a complementary specification to Spatio-Temporal Asset Catalog - indeed most every item of those catalogs will
expose its Spatio-Temporal Asset Metadata. 

The metadata fields are selected primary for search, and cross-catalog compatibility. In time a set of 'extensions' will
emerge to better specify and search certain types of assets, but the main goal is to enable a baseline of standardization.
Providers of imagery are also able to extend to the fields they care about.

This repository contains the 'abstract' specification of the core fields and their explanation. The JSON specification is 
currently being evolved in the [stac-spec](https://github.com/radiantearth/stac-spec) repo, so that it stays in line with
the catalog as a whole. This repo is maintained independently to emphasize that the core fields can be re-used in other 
contexts, like potentially embedded in GeoTIFFss, so that [cloud optimized geotiffs](http://cogeo.org) can be more 
self-describing. So the repo may lag a bit behind the latest.

## Background

This work started as the [Open Imagery Network Metadata](https://github.com/openimagerynetwork/oin-metadata-spec) spec, but is evolving to be more generic and flexible. Ideally the OIN metadata spec will simply be a compatible version of this metadata, with a constraint that data license must be a single, open data license. Additional work on the spec was done at the 
[stac boulder sprint](https://github.com/radiantearth/boulder-sprint)

## Contributing

All contributions should be done with pull requests, and should be informed by real, working software. 


## In this repo

[abstract-spec.md](abstract-spec.md) contains the core fields and their explanations. 

