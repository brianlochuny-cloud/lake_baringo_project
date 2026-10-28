# Lake Baringo Shoreline Change and Flood-Risk Screening, 2002–2026

Mapping how far Lake Baringo (Kenya) has expanded, whether the growth is continuing, and which land and infrastructure could be reached by 2027 and 2032.

**Author:** Brian Lochuny, Institute of Geomatics, GIS (Geographic Information System) and Remote Sensing (IGGReS), Dedan Kimathi University of Technology (DeKUT)

## Key results

| Year | Lake area (km²) | Satellite and sensor | Scene date(s) |
|---|---|---|---|
| 2002 | 120.36 | Landsat 7 ETM+ | 1 Feb 2002 |
| 2007 | 116.99 | Landsat 7 ETM+ | 3 Mar 2007 + 22 May 2007 (gap-fill) |
| 2012 | 137.65 | Landsat 7 ETM+ | 13 Feb 2012 + 28 Jan 2012 (gap-fill) |
| 2017 | 188.50 | Landsat 8 OLI | 18 Feb 2017 |
| 2022 | 221.19 | Landsat 8 OLI | 16 Feb 2022 |
| 2026 | 227.64 | Landsat 9 OLI-2 | 19 Feb 2026 |

- The lake grew from 120.36 km² to 227.64 km² between 2002 and 2026, an increase of 89%.
- Growth peaked at about 10 km² a year in 2012–2017 and slowed to about 1.6 km² a year in 2022–2026, so a straight-line trend would overshoot.
- The 2026 water map reached 99% overall accuracy (kappa 0.98) on 100 stratified random points.

## Projections (screening estimates)

| Scenario | Lake area (km²) | Buildings reached (minimum, cumulative) | Roads and tracks reached (km, minimum) |
|---|---|---|---|
| 2027 (recent-rate estimate) | about 229 | 17 | 2.16 |
| 2032 central | about 237 | 27 | 3.92 |
| 2032 high | about 262 | 115 | 26.75 |

The risk zones were built from a smoothed Shuttle Radar Topography Mission (SRTM) elevation model. A zone is the observed 2026 lake plus land at or below a set elevation, connected to the lake: 979 m for 2027, 980 m for 2032 central and 983 m for 2032 high.

## Method in brief

1. Downloaded Landsat Collection 2 Level-2 (surface reflectance) scenes from USGS EarthExplorer for dry-season dates.
2. Mosaicked tiles, and filled the Landsat 7 scan-line gaps (2007, 2012) with a second date.
3. Calculated the Modified Normalized Difference Water Index (MNDWI) and classified water with a fixed threshold of 0.
4. Clipped to a study-area boundary, converted to polygons, kept only the polygons that belong to the lake, and measured the area per year.
5. Checked the 2026 map with 100 stratified random points.
6. Built 2027 and 2032 risk zones from the elevation model and counted OpenStreetMap buildings and roads inside them.

All processing was done in ArcGIS Pro. Summary tables were prepared in WPS Office.

## Limitations

- The 2027 and 2032 figures are first-order screening estimates, not precise forecasts. The lake's rise reflects rainfall variability, catchment siltation and possibly tectonic influence, not a smooth trend.
- The accuracy check was labelled against the same Landsat image, so it is not fully independent.
- The SRTM lake surface reads about 972 m (flown in February 2000), but land flooded since 2002 has a median of about 976.8 m, so zone levels were set by matching the area estimates rather than from a fixed lake level.
- OpenStreetMap coverage is incomplete, so building and road counts are minimums. Power lines were not assessed.
- Field surveys should confirm any result before it is used for decisions.

## Repository contents

```
lake_baringo_project/
├── README.md
├── maps/     shoreline 2002–2026, before/after, projected 2027, risk zones 2032
├── charts/   lake area over time
├── data/     Excel workbook, lake outlines 2002–2026, 2027 and 2032 risk bands
└── poster/   conference poster (added later)
```

Large raw rasters and the geodatabase are not included.

## Data sources

- Landsat Collection 2 Level-2 imagery: U.S. Geological Survey (USGS), via EarthExplorer.
- Elevation: SRTM.
- Buildings and roads: © OpenStreetMap contributors, downloaded via Geofabrik (Open Database Licence).

## Licence

The maps, charts and tables created in this project are shared under Creative Commons Attribution 4.0 International (CC BY 4.0). You may reuse them if you credit Brian Lochuny. OpenStreetMap-derived data remains under its own licence.

## Contact

- LinkedIn: https://www.linkedin.com/in/brian-lochuny-2b7982386/
- Email: Brianlochuny@gmail.com
