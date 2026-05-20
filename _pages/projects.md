---
layout: page
title: Research
permalink: /research/
description:
nav: true
nav_order: 2
---

<style>
  .thrust {
    margin: 0;
  }
  hr.thrust-divider {
    width: 100%;
    max-width: 720px;
    border: 0;
    border-top: 1px dashed #b0b0b0;
    margin: 2.5rem auto;
    background: transparent;
    height: 0;
    opacity: 1;
  }
  html[data-theme="dark"] hr.thrust-divider {
    border-top-color: rgba(255, 255, 255, 0.28);
  }

  /* Image constrained to the same column width as the text */
  .thrust-image {
    max-width: 720px;
    margin: 0 auto;
    background: var(--global-card-bg-color, #fff);
    line-height: 0;
  }
  .thrust-image img {
    display: block;
    width: 100%;
    height: auto;
  }

  .thrust-intro {
    max-width: 760px;
    margin: 0.5rem auto 3.5rem;
    padding: 1.5rem 0 1.75rem;
    border-top: 1px dashed #b0b0b0;
    border-bottom: 1px dashed #b0b0b0;
    font-size: 1.35rem;
    line-height: 1.55;
    font-weight: 400;
    text-align: center;
    font-style: italic;
    color: var(--global-text-color, inherit);
  }
  html[data-theme="dark"] .thrust-intro {
    border-top-color: rgba(255, 255, 255, 0.28);
    border-bottom-color: rgba(255, 255, 255, 0.28);
  }

  .thrust-body {
    max-width: 720px;
    margin: 2.5rem auto 0;
  }
  .thrust-body h2 {
    font-size: 1.75rem;
    line-height: 1.3;
    font-weight: 600;
    margin: 0 0 1.1rem;
  }
  .thrust-body p {
    line-height: 1.7;
    margin: 0 0 1rem;
  }
  .thrust-body p:last-child { margin-bottom: 0; }

  .thrust-recent {
    margin-top: 1.75rem;
  }
  .thrust-recent-label {
    font-size: 0.72rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--global-text-color-light, #828282);
    margin: 0 0 0.6rem;
  }
  .thrust-recent-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  .thrust-recent-list li {
    padding: 0.55rem 0;
    border-bottom: 1px solid var(--global-divider-color, #eee);
    font-size: 0.95rem;
    line-height: 1.5;
    color: var(--global-text-color, inherit);
  }
  .thrust-recent-list li:first-child { border-top: 1px solid var(--global-divider-color, #eee); }

  @media (max-width: 600px) {
    .thrust { margin-bottom: 3.5rem; }
    .thrust-body { margin-top: 1.5rem; padding: 0 1rem; }
    .thrust-body h2 { font-size: 1.4rem; }
  }

  html[data-theme="dark"] .thrust-recent-list li,
  html[data-theme="dark"] .thrust-recent-list li:first-child {
    border-color: rgba(255, 255, 255, 0.08);
  }
</style>

<p class="thrust-intro">Our work spans five research thrusts, each tackling a different facet of how AI systems understand, anticipate, and act on dynamic video.</p>

<section class="thrust">
  <div class="thrust-image">
    <img src="{{ '/assets/img/research/trajpilot_crop.png' | relative_url }}" alt="TrajPilot" loading="lazy">
  </div>
  <div class="thrust-body">
    <h2>1. Egocentric perception, anticipation, and planning</h2>
    <p>Many of the most important physical AI applications, including wearable assistants, AR guidance systems, and robots operating alongside humans, perceive the world from a first-person perspective. Egocentric video has distinctive properties that make it information-rich yet poorly served by methods designed for third-person video: continuous long-duration streams, head motion encoding visual attention, and hand-object interactions at close range. We develop benchmarks, data, and models for understanding skilled human activity from this perspective, and for systems that go beyond classifying what is happening now toward anticipating what will happen next and planning multi-step procedures.</p>
    <div class="thrust-recent">
      <p class="thrust-recent-label">Recent work</p>
      <ul class="thrust-recent-list">
        <li>How You Move Tells What You'll Do: Trajectory-Conditioned Egocentric Prediction..</li>
        <li>Ego-Exo4D: Understanding Skilled Human Activity from First- and Third-Person Perspectives (CVPR 2024).</li>
        <li>Ego4D Goal-Step: Toward Hierarchical Understanding of Procedural Activities (NeurIPS 2023).</li>
      </ul>
    </div>
  </div>
</section>

<hr class="thrust-divider">

<section class="thrust">
  <div class="thrust-image">
    <img src="{{ '/assets/img/research/recipe_crop.png' | relative_url }}" alt="RECIPE" loading="lazy">
  </div>
  <div class="thrust-body">
    <h2>2. Learning from video at scale, without manual labels</h2>
    <p>Clean labeled video datasets are small and narrow. The web offers orders of magnitude more video content, often paired with noisy speech transcripts or external articles, sometimes with no annotation at all. This abundance resists direct supervision. Narrations are temporally misaligned with the actions they describe. Speech captures actions only loosely. Step boundaries are not annotated, and many tasks lack paired text entirely.</p>
    <p>We develop methods that turn this raw abundance into a useful training signal. Some of our work aligns instructional articles with how-to videos to discover step structure, or grounds procedural steps through correspondences between video, narration, and external knowledge. Other directions mine cross-video supervision for fine-grained comparison, treat noisy corpora as verifiers of generated plans rather than label sources, or train pairs of self-evolving agents that bootstrap their own supervision from raw unlabeled video. The resulting models generalize across domains and match or surpass fully supervised baselines while requiring no human annotation.</p>
    <div class="thrust-recent">
      <p class="thrust-recent-label">Recent work</p>
      <ul class="thrust-recent-list">
        <li>RECIPE: Procedural Planning via Grounding in Instructional Video.</li>
        <li>EvoGround: Self-Evolving Video Agents for Video Temporal Grounding.</li>
        <li>HT-Step: Aligning Instructional Articles with How-To Videos (NeurIPS 2023).</li>
        <li>Learning to Ground Instructional Articles in Videos through Narrations (ICCV 2023).</li>
        <li>Step Differences in Instructional Video (CVPR 2024).</li>
      </ul>
    </div>
  </div>
</section>

<hr class="thrust-divider">

<section class="thrust">
  <div class="thrust-image">
    <img src="{{ '/assets/img/research/svi_bench.png' | relative_url }}" alt="SVI-Bench" loading="lazy">
  </div>
  <div class="thrust-body">
    <h2>3. Strategic video intelligence for multi-agent worlds</h2>
    <p>Most video understanding research evaluates perception in isolation. But agents deployed in the real world, including wearable assistants, robotic fleets, and coordinated teams, must also reason about cause and consequence, simulate alternative futures, and plan under uncertainty. We build benchmarks and models for the full perception-to-agency stack in dynamic multi-agent settings, using team sports as a natural microworld: rich and visually complex, with unambiguous outcomes and verifiable strategic ground truth. Our work exposes a substantial capability cliff in current systems: state-of-the-art models perceive multi-agent scenes well but fail at causal reasoning, strategic simulation, and agentic synthesis over the same evidence.</p>
  </div>
</section>

<hr class="thrust-divider">

<section class="thrust">
  <div class="thrust-image">
    <img src="{{ '/assets/img/research/vited.png' | relative_url }}" alt="ViTED" loading="lazy">
  </div>
  <div class="thrust-body">
    <h2>4. Long-form video understanding and causal reasoning</h2>
    <p>Real-world activity unfolds over minutes to hours, far beyond the short clips most video models handle. We develop architectures that compress long video streams into compact memory representations supporting efficient question-answering, and we study causal and multi-hop reasoning across temporal spans where chain-of-thought approaches break down. Our BIMBA model adapts selective-scan mechanisms to video, winning the EgoSchema Challenge at CVPR 2025; our ViTED model produces visual-symbolic evidence justifying its answers without temporal annotations.</p>
    <div class="thrust-recent">
      <p class="thrust-recent-label">Recent work</p>
      <ul class="thrust-recent-list">
        <li>BIMBA: Selective-Scan Compression for Long-Range Video Question Answering (CVPR 2025).</li>
        <li>ViTED: Video Temporal Evidence Distillation (CVPR 2025).</li>
      </ul>
    </div>
  </div>
</section>

<hr class="thrust-divider">

<section class="thrust">
  <div class="thrust-image">
    <img src="{{ '/assets/img/research/ego_exo4d_crop.png' | relative_url }}" alt="Ego-Exo4D" loading="lazy">
  </div>
  <div class="thrust-body">
    <h2>5. Foundations: data engines for video understanding</h2>
    <p>Underlying all of the above is the challenge of producing the fine-grained video annotations that train strong models. We build data engines that use vision-language models to temporally segment video and auto-generate question-answer pairs, with active learning targeting human verification at low-confidence points. This pipeline produced PLM-FGQA, the largest manually-labeled video question-answering dataset, which trains an open-source VLM that outperforms proprietary industry models on video understanding benchmarks.</p>
    <div class="thrust-recent">
      <p class="thrust-recent-label">Recent work</p>
      <ul class="thrust-recent-list">
        <li>PerceptionLM: Open-Access Data and Models for Detailed Visual Understanding (NeurIPS 2025).</li>
        <li>Ego-Exo4D: Understanding Skilled Human Activity from First- and Third-Person Perspectives (CVPR 2024).</li>
      </ul>
    </div>
  </div>
</section>

<p class="mt-5 text-muted">
For the full list of papers and code, see <a href="{{ '/publications/' | relative_url }}">publications</a>.
</p>
