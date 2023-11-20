## Preview Maptiles
You can preview the resulting maptiles and MVT style.json in this repo here:

[Preview Maptiles as hosted on Github Pages](https://ctrepka.github.io/pmtiles_basemaps/preview)

## Problem Space
With multiple maptile source providers moving toward a paid model, I began seeking alternative maptile layers for use at work.
Nearly every 3rd party now charges a fee for retreiving maptiles. 

## Solution Space
While searching for static tile layer hosting methods, as opposed to the
traditional model of chopping tiles into zoom level directories with tiles in each directory, I found the pmtiles spec. Curious to test
this newer method of map tile hosting, I started with a small example hosted on GitHub. I was pleased to find that pmtiles were quick and 
simple to create from a source of vector data. In this case, open streetmaps are the originating source of streetmap data. PMTiles takes advantage
of the HTTP Byte Range request header to select only a portion of a binary blob on a CDN. This effectively provides a "serverless" hosting solution
for hosting scalable Mapbox Vector Tiles with little effort and very low costs, especially when using a cloud provider with zero egrees fees.

## Extract pmtiles area
`pmtiles extract <tile_src_url> <output_name>.pmtiles --bbox=<bbox_coordinates>`

### Tile source used
https://build.protomaps.com/20231001.pmtiles

### Bbox coordinates used
-98.20541,30.79963,-97.24411,29.90493
