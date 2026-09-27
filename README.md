# Subject-specific biliary-tree geometry

Public geometry-only release for the reproducible biliary-tree workflow.

This repository separates the reusable anatomical resource from the broader Three.js development repository. It contains a subject-specific biliary-tree surface/mesh asset, a liver-surface asset, the original `FLOW.exnode`/`FLOW.exelem` one-dimensional source files, and metadata needed to identify the files without treating unresolved scalar fields as physiological measurements.

## Contents

- `data/libzinc-json/S01_bile_1.json`: biliary-tree geometry exported from LibZinc/Three.js-compatible JSON.
- `data/libzinc-json/S01_surface_1.json`: corresponding liver-surface geometry.
- `data/libzinc-json/*_view.json`: legacy camera/view metadata for the two JSON assets.
- `data/exnode-exelem/FLOW.exnode`: original nodal coordinates and stored fields.
- `data/exnode-exelem/FLOW.exelem`: original element connectivity and Hermite data.
- `metadata/geometry_manifest.json`: file roles, provenance, and unit status.

## Important data-status note

The source metadata do not identify a reliable coordinate unit, radius unit, flow unit, speed unit, subject identifier, imaging acquisition protocol, or solver boundary-condition record. The FLOW scalar fields must therefore be treated as unresolved source fields, not as calibrated mL/min, cm/s, pressure, or validated physiological predictions. The geometry is released for visualization, topology inspection, mesh conversion, and reproducible method development.

The `S01_*` JSON assets are retained in their original LibZinc export format so that they can be loaded by compatible viewers. The `FLOW.exnode`/`FLOW.exelem` pair is retained as the original one-dimensional source representation used in the accompanying methods paper.

## Provenance

The S01 assets were identified in the public repository [`hwe001/hyu754.github.io`](https://github.com/hwe001/hyu754.github.io), under `models/`. This repository is a focused redistribution for the biliary-tree geometry resource. The original viewer repository and its license should be cited alongside this release.

## Suggested citation

Ho H, Bartlett A, Jalu M. Subject-specific biliary-tree geometry and liver-surface resource. Public data repository. Release 1.0.

## License

See `LICENSE`. Users should also review the provenance and licensing terms of the original source repository before redistributing modified derivatives.
