# STePNet

**STePNet** — **Spatially Transferable Pedestrian Demand and Network Modeling** — is an open-source Python framework for estimating pedestrian network flows in data-scarce cities.

STePNet integrates transferable pedestrian trip generation, destination choice, route assignment, OD demand adjustment, and graph-based diagnostics into a unified modeling pipeline. The framework is designed for cities where detailed pedestrian origin–destination data or link-level pedestrian counts are limited or unavailable.

---

## Repository Description

Graph-based transferable pedestrian demand and network flow modeling framework for data-scarce cities.

---

## Overview

STePNet estimates link-level pedestrian flows by combining:

1. **Transferable trip generation**
2. **Destination choice and OD flow estimation**
3. **Pedestrian route assignment**
4. **OD demand adjustment using observed pedestrian counts**
5. **Graph-based diagnostics of demand structure**

The framework supports transferability analysis across cities and spatial aggregation systems such as SA1s, Census Tracts, or other user-defined zones.

---

## Main Workflow

STePNet follows the modeling pipeline below:

```text
Input spatial data
        ↓
Trip generation
        ↓
Destination choice / OD matrix estimation
        ↓
Route generation
        ↓
C-Logit route assignment
        ↓
Link-level pedestrian flow estimation
        ↓
OD demand adjustment
        ↓
Graph-based transferability diagnostics


Python Requirements

The framework is developed in Python. Recommended version:

Python >= 3.9

Required packages:

pandas
numpy
geopandas
shapely
networkx
osmnx
scikit-learn
scipy
statsmodels
matplotlib
seaborn
tqdm
pyproj
rtree

Optional packages:

torch
torch-geometric
contextily
folium
plotly
```
---

## Repository Description


1. Spatial Aggregation Zones
2. Socio-Demographic Data in each zone
population
household_income
vehicle_ownership
median_age
3. Land-Use Data in each zone
commercial_landuse
residential_landuse
education_landuse
hospital_landuse
industrial_landuse
parkland_landuse
transport_landuse
4. Network Connectivity Data
intersection_count
number_of_nodes
edge_density
links_nodes_ratio
street_node_average
5. Public Transport Accessibility
6. Pedestrian Network
edge_id
from_node
to_node
geometry
length
slope
gradient
number_of_turns
number_of_crossings
green_view_index
poi_count


In the paper, STePNet is applied to:

Sydney, Australia
New York City, USA

Transferable demand models are trained in:

Brisbane, Australia
Seattle, USA

The framework shows that transferred pedestrian demand models can estimate network-level pedestrian flows after calibration, even when detailed local demand data are unavailable.
