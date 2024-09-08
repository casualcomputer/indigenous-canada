# Extracting Designated Places and Census Subdivisions for Métis, Inuit, and First Nations Communities (2021 Census)

This documentation outlines the process used to extract the designated places and Census subdivisions from the 2021 Census data to produce GeoJSON files representing the boundaries of Métis, Inuit, and First Nations communities.

## Overview

The goal of this project was to create GeoJSON files that delineate the boundaries of communities for Métis, Inuit, and First Nations using data from the 2021 Census. The extracted boundaries are used to create three separate GeoJSON files, one for each community type. This documentation provides details on the extraction process, the data sources, and the steps taken to generate these GeoJSON files.

## Data Sources

1. **Indigenous Population Profile, 2021 Census of Population:**

   - Designated places and Census subdivisions were identified using the Indigenous Population Profile from the 2021 Census of Population.
   - Métis settlements, Inuit regions, and First Nations reserves were defined using these designated places and Census subdivisions.

2. **Shapefiles:**
   - Shapefiles containing geographical boundaries for the designated places and Census subdivisions were used to create GeoJSON files.

## Métis Settlements

Métis Settlements are included within this profile and are defined using designated places. The Alberta Métis Settlement Act of 1990 legally established the Métis Settlements General Council, along with eight settlement corporations. There are 10 Métis settlements in northern Alberta:

- Gift Lake Part A
- Gift Lake Part B
- Kikino Part A
- Kikino Part B
- Paddle Prairie
- Buffalo Lake
- Elizabeth
- Fishing Lake
- East Prairie
- Peavine

## Inuit Regions

Inuit communities are defined using specific Census subdivisions that represent Inuit Nunangat, which includes the following regions:

- **Inuvialuit Settlement Region**
- **Nunatsiavut**
- **Nunavik**
- **Nunavut**

Each of these regions corresponds to specific Census subdivisions as outlined in the "List of Inuit regions and the census subdivisions they include" HTML file.

## First Nations Communities

First Nations communities are represented by specific designated places and Census subdivisions. These areas are generally associated with First Nations reserves, Indian bands, or tribal council areas. The communities were identified using:

- Designated places that align with First Nations reserves.
- Census subdivisions that include First Nations reserves and settlements.

The specific subdivisions are detailed in the "List of First Nation or Indian band and Tribal Council areas and the census subdivisions_designated places they include" HTML file.

## Extraction Process

### Step 1: Extracting Designated Places and Census Subdivisions

- The R script (`get_DGUID.R`) was used to extract the relevant designated places and Census subdivisions from the 2021 Census data.
- The script reads in the shapefiles and processes them to extract the specific designated places and Census subdivisions associated with Métis, Inuit, and First Nations communities.

### Step 2: Filtering Data for Métis, Inuit, and First Nations

- The designated places and Census subdivisions were filtered to create separate datasets for Métis, Inuit, and First Nations communities.
- The filtering was done based on the specific designated places and subdivisions defined in the provided HTML files:
  - **Métis Settlements:** Filtered based on the 10 settlements listed above.
  - **Inuit Regions:** Filtered using the specific subdivisions outlined in the "List of Inuit regions and the census subdivisions they include" HTML file.
  - **First Nations Communities:** Filtered using the subdivisions listed in the "List of First Nation or Indian band and Tribal Council areas and the census subdivisions_designated places they include" HTML file.

### Step 3: Generating GeoJSON Files

- The filtered datasets were converted into GeoJSON format using the R script.
- Three separate GeoJSON files were created, representing the boundaries for Métis, Inuit, and First Nations communities.

## Outputs

The outputs of this process are three GeoJSON files, each representing the geographical boundaries for:

1. **Métis Communities:** Includes all designated places within the 10 settlements defined in northern Alberta.
2. **Inuit Communities:** Includes all relevant subdivisions as defined in the provided HTML documentation.
3. **First Nations Communities:** Includes all relevant subdivisions and designated places as defined in the provided HTML documentation.

## Citation

**Catalogue Number:** 98-510-X2021001

> Statistics Canada. 2023. _Indigenous Population Profile. 2021 Census of Population_. Statistics Canada Catalogue number 98-510-X2021001. Ottawa. Released June 21, 2023.  
> [https://www12.statcan.gc.ca/census-recensement/2021/dp-pd/ipp-ppa/index.cfm?Lang=E](https://www12.statcan.gc.ca/census-recensement/2021/dp-pd/ipp-ppa/index.cfm?Lang=E) (accessed September 7, 2024).

## Terminology Note

The term "Indigenous" replaced "Aboriginal" when referring to the collective term for people who identify as First Nations, Métis, or Inuit. Its usage aligns with the Government of Canada and is coherent with standard terminology used in the United Nations Declaration on the Rights of Indigenous Peoples.

## Usage

The resulting GeoJSON files can be used in various GIS applications for mapping and analysis of Métis, Inuit, and First Nations community boundaries.

## Contact

For any questions or further assistance, please contact henry.data.io.20@hotmail.com!
