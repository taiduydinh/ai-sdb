# Consolidated VOSviewer term map

This package reconstructs the existing 88-term VOSviewer map as a 73-term map by consolidating true abbreviations, full forms, and orthographic variants. It does not rerun term extraction from the RIS file, so the original layout is preserved as closely as possible.

## Open directly in VOSviewer

- **VOSviewer Online:** choose **Open** and upload `VOSviewer_network_consolidated.json`.
- **VOSviewer desktop:** choose the option to open a VOSviewer map and network, then select `VOSviewer_map_consolidated.csv` and `VOSviewer_network_consolidated.csv`.

The JSON file is the simplest direct-open option. The selected-term list and thesaurus are not needed to open the reconstructed map.

## Conservative consolidation decisions

| Preferred label | Consolidated source labels |
|---|---|
| apnea-hypopnea index (AHI) | `ahi`, `apnea hypopnea index`, `apneahypopnea index` |
| convolutional neural network (CNN) | `cnn`, `convolutional neural network` |
| electrocardiogram (ECG) | `ecg`, `ecg signal`, `electrocardiogram` |
| electroencephalogram (EEG) | `eeg`, `eeg signal` |
| heart rate variability (HRV) | `heart rate variability`, `hrv` |
| obstructive sleep apnea (OSA) | `obstructive sleep apnea`, `osa`, `osas` |
| OSA detection | `obstructive sleep apnea detection`, `osa detection` |
| obstructive sleep apnea-hypopnea syndrome (OSAHS) | `obstructive sleep apnea hypopnea syndrome`, `osahs` |
| polysomnography (PSG) | `polysomnography`, `psg` |
| sleep apnea detection | `sa detection`, `sleep apnea detection` |
| sleep-disordered breathing (SDB) | `sdb`, `sleep disordered breathing` |
| support vector machine (SVM) | `support vector machine`, `svm` |

Related but non-equivalent concepts were deliberately left separate. In particular, `sleep apnea` was not merged with `obstructive sleep apnea (OSA)`, and OSAHS, SAHS, and SAS remain distinct labels. Task terms such as OSA diagnosis and OSA screening also remain separate from the disease name.

## Reconstruction method

- Occurrence counts were summed across merged source nodes.
- Coordinates and average publication year were combined using occurrence-weighted means.
- The cluster with the largest combined occurrence weight was retained.
- Link strengths between merged nodes and all other nodes were summed; self-links created by consolidation were removed.
- Link counts and total link strengths were recalculated from the reconstructed network.
- The relevance score in `selected_terms_consolidated.txt` is an occurrence-weighted summary of the exported source scores. It is included for auditability and is not required when opening the map.

## Rebuilding later from the RIS source

If the map is recreated from bibliographic text in VOSviewer, supply `VOSviewer_thesaurus_consolidated.txt` at the thesaurus/data-cleaning step. A full rebuild may produce a somewhat different layout because VOSviewer will recalculate term selection, normalization, clustering, and coordinates.

## Validation summary

- Source items: 88
- Consolidated items: 73
- Source links: 2967
- Consolidated links: 2101
- Source map SHA-256: `f69c0f5c11fc6b946e6d97ff79a21be7ccef080e228bf9697b1799fb88f74655`
- Source network SHA-256: `75e51b27d0106e0d5e00c2470c88bb06f5ce6b33ce3d8e6c59cc71c570c53cda`
- Source JSON SHA-256: `70dc8e8e1b730eeb2ef439640708e6c92c5e2c35633b70f7c8c10bda942a204e`

Official file-format references: https://app.vosviewer.com/docs/file-types/map-and-network-file-type/ and https://app.vosviewer.com/docs/file-types/json-file-type/
