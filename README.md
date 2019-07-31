# heroku-buildpack-tippecanoe

This buildpack clones, compiles, and installs Mapbox's [Tippecanoe](https://github.com/mapbox/tippecanoe) library for generating vector tiles from source data.

## Configuration

Add a `.tippecanoe-version` file to the source directory of your application to pin the version of tippecanoe that gets installed. If not specified, this buildpack will install the HEAD version of tippecanoe.

Example `.tippecanoe-version` file:

```sh
1.34.3
```

## Installation

`tippecanoe` and related binaries get installed to your application's `bin/` directory, which should already be on the application `$PATH`.
