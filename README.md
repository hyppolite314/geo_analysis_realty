# Geo-Spatial Analysis of Housing / Rental Market in San Francisco
Geo-spatial analysis of the housing market for San Francisco, using PyViz functions. The tools built in this module were designed based on a one-click buy-and-rent busines idea for people to buy properties and then rent them.

Based on the usage of interactive visualizations and geospatial analysis, the objective is to find properties in the San Francisco market, which are viable investment opportunities.

---

## Technologies

Required programs, libraries, systems, and overall dependencies:

Python (version 3.0 or later)
<br>
`Pathlib`
<br>
`pandas`
<br>
`%matplotlib`
<br>
`hvplot.pandas`

---

## Installation Guide

`pip install Pathlib`

conda install -c pyviz hvplot geoviews

---

## Usage

Interactive Line Plots:

```python
prices_sqft_yr_plot = prices_square_foot_by_year.hvplot.line(
    x='year',
    y=['sale_price_sqr_foot','gross_rent'],
    title="Gross Rent / Sale Price per SqFt",
).opts(yformatter="%.0f")
```
![Screenshot of Plot](https://github.com/hyppolite314/geo_analysis_realty/blob/main/inter_plot.png?raw=true)

GeoViews via `hvplot.points`

```python
all_neighborhoods_plot = all_neighborhoods_df.hvplot.points(
    'Lon',
    'Lat',
    geo=True,
    size='sale_price_sqr_foot',
    scale=1,
    color='gross_rent',
    tiles='OSM',
    frame_width=700,
    frame_height=500,
    title = "Average Sales Price per SqFt (2010-2016)"
    )

all_neighborhoods_plot
```
![Screenshot of Plot](https://github.com/hyppolite314/geo_analysis_realty/blob/main/geo_view.png?raw=true)

---

## Contributors

Reginald Hyppolite
https://www.linkedin.com/in/reginald-hyppolite-nyc/

BIG THANKS to all the great TAs and Professor Vinicio DeSola

---

## License

N/A -- Free open.ware for a better world.