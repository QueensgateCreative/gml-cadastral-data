# GML Data Files

This folder contains Land Registry GML cadastral parcel data files.

## File Format
- **Format:** GML (Geography Markup Language)
- **Coordinate System:** British National Grid (EPSG:27700)
- **Source:** Land Registry

## Usage
These files are processed by the SALA GML import pipeline to create property boundary polygons for mapping and address matching.

## File Naming Convention
- `Land_Registry_Cadastral_Parcels_[AREA].gml`
- Example: `Land_Registry_Cadastral_Parcels_London.gml`

## Processing Pipeline
1. GML files are uploaded to this repository
2. SALA's serverless function fetches files via GitHub raw URLs
3. Files are parsed and polygons are extracted
4. Coordinates are transformed from BNG (EPSG:27700) to WGS84 (EPSG:4326)
5. Data is stored in Supabase with PostGIS for mapping

## Raw URL Access
Files can be accessed via GitHub raw URLs:
- `https://raw.githubusercontent.com/QueensgateCreative/gml-cadastral-data/main/data/[filename].gml`
