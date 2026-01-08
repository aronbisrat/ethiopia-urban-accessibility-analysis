# Ethiopia Population & Density Analysis

## Project Overview
This project analyzes Ethiopia’s population distribution and density at the Woreda and Region levels using resampled WorldPop data. It highlights demographic patterns and provides recruiter‑friendly visualizations.

## Data Sources
- WorldPop 100m raster (resampled to 1km)
- Ethiopia administrative boundaries (Woreda shapefiles)

## Methodology
- Resampled raster for computational feasibility
- Zonal statistics (population sum, mean density per Woreda)
- Regional aggregation for summaries
- Visualizations (bar charts, choropleths with labels)

## Results

### Total Population by Region
![Total Population by Region](assets/images/total_population_by_region(Ethiopia).png)

### Population by Region
![Population by Region](assets/images/population_by_region(ethiopia).png)

### Population Density by Region
![Population Density by Region](assets/images/population_density_by_region(ethiopia).png)

### Population Density by Woreda
![Population Density by Woreda](assets/images/population_density_by_region.png)
## Key Insights
- Regions X and Y show the highest total populations.
- Woredas A and B have the highest densities.
- Density patterns reveal urban concentration but also highlight rural spread.

## Next Steps
Future work will expand into a multi‑factor Urban Accessibility Index, incorporating:
- Service reach (health, education, markets, transport hubs)
- Mobility friction (road density, terrain slope, congestion proxies)
- Demand pressure (population‑to‑service ratios)