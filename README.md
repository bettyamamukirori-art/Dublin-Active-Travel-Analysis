# **# 🚲 Dublin Mobility Project: Dundrum-Sandyford Corridor**

# 

An open-source spatial analysis project evaluating active travel (cycling and walking) infrastructure and transit accessibility (Luas Green Line) within the Dundrum-Sandyford mobility corridor in Dublin, Ireland.



### \## 📌 Project Overview

This project processes geographic data to analyse how well connected the cycling and walking network is to key transit hubs. By leveraging OpenStreetMap (OSM) data and local transit datasets, this repository automates the extraction, cleaning, and filtering of spatial networks to prepare for catchment and accessibility modelling.



\*\*Study Area:\*\* Dundrum to Sandyford, Dublin (Bounding Box: `53.300 N, -6.180 E, 53.250 S, -6.270 W`)



\## 🎯 Key Findings

\* \*\*53,112\*\* residents live within a 10-minute cycling catchment of the target stations.

\* \*\*12,289 Residents live within 10-Min Walking catchment.

\* \*\*2,063 vulnerable commuters.

\* \*\*37.9%\*\* of the supporting street network is classified as high-risk for vulnerable commuters.

\* \*\*12\*\* distinct high friction residential pockets were identified for immediate infrastructure intervention.



\## 🛠️ Tech Stack

\* \*\*Python 3.x\*\*

\* \*\*GeoPandas \& Pandas:\*\* Spatial data manipulation and filtering

\* \*\*OSMnx:\*\* Querying and downloading OpenStreetMap street networks

\* \*\*Shapely:\*\* Geometric operations

\* \*\*Jupyter Notebook:\*\* Interactive data pipeline



\## 📂 Repository Structure

To run this project locally, ensure your folders are structured as follows. \*(Note: Raw data files are not tracked in this repository due to size; please place them in the `raw` folder before running).\*



```text

dublin\_mobility\_project/            (left out CSO\_saps\_data.geojson due to file size limit)

│

├── data/

│   ├── raw/                                        # Original datasets (Not tracked in Git)

│   │   ├── cso\_saps\_data.geojson                   # Census Small Area Population Statistics

│   │   ├── cso\_small\_area\_boundaries.geojson       # CSO geographic boundaries

│   │   ├── dublin\_active\_travel.geojson            # Active travel off-road paths

│   │   ├── dublin\_cycle\_infrastructure.csv         # Local cycling infrastructure data

│   │   ├── dublin\_street\_edges.geojson             # Raw OSM street edges

│   │   ├── dublin-metropolitan-area-existing-protected-cycle-infrastructure-2025/

│   │   ├── routes.txt                              # GTFS transit routes

│   │   ├── stops.txt                               # GTFS transit stops

│   │   └── Small\_Area\_National\_Statistical\_Boundaries\_2022\_Ungeneralised...

│   │

│   └── processed/                                  # Cleaned data, analytics, and model outputs

│       ├── Dublin\_cycle\_network.geojson

│       ├── Dublin\_demographics\_sa2022.geojson

│       ├── Dublin\_luas\_stops.geojson

│       ├── Isochrone\_cycle\_1500m.geojson           # 1.5km cycle catchment buffers

│       ├── Isochrone\_cycle\_3000m.geojson           # 3.0km cycle catchment buffers

│       ├── Isochrone\_walk\_400m.geojson             # 400m walk catchment buffers

│       ├── Isochrone\_walk\_800m.geojson             # 800m walk catchment buffers

│       ├── Osm\_corridor\_edges.geojson

│       ├── Osm\_corridor\_edges\_tagged.geojson

│       ├── Osm\_corridor\_nodes.geojson

│       ├── Osm\_corridor\_safety\_scored.geojson      # Road network safety analysis

│       ├── Phase5\_high\_friction\_neighborhoods.csv  # Connectivity barriers analysis

│       ├── Processed\_dublin\_cycle\_infrastructure.geojson

│       ├── Processed\_dublin\_protected\_cycle\_infrastructure.geojson

│       ├── Processed\_gtfs\_routes.csv

│       ├── Processed\_gtfs\_stops\_dundrum.geojson

│       ├── Processed\_luas\_5\_stations.geojson

│       ├── Small\_areas\_combined\_infrastructure\_distances.csv

│       └── top\_10\_active\_travel\_priority\_areas.csv # Final prioritization outputs

│

├── notebooks/

│   └── dublin\_mobility\_analysis.ipynb              # Main data processing pipeline

│

└── README.md

