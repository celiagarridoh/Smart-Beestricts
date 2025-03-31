# Smart Beestricts

Dataset and codes of the paper "Smart Beestricts: improving the spatial resolution of air-quality data in Madrid through Transfer Learning", published in the International Journal of Geographical Information Science (2025).

Authors:
- Celia Garrido-Hidalgo (Celia.Garrido@uclm.es, Universidad de Castilla-La Mancha).
- Gürkan Solmaz (Guerkan.Solmaz@neclab.eu, NEC Laboratories Europe GmbH).
- Tobias Jacobs (Tobias.Jacobs@neclab.eu, NEC Laboratories Europe GmbH).
- Luis Roda-Sanchez (Luis.Roda@uclm.es, Universidad de Castilla-La Mancha).

NEC Laboratories Europe GmbH, Copyright (c) 2025, All rights reserved.  

The data is presented in three formats:
- Raw data presents the original raw data mapped to station locations according to the data source.
- Processed data includes temporal data interpolation and removal of frozen stations.
- Aggregated data presents aggregated data to the H3 grid (resolution = 7).
  
All the data is available in .pkl format based on GeoPandas Dataframes (gdf).

Data folder structure:
```
.
├── LICENSE
├── codes
|   └── numerical_results          # Reproducibility of numerical and graphical results
|   |   ├── confusion_plots.py
|   |   ├── cross_validation.py
|   |   ├── hexagonal_grid.py
|   |   ├── overall_reusability_results.py
|   |   └── ts_clsutering.py
|   ├── processing_ipynb        # Jupyter notebooks to obtin dataset processed files           
|   |   ├── airpollution_preparation1.ipynb
|   |   ├── airpollution_preparation2.ipynb
|   |   ├── traffic_preparation1.ipynb
|   |   ├── traffic_preparation2.ipynb
|   |   ├── weather_preparation1.ipynb
|   └── └── weather_preparation2.ipynb
├── air_pollution
|   ├── raw_data               # Raw data (mapped to station location)  
|   |   ├── gdf_CO.pkl
|   |   ├── gdf_NO2.pkl
|   |   ├── gdf_O3.pkl
|   |   ├── gdf_PM10.pkl
|   |   ├── gdf_PM2.5.pkl
|   |   └── gdf_SO2.pkl
|   ├── processed_data         # Processed data (filtered and re-sampled) 
|   |   ├── gdf_CO.pkl
|   |   ├── gdf_NO2.pkl
|   |   ├── gdf_O3.pkl
|   |   ├── gdf_PM10.pkl
|   |   ├── gdf_PM2.5.pkl
|   |   └── gdf_SO2.pkl
|   ├── aggregated_data        # Hexagon-aggregated data 
|   |   ├── gdf_CO.pkl
|   |   ├── gdf_NO2.pkl
|   |   ├── gdf_O3.pkl
|   |   ├── gdf_PM10.pkl
|   |   ├── gdf_PM2.5.pkl
|   |   └── gdf_SO2.pkl
├── traffic
|   ├── raw_data               # Raw data (mapped to station location)  
|   |   └── gdf_traffic.pkl
|   ├── aggregated_data        # Hexagon-aggregated (only urban) data 
|   |   └── gdf_traffic_urb.pkl
├── weather
|   ├── raw_data               # Raw data (mapped to station location)  
|   |   ├── gdf_temperature.pkl
|   |   ├── gdf_relhumidiy.pkl
|   |   └── gdf_irradiation.pkl
|   ├── processed_data         # Processed data (filtered and re-sampled)  
|   |   ├── gdf_temperature.pkl
|   |   ├── gdf_relhumidiy.pkl
|   |   └── gdf_irradiation.pkl
|   ├── aggregated_data        # Hexagon-aggregated data 
|   |   ├── gdf_temperature.pkl
|   |   ├── gdf_relhumidity.pkl
|   |   └── gdf_irradiation.pkl
└── meteorology	
    ├── raw_data               # Raw data (mapped to station location) 
    |   ├── gdf_wind_speed.pkl
    |   ├── gdf_wind_direction.pkl
    |   ├── gdf_barometric_pressure.pkl
    |   └── gdf_rain.pkl
    ├── processed_data         # Processed data (filtered and re-sampled) 
    |   ├── gdf_wind_speed.pkl
    |   ├── gdf_wind_direction.pkl
    |   ├── gdf_barometric_pressure.pkl
    |   └── gdf_rain.pkl
    └── aggregated_data        # Hexagon-aggregated data
        ├── gdf_wind_speed.pkl
        ├── gdf_wind_direction.pkl
        ├── gdf_barometric_pressure.pkl
        └── gdf_rain.pkl
```

Acknowledgement for original data: Origen de los datos: [Ayuntamiento de Madrid](https://datos.madrid.es/portal/site/egob) / [Powered by EMT de Madrid](http://www.emtmadrid.es).
