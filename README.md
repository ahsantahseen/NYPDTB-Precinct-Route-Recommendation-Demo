# NYPD-TB Precinct Route Recommendation Demo

## What is this?
This is a simple stakeholder demo for NYPD/MTA transit operations.

It answers one workflow:
1. Select a transit precinct.
2. View stations associated with that precinct.
3. Get a recommended patrol route based on ML-predicted station demand.

## What it shows
- Precinct-level summary (stations, predicted demand, lines, route distance)
- Interactive map with route polyline and station markers
- Ordered route table
- Full station list for the selected precinct

## How data was generated
- Station-level historical transit complaint and temporal feature data was used as the modeling input.
- Subway station geospatial data was used to place and connect stations on the map.
- A lightweight ML regression step was used to estimate near-term station-level complaint demand.
- Those station-level predictions were then grouped into transit precinct views for allocation and route planning.
- Station-to-precinct association in this demo is based on nearest precinct anchor-station approximation.

This was generated as a Proof of Concept using intermediate ML prediction outputs; the final deployable model artifact is still in progress and is not uploaded yet.
