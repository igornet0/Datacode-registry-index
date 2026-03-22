# Datacode library registry index

This repository holds **links and metadata** for Datacode library packages: names, sources (repository URLs), descriptions, and Datacode version requirements. Library source code is not stored here—only the index that tools use to discover and wire up packages.

**This documentation is also available in [Russian](README.md).**

## `config.json`

The root index file is `config.json`. Its structure:

| Field | Description |
|-------|-------------|
| `version` | Index schema version (integer). |
| `packages` | Array of package records. |

Each `packages` entry may include:

| Field | Description |
|-------|-------------|
| `name` | Package name (identifier in the Datacode ecosystem). |
| `source` | Source URI, typically a Git URL as `git+https://...`. |
| `description` | Short description and, if needed, build steps or where to place artifacts. |
| `min_datacode` | Minimum compatible Datacode version (e.g. `>=2.0.0`). |

## Adding or updating a package

1. Edit `config.json`: append an object to `packages` or update an existing one.
2. Write a clear `description` so users know how to build or integrate the library.
3. Submit your changes via a pull request to this repository.

## License and contributions

The index data is intended for use with Datacode. Licensing of individual libraries is defined in their own repositories.
