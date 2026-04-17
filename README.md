# Network Data Analysis Coursework
**King's College London | 2025-26**

**Student:** Rutuja Patil | **K-Number:** K25054456

## Repository Structure
├── PART1_wikidata_network_analysis.ipynb  # Part 1 notebook
├── PART2_leeds_road_network.ipynb         # Part 2 notebook
├── data/
│   ├── BOT_REQUESTS.csv
│   ├── USERS.csv
│   ├── REQUEST_FOR_DELETION.csv
│   └── 2009.csv ... 2016.csv             # Leeds accident data
├── figures/                               
└── Coursework_instructions_26.pdf

## Part 1 — Wikidata Editor Network Analysis

Constructs and analyses three Wikidata Talk-page 
co-commenting networks of varying scale:
- **BOT_REQUESTS** (552 nodes, small)
- **USERS** (11,387 nodes, medium)  
- **REQUEST_FOR_DELETION** (9,935 nodes, large)

**Key findings:**
- All three are strongly small-world networks 
  (σ = 52, 1388, 1275)
- Heavy-tailed degree distributions consistent 
  with scale-free topology
- SIR epidemic model applied to troll propagation
  with priority list for monitoring

## Part 2 — Leeds Road Network Analysis

Analyses the Leeds city centre drive network and 
road accident data (2009-2016):
- 264 nodes, 446 edges, non-planar (Inner Ring Road)
- 837 accidents, Moran's I = 0.226 (p=0.010)
- Node-network Voronoi diagram with 4 marathon zones
- Valid ~42km circular routes found in all 4 cells

## Requirements

```bash
pip install networkx osmnx geopandas spaghetti 
            libpysal esda pointpats pyproj 
            matplotlib pandas numpy scipy
```

## How to Run

1. Clone the repository
2. Place data files in the `data/` directory
3. Open notebooks in Jupyter and run all cells
4. All figures are saved automatically to `figures/`

## Data Sources

- Wikidata Talk-page CSV files (provided)
- Leeds City Council road accident data 2009-2016:
  https://data.gov.uk/dataset/6efe5505-941f-45bf-b576-4c1e09b579a1
- OpenStreetMap via osmnx

