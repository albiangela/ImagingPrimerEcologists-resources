---
layout: default
---

# Animal Tracking Software

Tracking the location, posture, or behaviour of animals over time is a central
application in behavioural ecology. A fundamental trade-off exists between
classical computer-vision methods such as background subtraction (less
computationally intensive but more rigid, requiring controlled conditions) and
AI-assisted keypoint methods (which benefit from GPU acceleration and generalize
to complex scenes but require training data).

## Tracking Software

Overview of animal-tracking software, showing tracking method, ability to identify individuals, and multi-animal support. Background subtraction methods (TRex, idtracker.ai) require controlled laboratory conditions; keypoint detection methods (SLEAP, DeepLabCut, Lightning-pose) require training data but generalize to more complex scenes. For a more exhaustive list, see Panadeiro et al. 2021.

| Software | Tracking Method | Individual ID | Multi-Animal | Reference |
|----------|----------------|:-------------:|:------------:|-----------|
| [TRex](https://trex.run/) | Background subtraction and identity learning; YOLO-compatible | Yes | Yes | Walter & Couzin 2021 |
| [idtracker.ai](https://idtracker.ai/latest/) | Background subtraction and identity learning | Yes | Yes | Torrents et al. 2026 |
| [SLEAP](https://sleap.ai/) | Keypoint detection | Limited | Yes | Pereira et al. 2022 |
| [DeepLabCut](https://github.com/DeepLabCut/DeepLabCut) | Keypoint detection with 3D support | Limited | Yes | Nath et al. 2019; Lauer et al. 2022 |
| [Lightning-pose](https://lightning-pose.readthedocs.io/en/latest/index.html) | Keypoint detection with 3D support | Limited | Limited | Biderman et al. 2024 |
| [FastTrack](https://www.fasttrack.sh/) | Centroid tracking | Limited | Limited | Gallois & Candelier 2021 |
| [AnimalTA](http://vchiara.eu/index.php/animalta) | Centroid tracking with manual correction | Limited | Limited | Chiara & Kim 2023 |

| [Tracktor](https://github.com/vivekhsridhar/tracktor) | Centroid tracking | Limited | Limited | [Sridhar et al. 2019](https://doi.org/10.1111/2041-210X.13166); [Minasandra et al. 2026, TracktorLive](https://doi.org/10.64898/2026.03.12.711471) |

## Preserving Identities

When individual identity must be maintained, two broad approaches are available:
physical tagging (visible markers such as QR or color tags attached to
individuals) and natural visual differences (markerless re-identification, more
challenging for clonal or visually similar animals). Persistent identity matching
adds considerable complexity and should be attempted only when analyses genuinely
depend on distinguishing specific individuals (e.g., social hierarchy or
individual-specific treatments). Tools such as TRex allow users to review and
manually correct identities efficiently by focusing only on ambiguous segments.

## Notes for contributors

Keep additions concise, clearly labeled, and beginner-friendly.
