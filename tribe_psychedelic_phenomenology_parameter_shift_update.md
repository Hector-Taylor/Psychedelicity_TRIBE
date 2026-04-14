# TRIBE v2 project update: neuroscientific psychedelic phenomenology + computational parameter shifts

## Why the hypothesis should change

The stronger version of the project is **not** “trippy videos change predicted brain responses.”

That is too vague, and honestly not sharp enough.

The better hypothesis is grounded in recent work arguing that psychedelic phenomenology has an important **low-level sensory and computational structure**, and that these effects are not merely decorative byproducts of higher-level cognitive change. Aqil and Roseman’s review argues that psychedelic alterations in low-level sensory dimensions—especially visual ones—are specific, mechanistically meaningful, and likely engaged in a two-way interplay with higher-level experience and therapeutics.citeturn614348view0

Even more importantly, Aqil et al. (2025) show something unusually useful for your project: psilocybin does **not** just make perception globally noisy. In psychophysics and 7T fMRI, it specifically alters **visual contextual computations**. In the Ebbinghaus task, psilocybin increased the contextual illusion while leaving control trials without context essentially unchanged; in visual cortex, it reduced **surround suppression** in V1–V3; and their divisive-normalization model captured this effect as a shift in a **specific parameter**—the activation constant **b**—rather than broad changes in pRF size, normalization size, or general model fit.citeturn614348view1turn589434view1turn589434view2

That is the missing impact angle.

The project should therefore be framed around **computational parameter shifts in contextual visual processing**.

---

## Revised conceptual core

We use psychedelic phenomenology to motivate a space of **sensory/contextual perturbations**, but we anchor the hypotheses in computational neuroscience:

**Psychedelic-like visual phenomena may reflect shifts in contextual computation—especially weakened surround suppression / altered normalization-like interactions—rather than generic perceptual distortion.**

Your TRIBE project then becomes:

1. Build a perturbation space that targets **contextual computations** in naturalistic videos.
2. Run TRIBE on those perturbations.
3. Ask which perturbations induce cortical prediction changes most consistent with **reduced contextual suppression**, **weakened figure-ground stabilization**, or other interpretable computational shifts.

That is a much more interesting paper.

---

## Critical synthesis of the Aqil angle

## What you should absolutely take from the 2023 review
The Aqil & Roseman review gives you permission to stop treating sensory phenomena as fluff. Their core claim is that low-level sensory changes under psychedelics are:
- specific,
- partly distinct from higher-level changes,
- and potentially causally relevant for brain dynamics, experience, and therapeutic effects.citeturn614348view0

That helps justify why a project centered on **visual/sensory dimensions** is not peripheral. It is central.

## What you should absolutely take from the 2025 Nature paper
The 2025 paper gives you the computational wedge:
- psilocybin increased the Ebbinghaus illusion by about **38% at 5 mg** and **59% at 10 mg** relative to placebo, with control perception unchanged, implying a contextual rather than global effect;citeturn614348view1
- psilocybin reduced **surround suppression** in early visual cortex;citeturn589434view1
- the effect was captured by a change in a **specific model parameter** (activation constant **b**) rather than pRF size or normalization constant.citeturn589434view0turn589434view2

That is exactly the sort of mechanistic specificity your application was missing.

## What not to overclaim
TRIBE is **not** Aqil’s divisive-normalization model.
TRIBE was not trained on psychedelic data.
So you cannot claim that TRIBE estimates “the psilocybin parameter” or directly recovers psychedelic brain states.

What you **can** claim is much cleaner:
TRIBE lets you perform an **in-silico search over naturalistic stimuli** to identify which perturbations most strongly and systematically alter predicted cortical response structure in ways that are **consistent with computational hypotheses from psychedelic vision science**.

That is rigorous and exciting without being bullshit.

---

## Revised hypotheses

## Main hypothesis
Naturalistic video perturbations that selectively alter **contextual visual structure**—rather than merely exaggerating color or adding generic “trippy” effects—will produce larger and more structured shifts in TRIBE-predicted cortical responses.

## Computational hypothesis
Perturbations that weaken contextual constraints in the stimulus should produce response signatures consistent with **reduced contextual suppression / altered normalization-like interactions**, especially in early visual cortex and in downstream sensory-integration regions.

## Phenomenology-linked hypothesis
Psychedelic-relevant visual qualities such as boundary instability, figure-ground slippage, local recursive patterning, and temporal persistence will matter to the extent that they perturb **contextual computations**, not simply because they look weird.

## Specific parameter-shift hypothesis
The most informative outcome is not a scalar “trippiness score,” but the discovery of a **low-dimensional perturbation manifold** whose dominant axes can be interpreted as computational shifts in contextual processing. In other words: your project should hunt for **latent computational axes**, not vibes.

---

## How to redesign the perturbation space

The perturbation dimensions should now be chosen to target contextual computation more directly.

### Tier 1: strongly Aqil-aligned perturbations
1. **Figure-ground instability**  
   weaken segmentation boundaries; soften local ownership of edges

2. **Context gain manipulation**  
   modulate the visual prominence of surrounds relative to targets or local focal regions

3. **Local surround interference**  
   add structured nearby textures, echoes, or flankers that alter neighborhood interactions

4. **Boundary diffusion / contour bleed**  
   reduce edge precision and increase local overlap between adjacent structures

5. **Temporal persistence**  
   create short afterimage-like carryover that weakens clean separation between present input and recent context

### Tier 2: useful but less central
6. **Color drift / saturation modulation**  
7. **Pattern recursion / self-similar echoes**  
8. **Audiovisual incongruence**

These are still worth testing, but they should no longer be the conceptual heart of the project.

---

## The actual high-impact angle

The sexy version is this:

**Use TRIBE to perform a computational phenotype search.**

You are not just asking, “what edits make the model change?”
You are asking:

**Which perturbations in naturalistic video most strongly induce cortical prediction shifts compatible with theories that psychedelics alter contextual computations?**

That is way better.

You can even define target signatures such as:
- stronger alteration in early visual cortex than in high-level semantic cortex,
- increased sensitivity to local neighborhood manipulations,
- differential effects of target-vs-context weighting,
- perturbation families that cluster together despite very different surface appearances.

This turns the project from “artsy video edits meet brain model” into **theory-guided computational neurophenomenology**.

---

## The critical limitation

Here is the annoying but important part:

TRIBE gives you **encoding predictions**, not fitted normalization parameters.
So unless you add a downstream model, TRIBE will not directly tell you “parameter b decreased.”

There are two ways around this:

### Option A: signature matching
Use Aqil’s work to define expected neural signatures of reduced contextual suppression, then test which perturbations move TRIBE predictions in that direction.

### Option B: downstream surrogate modeling
Fit a compact interpretable model on top of TRIBE outputs—e.g. ROI-level response summaries, trajectory curvature, local-vs-global sensitivity metrics, surround-vs-target contrast metrics—to approximate latent computational axes.

Option B is cooler. Option A is safer.
Do both if you can.

---

## The version I would actually submit

### Updated workshop hypothesis
We hypothesize that psychedelic-relevant sensory phenomena are best understood as **computational shifts in contextual visual processing**, rather than generic perceptual distortion. Drawing on work by Aqil and colleagues, we predict that perturbations of figure-ground structure, local surround context, contour precision, and temporal persistence will produce dissociable changes in TRIBE-predicted cortical responses, with signatures consistent with reduced contextual suppression and altered normalization-like computations. We will use the BOLD Moments naturalistic video dataset as an open stimulus backbone, generate a preregistered perturbation space, and test which manipulations most strongly and consistently alter cortical response geometry.

---

## Tighter application draft
### Under ~300 words

We propose a preregistered open-data project using BOLD Moments and TRIBE v2 to test a ~~neuroscience-grounded~~ hypothesis about psychedelic visual phenomenology. ~~Rather than treating psychedelic-like visuals as generic “trippy” distortions~~, we draw on recent work arguing that low-level sensory changes are mechanistically meaningful and that psilocybin specifically alters **contextual visual computations**, including surround suppression and related normalization-like processes. In particular, Aqil and colleagues showed that psilocybin increases contextual illusion strength and reduces surround suppression in early visual cortex, with these effects captured by a shift in a specific computational parameter rather than broad changes in visual tuning. Our hypothesis is that naturalistic video perturbations targeting contextual structure—especially figure-ground instability, local surround interference, contour diffusion, and temporal persistence—will produce larger and more interpretable changes in TRIBE-predicted cortical responses than generic color exaggeration alone. We will use the open BOLD Moments video/fMRI resource to build a preregistered perturbation space, run TRIBE on original and edited clips, and identify low-dimensional sensory axes that best explain changes in predicted cortical response geometry. The project is low-cost (mainly compute and personnel time), fully reproducible, and designed to motivate a later human neuroimaging study.

---

## Even tighter <1500-character version

We propose a preregistered open-data project using BOLD Moments and TRIBE v2 to test a neuroscience-grounded hypothesis about psychedelic visual phenomenology. Drawing on Aqil and colleagues, we treat psychedelic visual effects not as generic distortion but as **computational shifts in contextual visual processing**. Aqil’s recent psychophysics + 7T fMRI work suggests psilocybin specifically alters contextual computations, reducing surround suppression in early visual cortex and changing a specific model parameter rather than broadly degrading perception. Our hypothesis is that naturalistic video perturbations targeting contextual structure—especially figure-ground instability, local surround interference, contour diffusion, and temporal persistence—will produce larger and more interpretable changes in TRIBE-predicted cortical responses than simple color exaggeration. Using the open BOLD Moments dataset, we will generate a preregistered perturbation space, run TRIBE on original and edited clips, and identify low-dimensional sensory axes that best explain changes in cortical response geometry. Cost is low and mostly limited to compute and personnel time.

---

## Final take

Yes — this is the missing impact angle.

The application should not be about “psychedelic-like videos.”
It should be about **computationally interpretable perturbations of contextual visual processing, inspired by psychedelic phenomenology and grounded in recent neuroscience.**
