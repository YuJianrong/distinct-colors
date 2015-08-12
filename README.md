# Distinct Colors

This is a complete rewrite of (but is heavily inspired by) [Mathieu Jacomy's](https://github.com/jacomyma) [Palette Generator](https://github.com/medialab/iwanthue/blob/master/js/libs/chroma.palette-gen.js)

I have taken the ideas and the theories, and put them into a simple modular library. I have also optimized it for speed.

This library generates a palette of *visually* distinct colors, and returns an array of [chroma-js](https://github.com/gka/chroma.js) objects.

## Installation

```
npm install distinct-colors
```

## Getting Started

```javascript
var distinctColors = require('distinct-colors')

var palette = distinctColors() // You may pass an optional config object

// Thats it!
```

## API

#### distinctColors([options])

Generates a new palette. Returns an array of [chroma-js](https://github.com/gka/chroma.js) objects.

#### Options

| Name | Type | Valid Range | Default | Description |
| --- | --- | --- | --- | --- |
| count | integer | `0 <= value <= Infinity` | `5` | The number of colors the palette should contain |
| hueMin | integer | `0 <= value <= 360` | `0` | The minimum hue for colors in the palette. Default: |
| hueMax | integer | `0 <= value <= 360` | `360` | The maximum hue for colors in the palette. Default: |
| chromaMin | integer | `0 <= value <= 100` | `0` | The minimum chroma (color) for colors in the palette. Default: |
| chromaMax | integer | `0 <= value <= 100` | `100` | The maximum chroma (color) for colors in the palette. Default: |
| lightMin | integer | `0 <= value <= 100` | `0` | The minimum lightness for colors in the palette. |
| lightMax | integer | `0 <= value <= 100` | `100` | The maximum lightness for colors in the palette. |
| quality | integer | `1 <= value <= Infinity` | `50` | The number of steps for [k-means](https://en.wikipedia.org/wiki/K-means_clustering) convergence. |
| samples | integer | `1 <= value <= Infinity` | `2000` | The number of color samples to choose from. |