---
layout: page
title: Learning from video at scale, without manual labels
description: Turning noisy, narrated, web-scale video into training signal.
importance: 2
category: research
related_publications: false
---

Clean labeled video datasets are small and narrow. The web offers orders of magnitude more video content, often paired with noisy speech transcripts or external articles, sometimes with no annotation at all. This abundance resists direct supervision: narrations are temporally misaligned with the actions they describe, speech captures actions only loosely, step boundaries are not annotated, and many tasks lack paired text entirely.

We develop methods that turn this raw abundance into a **useful training signal**. Some of our work aligns instructional articles with how-to videos to discover step structure, or grounds procedural steps through correspondences between video, narration, and external knowledge. Other directions mine cross-video supervision for fine-grained comparison, treat noisy corpora as **verifiers of generated plans** rather than label sources, or train pairs of **self-evolving agents** that bootstrap their own supervision from raw unlabeled video.

The resulting models generalize across domains and match or surpass fully supervised baselines while requiring no human annotation.

**Recent work**

- *RECIPE: Procedural Planning via Grounding in Instructional Video.*
- *EvoGround: Self-Evolving Video Agents for Video Temporal Grounding.*
- *HT-Step: Aligning Instructional Articles with How-To Videos* (NeurIPS 2023).
- *Learning to Ground Instructional Articles in Videos through Narrations* (ICCV 2023).
- *Step Differences in Instructional Video* (CVPR 2024).
