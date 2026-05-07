# Bridging the Annotation Gap: Temporally Grounded Egocentric Action Annotations for Nymeria and AEA

This repository contains structured, temporally grounded action annotations for clips from the **Nymeria** and **Aria Everyday Activities (AEA)** egocentric datasets.

The release contains **two CSV files only**:

- `nymeria_annotations.csv`
- `aea_annotations.csv`

The annotations are mapped to a shared **30-class daily-life action taxonomy (8 macro-categories)** and include temporal boundaries, action counts, and review-level scores.

This repository contains **derived annotations only**. It does **not** include the underlying Nymeria or AEA videos, sensor streams, audio, images, or raw dataset files. Users must obtain the underlying Nymeria and/or AEA data separately from the official sources and comply with their respective licenses and access terms.

## Files

### `nymeria_annotations.csv`

Temporally grounded action annotations for clips from the Nymeria dataset.

Columns:

| Column | Description |
|---|---|
| `dataset` | Dataset identifier. |
| `sequence_id` | Source recording, session, or sequence identifier. |
| `start_time_sec` | Clip start time in seconds relative to the source sequence. |
| `end_time_sec` | Clip end time in seconds relative to the source sequence. |
| `duration_sec` | Clip duration in seconds. |
| `script` | High-level scenario or script name associated with the clip. |
| `actions_json` | JSON-encoded list of temporally grounded action annotations. |
| `action_count` | Number of action labels assigned to the clip. |
| `review_level` | Quality-control score from 1 to 3. |
| `reviewed` | Boolean indicating whether the annotation was manually reviewed or corrected. |

### `aea_annotations.csv`

Temporally grounded action annotations for clips from the Aria Everyday Activities dataset.

Columns:

| Column | Description |
|---|---|
| `dataset` | Dataset identifier. |
| `sequence_id` | Source recording, session, or sequence identifier. |
| `start_time_sec` | Clip start time in seconds relative to the source sequence. |
| `end_time_sec` | Clip end time in seconds relative to the source sequence. |
| `duration_sec` | Clip duration in seconds. |
| `script` | High-level scenario or script name associated with the clip. |
| `script_id` | AEA high-level script identifier. |
| `script_sequence_id` | AEA script sequence identifier. |
| `actions_json` | JSON-encoded list of temporally grounded action annotations. |
| `action_count` | Number of action labels assigned to the clip. |
| `review_level` | Quality-control score from 1 to 3. |
| `reviewed` | Boolean indicating whether the annotation was manually reviewed or corrected. |

## Annotation Format

Each row corresponds to one clip.

The `actions_json` field contains a JSON-encoded list of action annotations. Each annotation includes an action label from the shared taxonomy and one or more local temporal segments.

Rows may contain an empty action list when no action from the taxonomy is present.

## Review Levels

The `review_level` column provides a quality-control score:

| Value | Meaning |
|---|---|
| `1` | Flag for review. |
| `2` | Acceptable with caveats. |
| `3` | Confident annotation / no review needed. |

The `reviewed` column indicates whether the annotation was manually reviewed or corrected.

## Data Sources

These annotations are derived from the following datasets:

- Nymeria dataset: https://www.projectaria.com/datasets/nymeria
- Aria Everyday Activities dataset: https://www.projectaria.com/datasets/aea

Users must obtain the underlying datasets separately from the official sources and comply with their licenses, access requirements, and privacy constraints.

## License

The CSV annotation files in this repository are released under the **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**.

See `LICENSE.md` for details.

Use of these annotations may also require access to, and compliance with, the terms of the underlying Nymeria and Aria Everyday Activities datasets.

## Citation

If you use this dataset, please cite the associated paper and this repository.

```text
Anonymous Authors. (2026). Bridging the Annotation Gap: Temporally Grounded Egocentric Action Annotations for Nymeria and AEA. GitHub repository.
