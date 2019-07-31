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

## Dependencies & Troubleshooting

This buildpack is verified to work on build machines on Heroku's `heroku-18` stack.

The only additional dependency you need is `libsqlite3-dev`; the [Aptfile buildpack](https://github.com/heroku/heroku-buildpack-apt) is a good way to get that installed.
