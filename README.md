# summer2022

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A prototype for a map-based data collection and visualization tool, created as a collaboration with Mr. Fukano.

## Demo

- **ふくモン プロトタイプ (Full Survey):** [mysurvey.futbol/fukumon](https://www.mysurvey.futbol/fukumon)
- **Map View Only:** [code4fukui.github.io/summer2022/](https://code4fukui.github.io/summer2022/)

## Overview

This project uses the `<csv-map>` web component to render points of interest on a map directly from CSV data embedded in an HTML file. Each row in the CSV represents a location, including a title, an image URL, and a `geo3x3` geospatial code.

The map displays data points for local figures and artisans, such as a lacquerware craftsman (`土直漆器さん`) and a paleontologist (`化石学者さん`), using images sourced from various platforms.

## Usage

To implement the map, include the `csv-map.js` script and add the `<csv-map>` element to your HTML with your data inside.

**Example:**
```html
<script type="module" src="https://code4fukui.github.io/csv-map/csv-map.js"></script>

<csv-map>
title,url,filename,geo3x3
深野さん,https://scontent-sjc3-1.xx.fbcdn.net/v/t1.18169-9/..._n.jpg,13265979..._n.jpg,E913873235844
土直漆器さん,https://drive.google.com/file/d/1v2KcxfeGGbRI8m7Qh1n79taz_Az2AP6Z/view,職人_漆器.jpeg,E9138733613632
</csv-map>
```

### CSV Data Format

The CSV data must contain the following columns:

- `title`: The name or title for the map pin.
- `url`: The direct URL to the image or associated web page.
- `