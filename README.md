# London council housing map

An interactive map of London's 4,994 neighbourhoods (2021 LSOAs) showing council and social housing, deprivation and recorded crime.

Live site: https://semiman.github.io/london-council-housing/

## Data
- **Council and social housing**: ONS Census 2021, table TS054 (tenure), via Nomis.
- **Deprivation**: English Indices of Deprivation 2025 (MHCLG), File 7. Includes the crime domain.
- **Council estates and buildings**: published by the councils themselves. Lambeth (building footprints, ArcGIS open data), Camden (large housing estates, with home counts), Hackney (estate boundaries, Hackney GeoServer), Hounslow and Wandsworth (estate boundaries, ArcGIS). The other 28 boroughs don't publish this, and OpenStreetMap barely tags council housing, so they show none.
- **Recorded crime**: Metropolitan Police LSOA-level crime, most recent 24 months, via the London Datastore. The map uses the latest 12 months (Oct 2025 to Sep 2026). City of London is policed by City of London Police and has no figures here.
- **Street-level crimes** (on demand, live): data.police.uk API, latest month.
- **Boundaries**: ONS LSOA December 2021 BGC, simplified. Contains OS data © Crown copyright and database right.
- **Basemap**: © OpenStreetMap contributors; optional grey basemap © Esri.

Crime per 1,000 residents runs high in town centres and transport hubs, where many visitors but few residents are counted.

`data/lsoa.geojson` holds per-area fields: `pla` % renting from council, `pso` % all social rent, `imd` IMD decile, `crd` crime-domain decile, `cr` crimes per 1,000 residents, `cg` crimes by type.
