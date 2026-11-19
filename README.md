# HIRO Client — Fabric 1.21.11

This repository contains the Java and Fabric metadata files from **HIRO Client Complete Edition**, separated into their matching project paths, plus Gradle/GitHub Actions build configuration.

## Requirements
- Java JDK 21
- Minecraft Java Edition 1.21.11
- Fabric Loader and Fabric API

## Build on GitHub
1. Create a new empty GitHub repository.
2. Upload the contents of this folder (not the outer ZIP folder).
3. Open the **Actions** tab and enable workflows if GitHub asks.
4. Push/commit the files. The workflow named **Build HIRO Client** runs `gradle build`.
5. When it finishes, open the workflow run and download the artifact named `HIRO-Client-Fabric-1.21.11`.

## Build locally
Run:

```bash
gradle build
```

The output JAR is created in `build/libs/`.

## Important status
The Java source files are separated from the supplied Markdown without redesigning their logic. The Gradle setup targets Minecraft 1.21.11 with official Mojang mappings and Java 21. **A successful build has not been verified in this environment.** The first GitHub Actions run may reveal Minecraft/Fabric API signature changes in the supplied Java code; if it fails, share the Actions error log so the exact source files can be corrected.

Some modules listed in the GUI are currently only registered/toggled; the source does not yet implement every named feature.
