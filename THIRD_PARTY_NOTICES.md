# Third-Party Notices

This repository is published under the MIT license. The third-party libraries
that are directly imported by the application or its runtime support code use
permissive licenses as well.

This is a practical compatibility note for the repository, not legal advice.
Each third-party package keeps its own license terms, copyright notices, and
any attribution requirements.

## Runtime Libraries Imported By This Project

| Package | License | Notes |
| --- | --- | --- |
| `streamlit` | Apache-2.0 | Permissive. Keep Apache license and notice obligations when redistributing the package itself. |
| `streamlit-folium` | MIT | Permissive. |
| `folium` | MIT | Permissive. |
| `branca` | MIT | Permissive. Imported directly in `src/mapview.py`. |
| `requests` | Apache-2.0 | Permissive. Keep Apache license and notice obligations when redistributing the package itself. |
| `astral` | Apache-2.0 | Permissive. |
| `python-dotenv` | BSD-3-Clause | Permissive. |
| `tzdata` | Apache-2.0 | Permissive. Windows-only runtime dependency in this project. |

## Development Dependencies

| Package | License | Notes |
| --- | --- | --- |
| `pytest` | MIT | Permissive. Test-only dependency. |
| `ruff` | MIT | Permissive. Lint/format dependency. |
| `pyright` | MIT | Permissive. Type-checking dependency. |
| `setuptools` | MIT | Permissive. Build dependency. |

## Map Data And Public Services

These defaults are used at runtime and are not vendored in the repository.
They keep their own terms; this is a practical summary, not legal advice.

| Source | Terms | Notes |
| --- | --- | --- |
| OpenStreetMap data | [ODbL](https://opendatacommons.org/licenses/odbl/) | © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright). Attribution required; share-alike can apply if you extract, store, or redistribute substantial OSM data. |
| Nominatim (geocoding) | [Nominatim usage policy](https://operations.osmfoundation.org/policies/nominatim/) | Public instance is for light/demo use. Identify your app with a contactable `User-Agent`. Prefer self-hosted or commercial geocoding for heavier traffic. |
| OSRM (routing) | Project demo / self-host terms | Default `router.project-osrm.org` is a public demo, not for production. Self-host or use a supported provider when traffic grows. Route geometry may derive from OSM (ODbL). |
| OpenStreetMap tiles | OSM tile [usage policy](https://operations.osmfoundation.org/policies/tiles/) + ODbL attribution | Folium `tiles="OpenStreetMap"` loads public OSM-style tiles. Keep the Leaflet attribution control visible; do not hide credits with CSS. |

## Summary

All direct runtime libraries currently imported by the project use permissive
licenses that are commonly compatible with distributing this repository under
MIT.

The main extra point to remember is that Apache-2.0 packages are still
permissive but carry their own attribution and notice requirements when you
redistribute those packages or substantial bundled copies of them.

Separately, OpenStreetMap-derived data and public Nominatim/OSRM/tile services
require attribution and fair-use compliance even though this repository's own
code remains MIT.
