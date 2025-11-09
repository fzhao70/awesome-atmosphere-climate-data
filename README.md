# Awesome Atmospheric and Climate Data [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of atmospheric and climate datasets for research, analysis, and applications. Each dataset includes source information, citations, content description, usage, and access methods.

## Contents

- [Reanalysis Datasets](#reanalysis-datasets)
- [Satellite Data](#satellite-data)
- [In-situ Observations](#in-situ-observations)
- [Climate Model Data](#climate-model-data)
- [Greenhouse Gas Data](#greenhouse-gas-data)
- [Precipitation Data](#precipitation-data)
- [Temperature Data](#temperature-data)
- [Wind and Circulation Data](#wind-and-circulation-data)
- [Ocean-Atmosphere Interaction](#ocean-atmosphere-interaction)
- [Aerosol and Air Quality Data](#aerosol-and-air-quality-data)
- [Cryosphere Data](#cryosphere-data)
- [Radiation Data](#radiation-data)
- [Extreme Weather Data](#extreme-weather-data)
- [Paleoclimate Data](#paleoclimate-data)

---

## Reanalysis Datasets

Reanalysis datasets combine observational data with numerical weather prediction models to create comprehensive, gridded datasets spanning multiple decades.

### ERA5

- **Source**: European Centre for Medium-Range Weather Forecasts (ECMWF)
- **Citation**: Hersbach, H., Bell, B., Berrisford, P., et al. (2020). The ERA5 global reanalysis. Quarterly Journal of the Royal Meteorological Society, 146(730), 1999-2049.
- **Content**: Hourly atmospheric, land, and ocean-wave parameters from 1940 to present with 31 km horizontal resolution and 137 vertical levels
- **Usage**: Weather analysis, climate research, renewable energy assessment, air quality modeling, hydrological studies
- **How to Use**:
  - Access via Copernicus Climate Data Store (CDS): https://cds.climate.copernicus.eu/
  - Python API: `cdsapi` library
  - Direct download or streaming via CDS toolbox
  - Example: `c.retrieve('reanalysis-era5-single-levels', {...})`

### ERA5-Land

- **Source**: ECMWF
- **Citation**: Muñoz Sabater, J. (2019). ERA5-Land hourly data from 1950 to present. Copernicus Climate Change Service (C3S) Climate Data Store (CDS).
- **Content**: Hourly land surface variables from 1950 to present at 9 km resolution
- **Usage**: Hydrology, agriculture, land surface modeling, water resources management
- **How to Use**:
  - Access via CDS: https://cds.climate.copernicus.eu/
  - API: `cdsapi` for Python
  - Variables include soil moisture, snow depth, temperature, evaporation

### MERRA-2

- **Source**: NASA Global Modeling and Assimilation Office (GMAO)
- **Citation**: Gelaro, R., et al. (2017). The Modern-Era Retrospective Analysis for Research and Applications, Version 2 (MERRA-2). Journal of Climate, 30(14), 5419-5454.
- **Content**: Atmospheric reanalysis from 1980 to present with 0.5° × 0.625° resolution, 72 vertical levels
- **Usage**: Aerosol research, renewable energy, climate variability studies, atmospheric composition
- **How to Use**:
  - Access via NASA GES DISC: https://disc.gsfc.nasa.gov/
  - Download tools: wget, curl, or OPeNDAP
  - Python: `pydap` or direct HTTP download

### JRA-55

- **Source**: Japan Meteorological Agency (JMA)
- **Citation**: Kobayashi, S., et al. (2015). The JRA-55 Reanalysis: General specifications and basic characteristics. Journal of the Meteorological Society of Japan, 93(1), 5-48.
- **Content**: Global atmospheric reanalysis from 1958 to present with ~60 km resolution, 60 vertical levels
- **Usage**: Climate monitoring, tropical meteorology, monsoon research, long-term climate studies
- **How to Use**:
  - Access via JMA data portal or NCAR Research Data Archive
  - Registration required
  - Download via web interface or ftp

### NCEP/NCAR Reanalysis 1

- **Source**: NOAA National Centers for Environmental Prediction (NCEP) and NCAR
- **Citation**: Kalnay, E., et al. (1996). The NCEP/NCAR 40-year reanalysis project. Bulletin of the American Meteorological Society, 77(3), 437-471.
- **Content**: Global reanalysis from 1948 to present with 2.5° × 2.5° resolution, 17 vertical levels
- **Usage**: Long-term climate analysis, trend detection, atmospheric circulation studies
- **How to Use**:
  - Access via NOAA PSL: https://psl.noaa.gov/data/gridded/data.ncep.reanalysis.html
  - Download via FTP or web interface
  - Python: `xarray` with OPeNDAP

### CFSR/CFSv2

- **Source**: NOAA NCEP
- **Citation**: Saha, S., et al. (2010). The NCEP Climate Forecast System Reanalysis. Bulletin of the American Meteorological Society, 91(8), 1015-1058.
- **Content**: Coupled atmosphere-ocean-land-sea ice reanalysis from 1979 to present, ~38 km resolution
- **Usage**: Seasonal forecasting, ocean-atmosphere interaction, climate prediction
- **How to Use**:
  - Access via NOAA NCEI or NCAR RDA
  - Download via HTTP or FTP
  - Subsetting tools available

---

## Satellite Data

### MODIS (Moderate Resolution Imaging Spectroradiometer)

- **Source**: NASA Terra and Aqua satellites
- **Citation**: Justice, C.O., et al. (2002). The Moderate Resolution Imaging Spectroradiometer (MODIS): Land remote sensing for global change research. IEEE Transactions on Geoscience and Remote Sensing, 36(4), 1228-1249.
- **Content**: Land surface, ocean, and atmospheric products including aerosols, clouds, vegetation, temperature (2000-present)
- **Usage**: Land cover mapping, vegetation monitoring, fire detection, aerosol analysis, cloud properties
- **How to Use**:
  - Access via NASA Earthdata: https://earthdata.nasa.gov/
  - Tools: `MODIS Reprojection Tool`, `AppEEARS`, Google Earth Engine
  - Python: `pyhdf`, `rasterio`, `earthaccess`

### GOES (Geostationary Operational Environmental Satellites)

- **Source**: NOAA
- **Citation**: Schmit, T.J., et al. (2017). A closer look at the ABI on the GOES-R series. Bulletin of the American Meteorological Society, 98(4), 681-698.
- **Content**: High-temporal resolution (5-15 min) imagery, lightning data, atmospheric motion vectors
- **Usage**: Weather forecasting, nowcasting, severe weather monitoring, aviation
- **How to Use**:
  - Access via NOAA CLASS or AWS Public Dataset
  - AWS S3: `s3://noaa-goes16/` and `s3://noaa-goes17/`
  - Python: `goes2go`, `satpy`

### Sentinel-5P TROPOMI

- **Source**: European Space Agency (ESA)
- **Citation**: Veefkind, J.P., et al. (2012). TROPOMI on the ESA Sentinel-5 Precursor: A GMES mission for global observations of the atmospheric composition. Remote Sensing of Environment, 120, 70-83.
- **Content**: Atmospheric composition (NO₂, O₃, SO₂, CH₄, CO, aerosols) with 7×3.5 km resolution
- **Usage**: Air quality monitoring, emission tracking, atmospheric chemistry research
- **How to Use**:
  - Access via Copernicus Open Access Hub: https://scihub.copernicus.eu/
  - Google Earth Engine
  - Python: `sentinelsat`, `harp`, `s5ppy`

### AIRS (Atmospheric Infrared Sounder)

- **Source**: NASA Aqua satellite
- **Citation**: Chahine, M.T., et al. (2006). AIRS: Improving weather forecasting and providing new data on greenhouse gases. Bulletin of the American Meteorological Society, 87(7), 911-926.
- **Content**: Temperature and humidity profiles, clouds, greenhouse gases (CO₂, CH₄), trace gases
- **Usage**: Weather prediction, climate monitoring, greenhouse gas tracking
- **How to Use**:
  - Access via NASA GES DISC
  - OPeNDAP, direct download
  - Python: `pydap`, `h5py`

### CALIPSO

- **Source**: NASA/CNES
- **Citation**: Winker, D.M., et al. (2009). Overview of the CALIPSO mission and CALIOP data processing algorithms. Journal of Atmospheric and Oceanic Technology, 26(11), 2310-2323.
- **Content**: Vertical profiles of aerosols and clouds using lidar
- **Usage**: Aerosol research, cloud vertical structure, atmospheric boundary layer studies
- **How to Use**:
  - Access via NASA Langley ASDC: https://asdc.larc.nasa.gov/
  - Python: `pyhdf`, custom readers

### GPM (Global Precipitation Measurement)

- **Source**: NASA/JAXA
- **Citation**: Hou, A.Y., et al. (2014). The Global Precipitation Measurement mission. Bulletin of the American Meteorological Society, 95(5), 701-722.
- **Content**: Global precipitation measurements every 3 hours with 0.1° resolution
- **Usage**: Precipitation monitoring, flood forecasting, water resources, agriculture
- **How to Use**:
  - Access via NASA GES DISC
  - IMERG products (Integrated Multi-satellitE Retrievals)
  - Python: `h5py`, direct download via API

### CERES (Clouds and Earth's Radiant Energy System)

- **Source**: NASA
- **Citation**: Wielicki, B.A., et al. (1996). Clouds and the Earth's Radiant Energy System (CERES): An Earth observing system experiment. Bulletin of the American Meteorological Society, 77(5), 853-868.
- **Content**: Earth radiation budget, cloud properties, surface radiation
- **Usage**: Climate modeling, radiation budget studies, cloud-climate feedback research
- **How to Use**:
  - Access via NASA Langley ASDC
  - Multiple products: EBAF, SYN, FLASHFLUX
  - NetCDF format, Python: `xarray`, `netCDF4`

---

## In-situ Observations

### NOAA Integrated Surface Database (ISD)

- **Source**: NOAA National Centers for Environmental Information (NCEI)
- **Citation**: Smith, A., et al. (2011). Improvements to NOAA's historical merged land-ocean surface temperature analysis (1880-2006). Journal of Climate, 24(8), 2283-2296.
- **Content**: Global hourly and synoptic surface observations from 1901 to present, 35,000+ stations
- **Usage**: Weather analysis, climate studies, model validation, air quality
- **How to Use**:
  - Access via NOAA NCEI: https://www.ncei.noaa.gov/products/land-based-station/integrated-surface-database
  - FTP download or web interface
  - Python: `ish_parser`, custom parsers

### GHCN (Global Historical Climatology Network)

- **Source**: NOAA NCEI
- **Citation**: Menne, M.J., et al. (2012). An overview of the Global Historical Climatology Network-Daily database. Journal of Atmospheric and Oceanic Technology, 29(7), 897-910.
- **Content**: Daily temperature, precipitation, and snow from 100,000+ stations worldwide
- **Usage**: Climate analysis, trend detection, extreme weather studies
- **How to Use**:
  - Access via NOAA NCEI
  - GHCN-Daily and GHCN-Monthly versions
  - Python: direct CSV/text file parsing with `pandas`

### AERONET (Aerosol Robotic Network)

- **Source**: NASA/PHOTONS
- **Citation**: Holben, B.N., et al. (1998). AERONET—A federated instrument network and data archive for aerosol characterization. Remote Sensing of Environment, 66(1), 1-16.
- **Content**: Ground-based aerosol optical depth, size distribution, and optical properties from 500+ sites
- **Usage**: Aerosol research, satellite validation, air quality monitoring
- **How to Use**:
  - Access via https://aeronet.gsfc.nasa.gov/
  - Direct download of ASCII files
  - Multiple quality levels (Level 1.0, 1.5, 2.0)

### ARGO Float Data

- **Source**: International Argo Program
- **Citation**: Riser, S.C., et al. (2016). Fifteen years of ocean observations with the global Argo array. Nature Climate Change, 6(2), 145-153.
- **Content**: Temperature and salinity profiles from surface to 2000m depth, global ocean coverage
- **Usage**: Ocean-atmosphere interaction, climate modeling, ocean heat content studies
- **How to Use**:
  - Access via Argo Data Centers or NOAA NCEI
  - Python: `argopy` library
  - NetCDF format

### SURFRAD (Surface Radiation Budget Network)

- **Source**: NOAA
- **Citation**: Augustine, J.A., et al. (2000). SURFRAD—A national surface radiation budget network for atmospheric research. Bulletin of the American Meteorological Society, 81(10), 2341-2357.
- **Content**: High-quality surface radiation measurements at 7 US sites
- **Usage**: Solar energy research, model validation, radiation budget studies
- **How to Use**:
  - Access via NOAA GML: https://gml.noaa.gov/grad/surfrad/
  - ASCII format, direct download
  - Minute-resolution data

---

## Climate Model Data

### CMIP6 (Coupled Model Intercomparison Project Phase 6)

- **Source**: World Climate Research Programme (WCRP)
- **Citation**: Eyring, V., et al. (2016). Overview of the Coupled Model Intercomparison Project Phase 6 (CMIP6) experimental design and organization. Geoscientific Model Development, 9(5), 1937-1958.
- **Content**: Climate model simulations from 100+ models, historical and future scenarios (SSP1-2.6 to SSP5-8.5)
- **Usage**: Climate projections, impact assessments, model evaluation, scenario analysis
- **How to Use**:
  - Access via ESGF nodes: https://esgf-node.llnl.gov/
  - Python: `intake-esm`, `xarray`, `pangeo`
  - Cloud: AWS, Google Cloud

### CORDEX (Coordinated Regional Climate Downscaling Experiment)

- **Source**: WCRP
- **Citation**: Gutowski, W.J., et al. (2016). WCRP COordinated Regional Downscaling EXperiment (CORDEX): a diagnostic MIP for CMIP6. Geoscientific Model Development, 9(11), 4087-4095.
- **Content**: Regional climate model simulations at 12-50 km resolution for 14 domains worldwide
- **Usage**: Regional climate projections, impact studies, high-resolution climate analysis
- **How to Use**:
  - Access via ESGF nodes
  - Regional domains: EUR, NAM, AFR, etc.
  - Python: similar tools as CMIP6

### HighResMIP

- **Source**: CMIP6 endorsed MIP
- **Citation**: Haarsma, R.J., et al. (2016). High Resolution Model Intercomparison Project (HighResMIP v1.0) for CMIP6. Geoscientific Model Development, 9(11), 4185-4208.
- **Content**: High-resolution climate models (25-50 km) for better representation of extremes
- **Usage**: Extreme weather, tropical cyclones, mesoscale processes
- **How to Use**:
  - Access via ESGF
  - Subset of CMIP6 models at higher resolution

---

## Greenhouse Gas Data

### NOAA Global Greenhouse Gas Reference Network

- **Source**: NOAA Global Monitoring Laboratory (GML)
- **Citation**: Dlugokencky, E.J., et al. (2019). Atmospheric methane dry air mole fractions from the NOAA GML carbon cycle cooperative global air sampling network. NOAA GML Data.
- **Content**: CO₂, CH₄, N₂O, SF₆, CO concentrations from 50+ sites globally since 1960s
- **Usage**: Long-term greenhouse gas trends, carbon cycle research, atmospheric chemistry
- **How to Use**:
  - Access via NOAA GML: https://gml.noaa.gov/dv/data/
  - ASCII text files, monthly/annual averages
  - Python: `pandas` for reading

### OCO-2/OCO-3 (Orbiting Carbon Observatory)

- **Source**: NASA
- **Citation**: Crisp, D., et al. (2017). The on-orbit performance of the Orbiting Carbon Observatory-2 (OCO-2) instrument and its radiometrically calibrated products. Atmospheric Measurement Techniques, 10(1), 59-81.
- **Content**: Column-averaged CO₂ concentrations (XCO₂) with high spatial resolution
- **Usage**: Carbon cycle research, emission monitoring, source/sink identification
- **How to Use**:
  - Access via NASA GES DISC
  - Level 2 (retrievals) and Level 3 (gridded) products
  - Python: `h5py`, `netCDF4`

### GOSAT/GOSAT-2

- **Source**: JAXA/NIES/MOE (Japan)
- **Citation**: Kuze, A., et al. (2016). Update on GOSAT TANSO-FTS performance, operations, and data products after more than 6 years in space. Atmospheric Measurement Techniques, 9(6), 2445-2461.
- **Content**: Column CO₂ and CH₄ concentrations from space
- **Usage**: Greenhouse gas monitoring, emission verification, carbon budget studies
- **How to Use**:
  - Access via GOSAT Data Archive Service (GDAS)
  - Registration required
  - HDF5 format

### TCCON (Total Carbon Column Observing Network)

- **Source**: International ground-based network
- **Citation**: Wunch, D., et al. (2011). The Total Carbon Column Observing Network. Philosophical Transactions of the Royal Society A, 369(1943), 2087-2112.
- **Content**: Ground-based Fourier Transform Spectrometer measurements of CO₂, CH₄, CO, N₂O
- **Usage**: Satellite validation, carbon cycle research, greenhouse gas trends
- **How to Use**:
  - Access via https://tccondata.org/
  - NetCDF files
  - Quality-controlled data

---

## Precipitation Data

### CHIRPS (Climate Hazards Group InfraRed Precipitation with Station data)

- **Source**: UC Santa Barbara Climate Hazards Center
- **Citation**: Funk, C., et al. (2015). The climate hazards infrared precipitation with stations—a new environmental record for monitoring extremes. Scientific Data, 2, 150066.
- **Content**: Daily and pentadal precipitation at 0.05° resolution from 1981 to near-present
- **Usage**: Drought monitoring, agriculture, food security, hydrology
- **How to Use**:
  - Access via CHC data portal: https://data.chc.ucsb.edu/products/CHIRPS-2.0/
  - FTP download, direct HTTP
  - Python: `xarray`, `rasterio`
  - Google Earth Engine: `UCSB-CHG/CHIRPS/DAILY`

### TRMM (Tropical Rainfall Measuring Mission)

- **Source**: NASA/JAXA
- **Citation**: Huffman, G.J., et al. (2007). The TRMM multisatellite precipitation analysis (TMPA): Quasi-global, multiyear, combined-sensor precipitation estimates. Journal of Hydrometeorology, 8(1), 38-55.
- **Content**: 3-hourly and daily precipitation for tropics (50°S-50°N), 1998-2015
- **Usage**: Tropical precipitation analysis, monsoon research, flood monitoring
- **How to Use**:
  - Access via NASA GES DISC
  - TMPA 3B42 and 3B43 products
  - Continued by GPM

### GPCC (Global Precipitation Climatology Centre)

- **Source**: Deutscher Wetterdienst (DWD), Germany
- **Citation**: Schneider, U., et al. (2014). GPCC's new land surface precipitation climatology based on quality-controlled in situ data. International Journal of Climatology, 34(11), 2607-2622.
- **Content**: Monthly precipitation from 85,000+ stations, gridded at 0.25° to 2.5°, 1891-present
- **Usage**: Long-term precipitation climatology, trend analysis, model validation
- **How to Use**:
  - Access via GPCC: https://www.dwd.de/EN/ourservices/gpcc/gpcc.html
  - NetCDF format
  - Full Data Reanalysis and Monitoring products

### PERSIANN-CDR

- **Source**: Center for Hydrometeorology and Remote Sensing (CHRS), UC Irvine
- **Citation**: Ashouri, H., et al. (2015). PERSIANN-CDR: Daily precipitation climate data record from multisatellite observations. Bulletin of the American Meteorological Society, 96(1), 69-83.
- **Content**: Daily precipitation at 0.25° resolution, 1983-present
- **Usage**: Climate research, hydrological modeling, trend analysis
- **How to Use**:
  - Access via NOAA NCEI
  - NetCDF format
  - Web interface and bulk download

---

## Temperature Data

### Berkeley Earth Surface Temperature (BEST)

- **Source**: Berkeley Earth
- **Citation**: Rohde, R., et al. (2013). Berkeley Earth temperature averaging process. Geoinformatics & Geostatistics: An Overview, 1(2).
- **Content**: Monthly land and ocean temperature from 1750 to present, gridded at 1° resolution
- **Usage**: Climate change analysis, temperature trends, historical climate reconstruction
- **How to Use**:
  - Access via http://berkeleyearth.org/data/
  - Text and NetCDF formats
  - Free download, open source

### HadCRUT5

- **Source**: Met Office Hadley Centre and University of East Anglia CRU
- **Citation**: Morice, C.P., et al. (2021). An updated assessment of near‐surface temperature change from 1850. Journal of Geophysical Research: Atmospheres, 126(3), e2019JD032361.
- **Content**: Global temperature anomalies from 1850 to present, 5° × 5° grid
- **Usage**: Global temperature monitoring, climate change assessment, IPCC reports
- **How to Use**:
  - Access via Met Office: https://www.metoffice.gov.uk/hadobs/hadcrut5/
  - NetCDF format
  - Ensemble members available

### GISTEMP

- **Source**: NASA Goddard Institute for Space Studies (GISS)
- **Citation**: Lenssen, N.J., et al. (2019). Improvements in the GISTEMP uncertainty model. Journal of Geophysical Research: Atmospheres, 124(12), 6307-6326.
- **Content**: Global surface temperature anomalies from 1880 to present, 2° × 2° grid
- **Usage**: Climate monitoring, temperature trend analysis, climate modeling
- **How to Use**:
  - Access via NASA GISS: https://data.giss.nasa.gov/gistemp/
  - Text and NetCDF formats
  - Monthly and annual means

### OISST (Optimum Interpolation Sea Surface Temperature)

- **Source**: NOAA
- **Citation**: Huang, B., et al. (2021). Improvements of the Daily Optimum Interpolation Sea Surface Temperature (DOISST) version 2.1. Journal of Climate, 34(8), 2923-2939.
- **Content**: Daily global SST at 0.25° resolution from 1981 to present
- **Usage**: Ocean-atmosphere interaction, marine ecosystems, climate monitoring, El Niño tracking
- **How to Use**:
  - Access via NOAA PSL or NCEI
  - NetCDF format
  - Python: `xarray`, OPeNDAP

---

## Wind and Circulation Data

### QuikSCAT/ASCAT

- **Source**: NASA (QuikSCAT) / EUMETSAT (ASCAT)
- **Citation**: Ricciardulli, L., & Wentz, F.J. (2015). A scatterometer geophysical model function for climate-quality winds. Journal of Atmospheric and Oceanic Technology, 32(10), 1829-1846.
- **Content**: Ocean surface wind vectors at 12.5-25 km resolution
- **Usage**: Ocean wind analysis, tropical cyclones, ocean-atmosphere interaction
- **How to Use**:
  - Access via Remote Sensing Systems or NOAA
  - NetCDF/HDF format
  - Python: `netCDF4`, `xarray`

### NCEP/DOE Reanalysis 2 Winds

- **Source**: NOAA NCEP
- **Citation**: Kanamitsu, M., et al. (2002). NCEP–DOE AMIP-II reanalysis (R-2). Bulletin of the American Meteorological Society, 83(11), 1631-1644.
- **Content**: Global wind fields at multiple levels from 1979 to present
- **Usage**: Atmospheric circulation studies, wind energy, climate variability
- **How to Use**:
  - Access via NOAA PSL
  - GRIB or NetCDF format
  - OPeNDAP access available

### 20th Century Reanalysis (20CR)

- **Source**: NOAA-CIRES-DOE
- **Citation**: Compo, G.P., et al. (2011). The twentieth century reanalysis project. Quarterly Journal of the Royal Meteorological Society, 137(654), 1-28.
- **Content**: Global atmospheric circulation from 1836 to 2015 with uncertainty estimates
- **Usage**: Historical climate analysis, circulation trends, long-term variability
- **How to Use**:
  - Access via NOAA PSL
  - Ensemble members available
  - NetCDF format

---

## Ocean-Atmosphere Interaction

### ENSO Indices (Niño 3.4, SOI, MEI)

- **Source**: NOAA Climate Prediction Center, NOAA PSL
- **Citation**: Trenberth, K.E., & Stepaniak, D.P. (2001). Indices of el Niño evolution. Journal of Climate, 14(8), 1697-1701.
- **Content**: El Niño-Southern Oscillation indices from 1950s to present
- **Usage**: ENSO monitoring, seasonal forecasting, climate teleconnections
- **How to Use**:
  - Access via NOAA CPC: https://www.cpc.ncep.noaa.gov/data/indices/
  - Text files, monthly values
  - Python: `pandas` reading

### NAO/AO Indices

- **Source**: NOAA Climate Prediction Center
- **Citation**: Hurrell, J.W., et al. (2003). An overview of the North Atlantic Oscillation. Geophysical Monograph-American Geophysical Union, 134, 1-36.
- **Content**: North Atlantic Oscillation and Arctic Oscillation indices
- **Usage**: Northern Hemisphere climate variability, weather pattern analysis
- **How to Use**:
  - Access via NOAA CPC
  - Monthly indices
  - Text format

### OAFlux (Objectively Analyzed Air-sea Fluxes)

- **Source**: Woods Hole Oceanographic Institution
- **Citation**: Yu, L., & Weller, R.A. (2007). Objectively analyzed air–sea heat fluxes for the global ice-free oceans (1981–2005). Bulletin of the American Meteorological Society, 88(4), 527-540.
- **Content**: Global ocean heat, moisture, and momentum fluxes from 1958 to 2019
- **Usage**: Ocean-atmosphere heat exchange, climate modeling, ocean energetics
- **How to Use**:
  - Access via WHOI OAFlux project
  - NetCDF format
  - Monthly gridded products

### TAO/TRITON (Tropical Atmosphere Ocean Array)

- **Source**: NOAA PMEL
- **Citation**: McPhaden, M.J., et al. (1998). The Tropical Ocean-Global Atmosphere observing system: A decade of progress. Journal of Geophysical Research: Oceans, 103(C7), 14169-14240.
- **Content**: Real-time oceanic and atmospheric observations in tropical Pacific
- **Usage**: El Niño monitoring and forecasting, tropical climate research
- **How to Use**:
  - Access via NOAA PMEL: https://www.pmel.noaa.gov/tao/
  - ASCII and NetCDF formats
  - Daily to hourly data

---

## Aerosol and Air Quality Data

### MERRA-2 Aerosol Reanalysis

- **Source**: NASA GMAO
- **Citation**: Randles, C.A., et al. (2017). The MERRA-2 aerosol reanalysis, 1980 onward. Part I: System description and data assimilation evaluation. Journal of Climate, 30(17), 6823-6850.
- **Content**: Global 3D aerosol distributions (dust, sea salt, sulfate, BC, OC) from 1980 to present
- **Usage**: Aerosol research, air quality modeling, climate impacts of aerosols
- **How to Use**:
  - Access via NASA GES DISC
  - Multiple collections (tavg1_2d_aer_Nx, etc.)
  - NetCDF/HDF5 format

### CAMS (Copernicus Atmosphere Monitoring Service)

- **Source**: ECMWF
- **Citation**: Inness, A., et al. (2019). The CAMS reanalysis of atmospheric composition. Atmospheric Chemistry and Physics, 19(6), 3515-3556.
- **Content**: Global atmospheric composition including greenhouse gases, aerosols, reactive gases
- **Usage**: Air quality forecasting, atmospheric composition monitoring, emission assessment
- **How to Use**:
  - Access via Copernicus ADS: https://ads.atmosphere.copernicus.eu/
  - API: `cdsapi`
  - Near-real-time and reanalysis products

### EPA Air Quality System (AQS)

- **Source**: U.S. Environmental Protection Agency
- **Citation**: EPA Air Quality System Data Mart
- **Content**: Criteria pollutants (PM2.5, PM10, O₃, NO₂, SO₂, CO) from thousands of US monitoring sites
- **Usage**: Air quality assessment, regulatory compliance, health impact studies
- **How to Use**:
  - Access via EPA AQS Data Mart: https://www.epa.gov/aqs
  - API available
  - Download pre-generated files or query database

### OpenAQ

- **Source**: OpenAQ Community
- **Citation**: OpenAQ: Fighting Air Inequality Through Open Data
- **Content**: Real-time and historical air quality data from 12,000+ locations in 100+ countries
- **Usage**: Global air quality monitoring, research, public health
- **How to Use**:
  - Access via OpenAQ API: https://openaq.org/
  - Python: `py-openaq`
  - JSON format, real-time access

---

## Cryosphere Data

### NSIDC Sea Ice Index

- **Source**: National Snow and Ice Data Center (NSIDC)
- **Citation**: Fetterer, F., et al. (2017). Sea Ice Index, Version 3. NSIDC: National Snow and Ice Data Center, Boulder, Colorado USA.
- **Content**: Sea ice extent and concentration for Arctic and Antarctic from 1978 to present
- **Usage**: Sea ice trends, climate change monitoring, polar research
- **How to Use**:
  - Access via NSIDC: https://nsidc.org/data/seaice_index/
  - GeoTIFF, PNG, NetCDF formats
  - Monthly and daily products

### PIOMAS (Pan-Arctic Ice Ocean Modeling and Assimilation System)

- **Source**: Polar Science Center, University of Washington
- **Citation**: Zhang, J., & Rothrock, D.A. (2003). Modeling global sea ice with a thickness and enthalpy distribution model. Journal of Physical Oceanography, 33(11), 2491-2515.
- **Content**: Arctic sea ice volume and thickness from 1979 to present
- **Usage**: Sea ice volume trends, Arctic climate research
- **How to Use**:
  - Access via PSC: http://psc.apl.uw.edu/research/projects/arctic-sea-ice-volume-anomaly/
  - Text and NetCDF formats

### MODIS Snow Cover

- **Source**: NASA
- **Citation**: Hall, D.K., & Riggs, G.A. (2016). MODIS/Terra Snow Cover Daily L3 Global 500m Grid, Version 6.
- **Content**: Daily global snow cover at 500m resolution from 2000 to present
- **Usage**: Hydrological modeling, snow monitoring, climate research
- **How to Use**:
  - Access via NASA Earthdata or NSIDC
  - HDF-EOS format
  - Google Earth Engine: `MODIS/006/MOD10A1`

### GRACE/GRACE-FO

- **Source**: NASA/DLR
- **Citation**: Tapley, B.D., et al. (2004). GRACE measurements of mass variability in the Earth system. Science, 305(5683), 503-505.
- **Content**: Changes in Earth's gravity field reflecting water mass changes including ice sheets
- **Usage**: Ice mass balance, groundwater depletion, sea level research
- **How to Use**:
  - Access via NASA JPL or GFZ Potsdam
  - Multiple processing centers (CSR, JPL, GFZ)
  - NetCDF format

### GLIMS (Global Land Ice Measurements from Space)

- **Source**: NSIDC/USGS
- **Citation**: Raup, B., et al. (2007). The GLIMS geospatial glacier database. Journal of Glaciology, 53(182), 372-376.
- **Content**: Glacier outlines and changes from satellite observations worldwide
- **Usage**: Glacier monitoring, climate change impacts, water resources
- **How to Use**:
  - Access via GLIMS viewer: https://www.glims.org/
  - Shapefile and other GIS formats

---

## Radiation Data

### CERES Energy Balanced and Filled (EBAF)

- **Source**: NASA Langley
- **Citation**: Loeb, N.G., et al. (2018). Clouds and the Earth's Radiant Energy System (CERES) Energy Balanced and Filled (EBAF) top-of-atmosphere. Journal of Climate, 31(2), 895-918.
- **Content**: Top-of-atmosphere and surface radiation fluxes, monthly 1° grid from 2000-present
- **Usage**: Earth's energy budget, climate model evaluation, radiation research
- **How to Use**:
  - Access via NASA Langley ASDC
  - NetCDF format
  - TOA and surface editions

### SolCast/NSRDB (National Solar Radiation Database)

- **Source**: NREL (National Renewable Energy Laboratory)
- **Citation**: Sengupta, M., et al. (2018). The National Solar Radiation Data Base (NSRDB). Renewable and Sustainable Energy Reviews, 89, 51-60.
- **Content**: Solar radiation (DNI, DHI, GHI) for US and selected regions, 1998-present
- **Usage**: Solar energy applications, renewable energy assessment
- **How to Use**:
  - Access via NREL: https://nsrdb.nrel.gov/
  - API and bulk download
  - Python: `nrel-pysam`

### ISCCP (International Satellite Cloud Climatology Project)

- **Source**: NASA/NOAA
- **Citation**: Rossow, W.B., & Schiffer, R.A. (1999). Advances in understanding clouds from ISCCP. Bulletin of the American Meteorological Society, 80(11), 2261-2288.
- **Content**: Cloud properties and radiative fluxes from 1983 to 2009
- **Usage**: Cloud climatology, radiation budget, cloud-climate feedback
- **How to Use**:
  - Access via ISCCP website or NOAA NCEI
  - Multiple products (D1, D2, H-series)

---

## Extreme Weather Data

### EM-DAT (Emergency Events Database)

- **Source**: CRED (Centre for Research on the Epidemiology of Disasters)
- **Citation**: Guha-Sapir, D., Below, R., & Hoyois, P. EM-DAT: International Disaster Database. Université Catholique de Louvain, Brussels, Belgium.
- **Content**: Global disaster events (floods, droughts, storms, etc.) from 1900 to present
- **Usage**: Disaster risk assessment, climate impacts, economic loss analysis
- **How to Use**:
  - Access via https://www.emdat.be/
  - Registration required
  - Excel/CSV export

### IBTrACS (International Best Track Archive for Climate Stewardship)

- **Source**: NOAA NCEI
- **Citation**: Knapp, K.R., et al. (2010). The International Best Track Archive for Climate Stewardship (IBTrACS). Bulletin of the American Meteorological Society, 91(3), 363-376.
- **Content**: Global tropical cyclone tracks from 1842 to present
- **Usage**: Tropical cyclone research, climate variability, risk assessment
- **How to Use**:
  - Access via NOAA NCEI: https://www.ncdc.noaa.gov/ibtracs/
  - NetCDF, CSV, shapefile formats
  - Python: `xarray`, `geopandas`

### SPEI Global Drought Monitor

- **Source**: Spanish National Research Council (CSIC)
- **Citation**: Vicente-Serrano, S.M., et al. (2010). A multiscalar drought index sensitive to global warming. Journal of Climate, 23(7), 1696-1718.
- **Content**: Standardized Precipitation-Evapotranspiration Index (SPEI) globally, 1901-present
- **Usage**: Drought monitoring and analysis, agricultural impacts, water resources
- **How to Use**:
  - Access via https://spei.csic.es/database.html
  - NetCDF format, multiple timescales (1-48 months)

### NOAA Storm Events Database

- **Source**: NOAA NCEI
- **Citation**: NOAA National Centers for Environmental Information, Storm Events Database
- **Content**: Severe weather events in the US from 1950 to present
- **Usage**: Severe weather climatology, damage assessment, forecasting research
- **How to Use**:
  - Access via NOAA NCEI: https://www.ncdc.noaa.gov/stormevents/
  - CSV bulk download or web query

---

## Paleoclimate Data

### NOAA Paleoclimatology Database

- **Source**: NOAA NCEI
- **Citation**: NOAA National Centers for Environmental Information, Paleoclimatology Data
- **Content**: Ice cores, tree rings, corals, sediments, pollen spanning thousands to millions of years
- **Usage**: Past climate reconstruction, climate variability, climate change context
- **How to Use**:
  - Access via https://www.ncei.noaa.gov/products/paleoclimatology
  - Multiple data types and formats
  - Individual dataset citations required

### PAGES 2k Network

- **Source**: Past Global Changes (PAGES) Project
- **Citation**: PAGES 2k Consortium (2017). A global multiproxy database for temperature reconstructions of the Common Era. Scientific Data, 4, 170088.
- **Content**: Temperature reconstructions for the past 2000 years from multiple proxies
- **Usage**: Climate variability, pre-industrial climate, model-data comparison
- **How to Use**:
  - Access via NOAA NCEI or PAGES website
  - Text and NetCDF formats

### LiPD (Linked Paleo Data)

- **Source**: LinkedEarth Project
- **Citation**: McKay, N.P., & Emile-Geay, J. (2016). Technical note: The Linked Paleo Data framework. Climate of the Past, 12(4), 1093-1100.
- **Content**: Standardized format for paleoclimate data with linked metadata
- **Usage**: Paleoclimate data integration, meta-analysis, data discovery
- **How to Use**:
  - Access via http://lipd.net/
  - Python: `pylipd`
  - JSON-LD format

---

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

To add a new dataset:
1. Fork this repository
2. Add your dataset following the format above (Name, Source, Citation, Content, Usage, How to Use)
3. Submit a pull request

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related rights to this work.

## Acknowledgments

This list is maintained by the community. Thanks to all contributors and the data providers who make their datasets openly available for research and applications.

---

**Last Updated**: 2025

For questions, suggestions, or corrections, please open an issue or submit a pull request.
