---
layout: page
title: "Foundations: data engines for video understanding"
description: VLM-driven pipelines that produce the fine-grained annotations strong video models need.
importance: 5
category: research
related_publications: false
---

Underlying all of the above is the challenge of producing the **fine-grained video annotations** that train strong models. We build data engines that use vision-language models to temporally segment video and auto-generate question–answer pairs, with **active learning** targeting human verification at low-confidence points.

This pipeline produced **PLM-FGQA**, the largest manually-labeled video question-answering dataset, which trains an open-source VLM that **outperforms proprietary industry models** on video understanding benchmarks.

**Recent work**

- *PerceptionLM: Open-Access Data and Models for Detailed Visual Understanding* (NeurIPS 2025, spotlight).
- *Ego-Exo4D: Understanding Skilled Human Activity from First- and Third-Person Perspectives* (CVPR 2024).
