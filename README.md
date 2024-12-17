# Identifying Suitable Aquaculture Habitats 
## An Analysis of Exclusive Economic Zones of The West Coast 

![oyster-aquaculture-image](https://www.fisheries.noaa.gov/s3//styles/original/s3/2021-10/hog-island-oyster-co-lease.png?itok=pKpf1VLD)
Source : [fisheries.noaa.gov](https://www.fisheries.noaa.gov/feature-story/tide-table-profiles-hog-island-oyster-co)

By [Stephen Carroll](https://stephenccodes.github.io./) 

## About

This repository hold the project `aquaculture_habitats.qmd` which has a goal of determining which Exclusive Economic Zones (EEZ) on the West Coast of the United States are best suited to developing marine aquaculture for a given species. It makes this determination using suitable ranges of sea surface temperature (SST) and  depth below the sea level in meters. The data is presented as a map of the West coast, with EEZs shaded by total suitable area.

The workflow was established with the generic species 'Oysters'. This workflow was then generalized into a function able to determine the total suitable area by EEZ for any given species with the following arguments provided:

- `species` str, the name of the species of interest
- `min_sst` int, the minimum suitable sea surface temperature of the species
- `max_sst` int, the maximum suitable sea surface temperature of the species
- `min_depth` int, the minimum suitable depth of the species
- `max_depth` int, the maximum suitable depth of the species

Information on species depth and temperature requirements on [SeaLifeBase.](https://www.sealifebase.ca/search.php)

### Skills used in this analysis:

- Raster resampling, reclassifying, and zonal algebra

- Working with vector data using sf

- Working with raster data using terra

- Map making using tmap

- Writing a function for repeatable workflow


## Data access

Data for this project was downloaded and read in from the sources listed below. All data files can be found locally in the `data` folder. 


### Citations

- Bathymetry data: [GEBCO Compilation Group](https://www.gebco.net/data_and_products/gridded_bathymetry_data/#area)

- Exclusive Economic Zone data: [Flanders Marine Institue](https://www.marineregions.org/eez.php)

- Sea Surface Temperature data: [NOAA Coral Reef Watch](https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php)

- Species aquaculture data: [Sea Life Base](https://www.sealifebase.ca/search.php)

- Hall, S. J., Delaporte, A., Phillips, M. J., Beveridge, M. & O’Keefe, M. Blue Frontiers: Managing the Environmental Costs of Aquaculture (The WorldFish Center, Penang, Malaysia, 2011).
- Gentry, R. R., Froehlich, H. E., Grimm, D., Kareiva, P., Parke, M., Rust, M., Gaines, S. D., & Halpern, B. S. Mapping the global potential for marine aquaculture. Nature Ecology & Evolution, 1, 1317-1324 (2017).
- GEBCO Compilation Group (2022) GEBCO_2022 Grid (doi:10.5285/e0f0bb80-ab44-2739-e053-6c86abc0289c).

## References & Acknowledgements

All materials were created by [Ruth Oliver](https://github.com/ryoliver) for EDS-223.

## Repository Organization

```
├── aquaculture_habitats_files/
├─ data/
│    ├── average_annual_sst_2008.tif     # Yearly SST data
│    ├── average_annual_sst_2009.tif
│    ├── average_annual_sst_2010.tif
│    ├── average_annual_sst_2011.tif│
│    ├── average_annual_sst_2012.tif
│    ├── depth.tif                       # Bathymetry data
│    ├── wc_regions_clean.dbf
│    ├── wc_regions_clean.prj
│    ├── wc_regions_clean.shp            # Economic zone data
│    └── wc_regions_clean.shx             
├── .gitignore
├── README.md                         
├── aquaculture_habitats.Rproj
├── aquaculture_habitats.html
└── aquaculture_habitats.qmd         # Complete analysis quarto document
```
  
  
  
  
  
  
  
  
  
  
 