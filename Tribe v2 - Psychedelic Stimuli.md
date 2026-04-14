# TRIBE v2 × Psychedelic Phenomenology-Inspired Stimuli

## Working title

**A Computational Psychedelicity Atlas: Mapping Predicted Cortical Response Geometry Under Parametric, Phenomenology-Inspired Video Perturbations**

---

## Abstract

Psychedelic experiences are often described in terms of altered perception, including intensified color, contour instability, pattern recursion, temporal distortion, audiovisual coupling changes, salience amplification, and shifts in self-world boundaries. Yet most computational approaches to psychedelic neuroscience focus on pharmacological state changes rather than the structure of the external stimuli that may evoke, mimic, or interact with psychedelic phenomenology. Here we propose a realistic, high-impact, and experimentally tractable project using **TRIBE v2**, Meta’s multimodal brain foundation model for predicting cortical responses to naturalistic stimuli, to construct a **computational psychedelicity atlas**. Rather than asking whether a model can recognize a “psychedelic brain state,” we ask a cleaner question: **which controlled, phenomenology-inspired transformations of naturalistic video most strongly and selectively alter predicted cortical response geometry?**

The core idea is to begin with short naturalistic clips and generate edited variants that systematically manipulate dimensions such as color instability, contour instability, pattern recursion, temporal persistence, and audiovisual incongruence. TRIBE v2 can then be used to predict cortical responses to each variant, enabling analysis of whole-cortex response distance, region-of-interest shifts, temporal dynamics, and representational clustering across perturbation families. This allows us to identify which stimulus manipulations produce the largest departures from baseline predictions, which combinations show non-additive or synergistic effects, and whether different edit families converge on shared response manifolds.

The project is explicitly framed as a study of **stimulus perturbation rather than pharmacological state perturbation**. That distinction is crucial. Psychedelic-style editing cannot reproduce the full endogenous state induced by compounds such as psilocybin, LSD, or 5-MeO-DMT. It can, however, approximate selected perceptual and temporal aspects of psychedelic phenomenology in a controlled way. By isolating these components, the proposed work offers a principled strategy for decomposing “trippiness” into testable stimulus dimensions rather than treating it as a vague, binary category.

The project can proceed in three escalating stages. First, an in silico mapping stage uses TRIBE v2 alone to identify stimulus dimensions that most strongly shift predicted cortical response geometry. Second, a behavioral validation stage tests whether TRIBE-derived metrics predict human ratings of trippiness, instability, awe, salience, and self-boundary loosening. Third, a neural validation stage can compare model-derived predictions with empirical EEG and/or fNIRS responses collected while participants view selected clips. Together, these stages create a bridge between stimulus engineering, brain prediction, and subjective phenomenology.

Beyond proof of concept, this framework opens several applications: principled generation of experimental stimuli for psychedelic neuroscience, computational screening of candidate stimuli before human testing, quantification of latent dimensions of altered visual phenomenology, and eventual comparison between non-pharmacological perceptual perturbations and drug-modulated neural responses. If successful, the project would provide a novel platform for understanding which features of sensory input most strongly shape brain activity in ways that resemble, approximate, or interact with altered states of consciousness.

---

## 1. Core idea in one sentence

Use TRIBE v2 to quantify how **controlled, psychedelic phenomenology-inspired edits to naturalistic videos** change predicted cortical response geometry, then use those predictions to guide behavioral and neural validation in humans.

---

## 2. Why this is interesting

Most psychedelic neuroscience asks what a drug does to the brain. That is important, but it is only half the story. Psychedelic experience is not just a state floating in empty space; it is a relationship between a transformed subject and a structured sensory world. Different sensory inputs likely interact with altered priors, salience weighting, predictive processing, temporal integration, and bodily self-modeling in different ways.

This project goes after the neglected half: **the structure of the stimulus itself**.

Instead of treating “psychedelic content” as vibes, aesthetics, or something you know when you see it, we make it computationally explicit. We define dimensions of sensory transformation, manipulate them parametrically, and ask what they do to predicted cortical responses.

That is strong for four reasons:

1. **It is conceptually clean.** We are not pretending edited videos create a drug state.
    
2. **It is experimentally realistic.** The in silico stage is immediately doable.
    
3. **It scales.** It can grow into behavioral and neural work.
    
4. **It is genuinely novel.** Most people would stop at “normal video vs trippy video.” That is way too blunt.
    

---

## 3. The key conceptual distinction: stimulus perturbation is not state perturbation

This is the single most important thing to get right.

A psychedelic drug changes the organism. It alters neurochemistry, network dynamics, precision weighting, time perception, bodily salience, affective tone, suggestibility, interoceptive amplification, and often meaning attribution. A video edit does not do that.

A video edit changes the **stimulus statistics**.

So the right framing is not:

> Can TRIBE v2 detect psychedelic brain states from trippy videos?

The right framing is:

> Which stimulus transformations inspired by psychedelic phenomenology produce the strongest and most selective changes in predicted cortical response geometry?

That is cleaner, more defensible, and frankly more interesting.

Once you have that result, you can later ask whether those same transformations interact with actual psychedelic states in people.

---

## 4. What TRIBE v2 is good for in this context

TRIBE v2 is useful here because it provides a way to turn naturalistic multimodal stimuli into predicted cortical responses. That means it can act as a **brain-space screening engine** for large stimulus sets.

Instead of guessing which edits might matter, you can:

- generate many variants,
    
- run them through the model,
    
- quantify how predictions shift,
    
- identify candidate transformations,
    
- then bring only the most informative stimuli into real human testing.
    

That is a huge efficiency gain. It turns stimulus design from an art project into an analysis pipeline.

---

## 5. The strongest version of the project

### Project name

**Computational Psychedelicity Atlas**

### High-level aim

To map how controlled sensory perturbations inspired by psychedelic phenomenology alter predicted cortical response geometry.

### Basic workflow

1. Start with naturalistic video clips.
    
2. Create systematically edited variants.
    
3. Run TRIBE v2 on all clips.
    
4. Analyze the response geometry.
    
5. Validate a selected subset with human ratings.
    
6. Optionally validate further with EEG and/or fNIRS.
    

---

## 6. Why binary “normal vs trippy” is not enough

A two-condition comparison is tempting because it feels intuitive. It is also scientifically weak.

Why?

Because “trippy” is not one thing. It mixes together multiple latent dimensions:

- color intensity and instability,
    
- edge shimmer or contour instability,
    
- geometric repetition or recursion,
    
- temporal persistence or trails,
    
- altered apparent causality,
    
- figure-ground ambiguity,
    
- audiovisual decoupling or hyper-coupling,
    
- salience weirdness,
    
- semantic destabilization.
    

If you bundle all of that into a single edited clip, you learn almost nothing about which feature mattered.

A binary design is fine for a poster demo. It is not fine if you want real traction.

The better move is to define a **stimulus factor space**.

---

## 7. Candidate stimulus dimensions

Below is a strong first-pass parameter dictionary. The ideal set should be interpretable, reasonably orthogonal, and technically feasible to implement.

### 7.1 Color instability

Manipulations of saturation, hue cycling, local chromatic drift, rainbow contouring, or luminance exaggeration.

**Phenomenology link:** intensified or unstable color experience.

### 7.2 Contour instability

Subtle waviness of edges, breathing surfaces, texture ripple, local deformation of object boundaries.

**Phenomenology link:** “things are moving even when they are still.”

### 7.3 Pattern recursion

Fractalization, tiling, kaleidoscopic repetition, recursive motif embedding.

**Phenomenology link:** geometric patterning and self-similarity.

### 7.4 Temporal persistence

Motion trails, afterimage-like carryover, delayed decay of prior frames, smearing of object motion.

**Phenomenology link:** perceptual persistence and temporal elongation.

### 7.5 Temporal warping

Local speed fluctuations, slowed causality, pulse-like time dilation, micro-jitter in temporal continuity.

**Phenomenology link:** altered temporal flow.

### 7.6 Figure-ground ambiguity

Reduced segmentation stability, partial blending of object/background boundaries, ambiguous object emergence.

**Phenomenology link:** loosened perceptual organization and uncertainty.

### 7.7 Semantic destabilization

Slightly uncanny object transformations, improbable object persistence, subtle scene logic violations.

**Phenomenology link:** the world feels familiar but not quite right.

### 7.8 Audiovisual incongruence or coupling

Audio either lags, leads, mismatches, or is over-coupled to visual transformations.

**Phenomenology link:** altered multisensory binding.

---

## 8. Best first design: a parametric stimulus engine

The cleanest design is not a huge brute-force grid with every combination. That explodes fast and becomes stupid.

A better approach is:

- choose a modest number of interpretable dimensions,
    
- set a few levels per dimension,
    
- sample the space efficiently.
    

### Suggested first-pass design

Use 24 source clips, each 8–12 seconds long.

Include a few content classes:

- faces/social interaction,
    
- natural scenes,
    
- urban motion,
    
- object manipulation,
    
- abstract movement.
    

Manipulate 4 core dimensions at 4 levels each:

- color instability,
    
- contour instability,
    
- temporal persistence,
    
- pattern recursion.
    

A full crossing gives 256 variants per clip, which is overkill. Instead, use:

- a fractional factorial design,
    
- Latin hypercube sampling,
    
- or another efficient coverage strategy.
    

The goal is not to exhaust the space. The goal is to map it intelligently.

---

## 9. What to compute from TRIBE v2 outputs

This is where the project becomes actually good.

You do not just want screenshots of predicted brain maps. You want **response geometry**.

### 9.1 Whole-cortex distance from baseline

For each edited clip, compute the distance between the predicted cortical response and the original clip.

This gives a simple measure of how much the edit perturbs the predicted response.

### 9.2 ROI-specific deltas

Define regions or networks of interest, then quantify how each manipulation shifts predictions within them.

Potential targets:

- early visual cortex,
    
- ventral visual stream,
    
- motion-sensitive regions,
    
- auditory cortex,
    
- parietal association cortex,
    
- medial frontal/posterior midline proxies,
    
- multisensory integration zones.
    

### 9.3 Temporal trajectory geometry

Treat each clip as a trajectory through predicted cortical response space.

Then quantify:

- path length,
    
- curvature,
    
- temporal smoothness,
    
- entropy,
    
- acceleration in state-space.
    

This lets you ask whether some perturbations produce unusually unstable or wandering response trajectories.

### 9.4 Representational clustering

Do clips cluster by source content, by edit family, or by parameter strength?

That is a big question. If edit family dominates over source content, then the manipulation is doing something robust and generalizable.

### 9.5 Interaction and synergy analysis

Test whether combinations of transformations produce non-additive effects.

Example:

- does contour instability plus temporal persistence create a larger-than-expected shift?
    
- does color instability matter only when recursion is present?
    

That is where things get spicy.

### 9.6 Convergent manifolds

Different edits may look visually distinct but end up producing similar predicted cortical trajectories.

That would be an especially cool result. It would suggest multiple sensory routes into a shared “altered response geometry.”

---

## 10. The most original twist

One of the strongest unorthodox extensions is this:

### Optimize for maximal brain divergence under minimal visible change

Instead of asking “what looks most psychedelic,” ask:

> Which subtle, nearly invisible perturbations produce the largest predicted cortical shifts?

That is a much sharper scientific question.

Why it matters:

- It avoids reducing the project to psychedelic aesthetics.
    
- It might reveal hidden stimulus features with disproportionate neural leverage.
    
- It creates a path toward discovering sensory manipulations that alter brain dynamics without obvious visual weirdness.
    

That is not just cooler. It is also more useful.

---

## 11. The second original twist

### Search for shared latent axes rather than hand-coded categories

The hand-coded parameter dictionary is necessary at first. But after generating enough stimuli, you can also ask whether the model reveals latent dimensions you did not explicitly define.

For example:

- Which principal axes of variation in the edited stimuli best explain shifts in predicted cortical geometry?
    
- Do those axes line up with perceptual ratings like trippiness, awe, confusion, instability, or self-loss?
    
- Are there hidden composite features that matter more than your original edit labels?
    

That turns the project from a stimulus-comparison paper into a possible **feature-discovery platform**.

---

## 12. What you were not fully accounting for

### 12.1 Out-of-distribution risk

If the edits become too bizarre, the model may no longer be behaving in a trustworthy, interpretable way.

That does not invalidate the project. It means you must track and report it.

You should explicitly compare:

- mild edits,
    
- moderate edits,
    
- extreme edits.
    

If effects only appear at absurd settings, that is less compelling.

### 12.2 Content confounds

A face clip and a forest clip are already different before you touch them.

So your main analysis should be within-clip whenever possible:

- original clip versus edited variants of that same clip.
    

Then test generalization across content classes later.

### 12.3 Motion sickness is not trippiness

This one matters a lot for human data.

Certain manipulations may inflate ratings simply because they are nauseating, disorienting, or annoying.

So include separate ratings for:

- trippiness,
    
- visual instability,
    
- awe,
    
- discomfort,
    
- nausea,
    
- confusion,
    
- affective valence.
    

Do not let sickness masquerade as altered-state phenomenology.

### 12.4 Phenomenology is multi-dimensional

If you collect only one subjective rating like “how psychedelic was this?”, you are throwing away the whole point.

You want at least a few dimensions, such as:

- trippiness,
    
- perceptual instability,
    
- meaningfulness/salience,
    
- self-boundary looseness,
    
- emotional valence,
    
- discomfort.
    

### 12.5 Audio matters

If the stimulus includes sound, audio can either stabilize or destabilize the perceptual interpretation of the scene.

You should probably run at least three stimulus families:

- visual-only edits,
    
- audio-only manipulations,
    
- audiovisual interaction manipulations.
    

### 12.6 Validation mismatch

TRIBE v2 is not your participant.

So the strongest empirical question is not “did the exact cortical map match?” but something like:

> Did the model-derived ranking or geometry predict human ratings and empirical neural sensitivity across stimuli?

That is far more realistic.

### 12.7 State dependence in future work

Later, if you do collect neural data under actual altered states, the same stimulus may behave differently depending on drug condition, expectation, fatigue, arousal, or trait absorption.

That is not a bug. That is the whole frontier.

---

## 13. Three-stage roadmap

## Stage 1: In silico atlas

### Aim

Map how phenomenology-inspired video perturbations alter predicted cortical response geometry.

### Inputs

- naturalistic video clips,
    
- edited variants,
    
- optional audio manipulations.
    

### Outputs

- perturbation maps,
    
- ROI-level sensitivity profiles,
    
- temporal response trajectories,
    
- response-distance rankings,
    
- convergent manifolds.
    

### Deliverable

A computational map of which stimulus dimensions matter most.

---

## Stage 2: Behavioral validation

### Aim

Test whether TRIBE-derived metrics predict subjective experience.

### Human measures

Participants view selected stimuli and rate:

- trippiness,
    
- instability,
    
- awe,
    
- salience/meaningfulness,
    
- self-boundary loosening,
    
- confusion,
    
- discomfort/nausea.
    

### Main question

Do model-derived distances, cluster memberships, or ROI signatures predict subjective ratings?

### Why this matters

If yes, the model is not just producing arbitrary neural-looking outputs. It is capturing something psychologically relevant.

---

## Stage 3: Neural validation

### Aim

Test whether model-selected stimuli predict real neural differentiation.

### Possible modalities

- EEG,
    
- fNIRS,
    
- ideally both if practical.
    

### Candidate neural targets

- occipital signal complexity,
    
- spectral desynchronization,
    
- functional coupling changes,
    
- temporal response variability,
    
- multisensory integration signatures.
    

### Realistic framing

You are not directly “validating TRIBE v2 as a psychedelic model.”  
You are testing whether **stimuli identified by the model as high-impact** also produce stronger measurable neural effects in people.

That is much more defensible.

---

## 14. Aims and hypotheses

## Aim 1

Construct a parametric stimulus space inspired by psychedelic phenomenology.

### Hypothesis 1

Different classes of perturbation will produce dissociable shifts in predicted cortical response geometry rather than a single monotonic “trippiness” effect.

## Aim 2

Identify which perturbation dimensions and combinations produce the largest departures from baseline predicted responses.

### Hypothesis 2

Contour instability, temporal persistence, and pattern recursion will have stronger and more widespread effects than simple color exaggeration alone.

## Aim 3

Test whether different perturbation families converge onto shared response manifolds.

### Hypothesis 3

Distinct edit types will sometimes produce similar predicted response geometry, suggesting common latent axes of altered sensory processing.

## Aim 4

Validate whether model-derived metrics predict human subjective ratings.

### Hypothesis 4

Stimuli with larger model-derived cortical distance and more unstable temporal trajectories will be rated as more trippy and perceptually unstable.

## Aim 5

Explore whether model-selected stimuli show stronger empirical neural differentiation.

### Hypothesis 5

Stimuli identified by the model as maximally perturbative will elicit greater neural complexity and/or altered coupling relative to low-perturbation controls.

---

## 15. Practical implementation plan

### 15.1 Stimulus acquisition

Curate a set of short, high-quality naturalistic videos.

Keep them:

- visually rich,
    
- semantically diverse,
    
- legally usable,
    
- not too long.
    

### 15.2 Stimulus editing pipeline

Build or adopt a reproducible transformation pipeline.

Possible implementation routes:

- shader-based edits,
    
- video post-processing scripts,
    
- computer vision filters,
    
- generative or diffusion-based stylization for selected manipulations.
    

The important thing is reproducibility and parameter control.

### 15.3 Parameter bookkeeping

Every clip variant should carry metadata for:

- source clip,
    
- edit family,
    
- parameter values,
    
- audio condition,
    
- version number.
    

If you do not track this cleanly, the project will become an archaeological dig through chaos.

### 15.4 Model execution

Run TRIBE v2 on all stimuli and store:

- cortical prediction outputs,
    
- any intermediate embeddings that are useful,
    
- clip timestamps and alignment info.
    

### 15.5 Analysis layer

Build an analysis pipeline that computes:

- baseline distance,
    
- ROI summaries,
    
- temporal trajectory features,
    
- clustering and manifold structure,
    
- parameter sensitivity and interaction models.
    

### 15.6 Human study selection

Choose a representative subset of stimuli that span:

- low to high perturbation,
    
- distinct edit families,
    
- overlapping versus separated manifolds.
    

This is where the computational stage saves you money and participant time.

---

## 16. What makes the idea realistic

It is realistic because the first stage does not require immediate human data collection.

You can get meaningful results from:

- curation,
    
- controlled editing,
    
- model inference,
    
- careful geometry analysis.
    

That means you can produce something interesting fast, while laying groundwork for a later empirical study.

It is also realistic because the project decomposes naturally:

- stimulus engine,
    
- model pipeline,
    
- analysis pipeline,
    
- behavioral validation,
    
- neural validation.
    

Each part can become a module, a student project, or a standalone contribution.

---

## 17. What would make the paper genuinely good

Not just showing pretty stimuli.  
Not just showing pretty brain maps.

The paper becomes good if it demonstrates at least one of these:

1. **A principled decomposition** of psychedelic-like sensory perturbations into interpretable dimensions.
    
2. **A stable cortical response geometry** induced by those perturbations.
    
3. **Convergence across distinct edit families** onto shared manifolds.
    
4. **Prediction of subjective phenomenology** from model-derived measures.
    
5. **Efficient screening of candidate altered-state stimuli** for future experiments.
    

Hit two or three of those and you have something real.

---

## 18. Obvious failure modes

### Failure mode 1

The edits are too crude and just look like cheap music-video effects.

**Fix:** prioritize subtle, principled transformations over cliché aesthetics.

### Failure mode 2

Effects are driven mostly by source clip content.

**Fix:** within-clip analyses, larger clip set, cross-content validation.

### Failure mode 3

The strongest predictors are nausea and disorientation.

**Fix:** separate discomfort from trippiness in behavioral ratings.

### Failure mode 4

The model only reacts strongly when stimuli are wildly out of distribution.

**Fix:** focus on moderate perturbations and track intensity-response curves.

### Failure mode 5

The phenomenon is too broad and under-specified.

**Fix:** define a crisp parameter dictionary and a compact hypothesis set.

---

## 19. Strong application areas

### 19.1 Experimental stimulus design for psychedelic neuroscience

Use the atlas to select sensory perturbations for studies under placebo, psilocybin, LSD, ketamine, or related compounds.

### 19.2 Non-pharmacological altered-state induction research

Use model-selected stimuli to study perceptual destabilization without drugs.

### 19.3 Computational phenotyping of visual phenomenology

Map which stimulus features most strongly predict ratings like trippiness, awe, instability, and salience.

### 19.4 Closed-loop or adaptive experience design

In the long run, stimuli could be dynamically tuned to target specific phenomenological dimensions.

### 19.5 Theory-building in predictive processing and altered perception

The project offers a way to explore which kinds of sensory perturbation most strongly engage mechanisms associated with uncertainty, loosened priors, multisensory ambiguity, and temporal disruption.

---

## 20. How this could connect to actual psychedelic data later

This project becomes especially powerful if later paired with empirical data under drug conditions.

Possible future design:

- participants view the same stimulus families under placebo and psilocybin,
    
- model-derived perturbation metrics are used to select or stratify stimuli,
    
- neural responses are compared across states,
    
- interaction terms test whether some stimulus dimensions become especially potent under altered states.
    

That would let you ask questions like:

- Are some perceptual perturbations disproportionately amplified under psilocybin?
    
- Does the geometry of subjective ratings change under the drug?
    
- Do pharmacological state changes and stimulus perturbations converge, diverge, or interact nonlinearly?
    

That is where this could become really fucking interesting.

---

## 21. Concrete first experiment proposal

### Title

**Pilot In Silico Mapping of Phenomenology-Inspired Video Perturbations with TRIBE v2**

### Stimuli

24 naturalistic clips, 8–12 seconds each.

### Transformations

4 dimensions:

- color instability,
    
- contour instability,
    
- temporal persistence,
    
- pattern recursion.
    

### Parameterization

4 levels each, sampled with an efficient design rather than full crossing.

### Model outputs

- vertex-wise cortical predictions,
    
- temporal predictions per clip,
    
- derived ROI summaries,
    
- derived manifold metrics.
    

### Primary analyses

1. Which dimensions produce the largest whole-cortex perturbation?
    
2. Which combinations show interaction effects?
    
3. Do clips cluster by edit family or by content?
    
4. Do distinct edit families converge on shared cortical manifolds?
    

### Success criterion

A reproducible ranking of perturbation dimensions and/or a detectable convergent manifold structure.

---

## 22. Minimal behavioral follow-up

### Participants

A modest online or lab sample.

### Task

View a model-selected subset of clips and rate each on several dimensions.

### Ratings

- trippiness,
    
- perceptual instability,
    
- awe,
    
- salience,
    
- self-boundary looseness,
    
- discomfort/nausea.
    

### Main test

Can TRIBE-derived metrics predict ratings better than raw edit labels alone?

If yes, that is a big win.

---

## 23. Minimal neural follow-up

### EEG version

Use selected clips spanning low, medium, and high model-derived perturbation.

Look at:

- spectral signatures,
    
- signal complexity,
    
- temporal variability,
    
- occipital and frontoparietal responses.
    

### fNIRS version

Focus on realistic cortical coverage and slower changes in response profiles, especially if paired with behavioral ratings and repeated exposure blocks.

### Better framing

You are testing whether **model-derived perturbation structure predicts empirical differentiability**.

That is the grown-up way to say it.

---

## 24. Why this matters beyond the immediate project

This is not only about psychedelic videos.

It is about whether we can build a computational bridge between:

- engineered stimulus transformations,
    
- predicted brain response geometry,
    
- human phenomenology,
    
- and later, altered states.
    

If that bridge works, it gives you a new kind of experimental engine.

Instead of guessing what stimuli might be interesting, you can computationally discover them.

That is a big deal.

---

## 25. Final take

The best version of this project is not a gimmick about making videos more trippy.

It is a principled attempt to:

- decompose altered visual phenomenology into controllable stimulus dimensions,
    
- map those dimensions into predicted cortical response geometry,
    
- identify shared manifolds and interaction effects,
    
- and then validate whether those computational signatures matter to real human experience and neural measurement.
    

That is weird, ambitious, and still actually doable.

Which is exactly the sweet spot.

---

## 26. Ultra-short pitch version

We propose to use TRIBE v2 as a brain-space screening engine to map how controlled, psychedelic phenomenology-inspired transformations of naturalistic videos alter predicted cortical response geometry. By moving from binary “normal vs trippy” comparisons to a parametric stimulus manifold, we can identify which perceptual features most strongly perturb predicted brain responses, whether distinct edit families converge on shared cortical manifolds, and whether these model-derived signatures predict human phenomenology and empirical neural sensitivity.