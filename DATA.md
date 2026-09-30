# Local input data

The raw source files are intentionally not published. To rerun the notebook, place these files in the repository root:

| Input | Purpose |
|---|---|
| `Education-services-with-station-access_loc.csv` | Service records, approval dates, ratings, activity flags, geometry and recorded bus/train distances |
| `SOS_2021_AUST_GDA2020.shp`, `.shx`, `.dbf`, `.prj` | ABS 2021 Section of State boundaries used for spatial matching |
| `australia_states.geojson` | State geometry for the overview map |
| `ABS Birth estimation.xlsx` | Birth-cohort table used by the estimated-demand section |

The original service CSV is a supplied/enriched input. Its complete station inventory, route availability and redistribution terms have not been established in this project; no claim of comprehensive public-transport coverage is made. ABS geographic and birth-derived inputs should be obtained from their provider under the applicable terms. This package includes published chart results rather than a replacement raw dataset.

Refer to each notebook section for its own date restrictions, missing-value handling and denominator. Source records can change over time; the published charts are a saved analysis snapshot.
