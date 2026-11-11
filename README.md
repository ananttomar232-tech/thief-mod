# Secret City Heist: 5 Forbidden Items — Fabric 1.20.1 mod generator

`build_mod.py` generates the complete Fabric 1.20.1 (Java 17, official Mojang mappings) mod workspace:
Gradle/Loom setup with wrapper, all Java sources, resources, textures, procedural 3D models, sounds and voice lines.

```bash
python3 build_mod.py                 # -> ./SecretCityHeist/
cd SecretCityHeist && ./gradlew build  # -> build/libs/heistmod-fabric-1.0.0.jar
```

Options: `--out DIR`, `--models DIR` (default: `source_models/` next to the script), `--build`, `--sync-assets`, `--clean`.

`source_models/` holds the supplied Sketchfab glTF models (CC-BY 4.0, see `CREDITS.md`), one folder per mod model id:
`chingam_grappler`, `bhootiya_chaddar`, `bermuda_thaila`, `havaldar_cap`. Any folder you add there (glTF or GLB)
whose name matches an item id replaces that item's model on the next run.

The generated workspace has its own README with gameplay, commands and the asset drop-in conventions.
