# osm-adiff-parser-saxjs

Parses OSM augmented diff (`.osc` files) and returns elements grouped by changeset ids.

- Based on the parser in [planet-stream](https://github.com/developmentseed/planet-stream).
- For the node version, see [osm-adiff-parser](https://github.com/mapbox/osm-adiff-parser).

## Setup

* npm install --save osm-adiff-parser

## Usage

```js

var parser = require('osm-adiff-parser');

// to filter certain changesets

parser(xml, ['46613588', '46613589'], function(err,data) {
    console.log(data);
});

// to get all changesets

parser(xml, null, function(err,data) {
    console.log(data);
});

```
