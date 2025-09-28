## NITC Campus OSM Scene Setup

This guide walks you through opening the `base_osm_model.blend` scene. Follow the steps in order the first time you configure the project.

---

## 1. Prerequisites

- **Blender 4.0 or newer** – earlier versions may miss geometry nodes or material features used in the scene.
- [Blosm](https://gumroad.com/l/Blosm) makes OSM imports quicker, but the scene already includes prepared data if you prefer to skip add-ons.

> 💡 Keep the folder structure unchanged. Texture, asset, and OSM links rely on paths relative to the project root.

---

## 2. Repository Layout

| Folder/File                           | Purpose                                                                                     |
| ------------------------------------- | ------------------------------------------------------------------------------------------- |
| `base_osm_model.blend`                | Main Blender file with campus base mesh and references to assets/materials.                 |
| `assets/`                             | Library of building materials, vegetation, packaged assets, and metadata used by the scene. |
| `osm_data/osm/map.osm`                | Raw OpenStreetMap extract for the campus region.                                            |
| `osm_data/3d_tiles/google/`           | Offline Google photogrammetry tiles (optional reference).                                   |
| `overlay/.../tile/{z}/{y}/{x}`        | Aerial basemap tiles for viewport background images.                                        |
| `osm_data/terrain/N11E075.hgt.gz`     | SRTM heightmap covering Kozhikode/NITC area.                                                |
| `assets/default/asset_info/*.json`    | Metadata describing available building profiles and vegetation proxies.                     |
| `assets/default/style/building/*.pml` | Procedural material and style rules for various building categories.                        |

---

## 3. Opening the Base Scene

1. Launch Blender.
2. Use **File → Open…** and select `base_osm_model.blend` in the repository root.
3. When prompted to **Load UI**, keep it _enabled_ to get the prepared workspace layout.
4. Save a copy as `base_osm_model_working.blend` (recommended) so you always have the pristine source.

### Linked Libraries

The file references resources within `assets/`. If Blender shows missing data-blocks:

- Go to **File → External Data → Find Missing Files…** and point Blender to the project root folder.
- Enable **File → External Data → Automatically Pack Resources** if you plan to move the working `.blend` elsewhere.
