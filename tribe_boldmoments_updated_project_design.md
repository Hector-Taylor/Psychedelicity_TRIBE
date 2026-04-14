# TRIBE v2 × Sensory Perturbation Space × Open Naturalistic fMRI
## Updated project design and workshop-ready plan

## Executive summary

We now have a cleaner and stronger version of the project.

The core idea is to use **TRIBE v2** as an **in-silico brain-response engine** to explore a **parametric sensory perturbation space** built around short naturalistic video events. Instead of asking whether TRIBE can “detect psychedelic brain states,” we ask a sharper question:

**Which controlled perturbations of sensory dimensions—such as contour instability, color drift, temporal persistence, figure-ground ambiguity, and audiovisual incongruence—produce the largest and most structured changes in predicted cortical response geometry?**

For this purpose, the best backbone stimulus set is **BOLD Moments**, because it consists of **1,102 short 3-second naturalistic video clips across 10 participants**, was designed for dynamic visual-event research, and includes rich metadata. Short clips give us much cleaner leverage over sensory dimensions than long narrative movies do. Just as importantly, **BOLD Moments is one of the training datasets used by TRIBE v2**, which means it is unusually well matched to the model’s visual regime. The TRIBE paper lists BoldMoments among the training datasets and describes it as **1,102 3-second naturalistic video clips** shown to **10 healthy participants**. TRIBE was trained on four “deep” datasets, including BoldMoments, and tested on held-out broader datasets such as **NNDb** and **HCP**.fileciteturn0file0

That last fact is both **good** and **dangerous**.

It is **good** because:
- the stimulus format is close to what TRIBE actually learned from,
- the videos are short enough to preserve control over sensory manipulations,
- the metadata make feature decomposition much easier,
- and the clips are much less contaminated by plot and long-range narrative than full movies are.

It is **dangerous** because:
- if we use BOLD Moments human fMRI as our main validation target for TRIBE, we are no longer in a clean “out-of-sample” setting,
- and any claim that “TRIBE predicts the human data well” will be partly inflated by the fact that this dataset contributed to training.

So the right stance is:

**Use BOLD Moments for stimulus engineering and in-silico perturbation search.  
Do not use BOLD Moments as the sole confirmatory human-validation dataset.**

That is the grown-up answer.

The clean project architecture is therefore a **two-layer design**:

1. **Stimulus engineering / model-discovery layer**  
   Use BOLD Moments to build and search the perturbation space with TRIBE.

2. **Confirmatory validation layer**  
   Use a dataset that TRIBE held out for testing—such as **NNDb** or **HCP movie data**—or a later prospective human dataset, to test whether the discovered sensory axes generalize beyond the training regime. In the TRIBE paper, **NNDb** and **HCP** are explicitly listed as test datasets, not training datasets.fileciteturn0file0

That gives us:
- maximal fit to the model for the perturbation search,
- a defensible answer to the “is this circular?” question,
- and a compelling story for a follow-up human study.

---

## 1. Final project concept

### One-sentence version
Build a **computational sensory-perturbation atlas** by applying controlled, phenomenology-inspired transformations to short naturalistic videos and using TRIBE v2 to map which perturbations most strongly alter predicted cortical response geometry.

### Cleaner theoretical framing
This is **not** a direct assay of psychedelic drug states.

It is a study of **altered perceptual structure**. Psychedelic phenomenology motivates the perturbation dimensions, but the scientific object is the structure of the stimulus and its predicted effect on brain responses.

That is a stronger framing anyway.

---

## 2. Why BOLD Moments is the optimal stimulus backbone

The BOLD Moments dataset is the best fit for this project because it optimizes the three things we care about most:

### A. It matches the sensory logic of the project
The BOLD Moments paper describes the dataset as **whole-brain fMRI responses to over 1,000 short (3 s) naturalistic video clips of visual events across ten human subjects**. It also argues that **short naturalistic videos strike a good balance between ecological validity and experimental control**, which is exactly the sweet spot for our perturbation design.citeturn281571view1

That means we can perturb:
- local motion structure,
- contour stability,
- color dynamics,
- temporal persistence,
- ambiguity,
- audiovisual coupling,

without everything being dominated by long-range semantics and narrative memory.

### B. It is close to TRIBE’s actual training distribution
TRIBE’s methods section lists **BoldMoments** among the datasets used for training, alongside CNeuroMod, LeBel2023, and Wen2017. BoldMoments is described there as **10 healthy participants watching 1,102 3-second video clips** sampled to contain movement, natural context, and a broad range of events.fileciteturn0file0

That is a huge advantage for the model-discovery phase.

### C. It comes with rich metadata
The BOLD Moments dataset includes extensive metadata and human annotations, including descriptions of objects, scenes, actions, text descriptions, spoken transcription, and memorability-related measures. The paper emphasizes that these metadata help relate brain activity to meaningful aspects of visual events, and OpenNeuro/Aude Oliva’s dataset page summarizes those annotations directly.citeturn281571view1turn809266search20

That gives us a way to separate:
- low-level sensory perturbation,
- event semantics,
- memorability,
- and other content-level confounds.

---

## 3. Is it a problem that TRIBE was trained on BOLD Moments?

### Short answer
**Yes, if we are sloppy. No, if we use it correctly.**

### Why it is good
It is good because it means BOLD Moments is probably the best open stimulus domain for probing TRIBE with sensory perturbations. The model already learned from short naturalistic event clips, so it is less likely to behave bizarrely or purely out-of-distribution when we create moderate perturbations around them. TRIBE is explicitly a model for **naturalistic stimuli (video, audio, text)** and predicts average-subject fMRI responses on the cortical surface.citeturn281571view3turn809266search5

### Why it is a problem
It becomes a problem if we try to claim:

> “TRIBE predicts BOLD Moments human fMRI, therefore our results prove generalizable brain alignment.”

That is too self-flattering. Because BOLD Moments was used during training, that comparison is not fully independent. The BOLD Moments paper itself has train/test video splits within the dataset, and OpenNeuro notes that subjects saw the **1,000-video training set 3 times** and the **102-video test set 10 times**. But that is still an internal dataset split, not an entirely independent held-out dataset in the way **NNDb** or **HCP** are for TRIBE.citeturn809266search4turn281571view1turn0file0

### The right solution
Treat BOLD Moments as the **perturbation-space discovery substrate**, not the sole confirmatory substrate.

Concretely:
- **Discovery** on BOLD Moments
- **Generalization check** on an open dataset TRIBE did not train on
- **Prospective human validation** later

That is defensible.

---

## 4. Project architecture

## Phase A — In-silico perturbation search on BOLD Moments
Goal: identify which sensory perturbations most strongly alter TRIBE-predicted cortical response geometry.

### Inputs
- Original BOLD Moments clips
- Optional subset selection by semantic or visual class
- Controlled perturbation pipeline

### Perturbation dimensions
We should start with a compact, interpretable set:

1. **Contour instability**  
   subtle local edge waviness, surface breathing, texture ripple

2. **Color instability**  
   saturation modulation, hue drift, localized chromatic shift

3. **Temporal persistence**  
   motion trails, afterimage-like carryover, delayed frame decay

4. **Temporal warping**  
   micro-fluctuations in local timing, pulse-like nonlinearity in temporal flow

5. **Figure-ground ambiguity**  
   softened segmentation, partial blending, unstable foreground boundaries

6. **Pattern recursion**  
   local repetition, kaleidoscopic echoes, self-similar motif emergence

7. **Audiovisual congruence / incongruence**  
   only where audio is present and useful

### Output of Phase A
A ranked and structured perturbation manifold:
- which dimensions matter most,
- which combinations are synergistic,
- which perturbations produce broad vs selective cortical shifts,
- which perturbations are subtle but high-impact.

---

## Phase B — Open-data generalization / confirmatory validation
Goal: test whether the sensory axes discovered in Phase A generalize beyond BOLD Moments.

### Best validation datasets
The cleanest candidates are datasets that the TRIBE paper held out for testing:
- **NNDb**  
- **HCP movie data**

TRIBE’s dataset table lists both **NNDb** and **HCP** under **Test**, not Train.fileciteturn0file0

### Why this matters
If the same sensory metrics discovered on BOLD Moments also organize predictions or neural-response relationships on a truly held-out naturalistic dataset, that is far more convincing than a within-training-domain story.

### What this phase can test
- whether discovered perturbation-sensitive axes generalize,
- whether sensory-dimension scores explain variance beyond broad semantic content,
- whether the same axes show reproducible cortical signatures across datasets.

Important caveat:
these datasets will not contain our transformed versions. So this phase is **not** “people saw the perturbed clips.” It is:
- learn sensory axes on BOLD Moments,
- compute analogous features on held-out naturalistic clips,
- ask whether those axes remain useful.

That is still a strong validation.

---

## Phase C — Prospective human follow-up
Goal: collect new fMRI / EEG / fNIRS data on a curated subset of perturbations.

### Why this is the real payoff
This is where we stop living off borrowed datasets and actually test whether:
- model-ranked perturbations scale with subjective experience,
- selected sensory dimensions drive measurable neural differences,
- and phenomenology-inspired manipulations interact with real human perception the way we think they do.

This is the future paper the workshop project should motivate.

---

## 5. Exact analysis plan

## Step 1: Curate clip subset
Select a BOLD Moments subset that spans event types while keeping semantic diversity manageable.

Potential strategy:
- 200–300 clips for initial search
- balanced across action-rich vs low-action scenes
- avoid absurdly noisy or semantically bizarre clips at first

Use metadata to stratify:
- action density,
- social content,
- scene complexity,
- memorability,
- text richness.

## Step 2: Build the perturbation engine
For each source clip, generate a factorial or quasi-factorial set of perturbations.

Start smaller than your ego wants.
A good first pass is:
- 4–5 dimensions
- 3–4 intensity levels each
- efficient sampling rather than full crossing

That keeps compute sane.

## Step 3: Run TRIBE on originals and perturbations
TRIBE predicts average-subject cortical responses to naturalistic video/audio/text and outputs predictions on the **fsaverage5 cortical mesh** with a **5-second lag correction**.citeturn281571view3turn0file0

For each clip variant, extract:
- whole-cortex prediction matrix,
- ROI summaries,
- temporal trajectory features.

## Step 4: Quantify perturbation effects
Primary derived measures:
- whole-cortex distance from original
- ROI-specific delta
- trajectory curvature
- temporal entropy / instability
- cross-clip clustering by perturbation family
- interaction effects across sensory dimensions

## Step 5: Build latent sensory axes
Use dimensionality reduction or interpretable regression to discover:
- common perturbation manifolds,
- convergent axes across different edit families,
- low-dimensional “sensory perturbation scores.”

## Step 6: Relate to BOLD Moments metadata
Ask whether model-sensitive perturbations are independent of or entangled with:
- action labels
- scene labels
- object labels
- memorability
- textual descriptions

This is where the metadata earn their keep.

## Step 7: Held-out generalization
Project the discovered axes onto a held-out naturalistic dataset such as NNDb or HCP and test whether they remain explanatory or structurally meaningful.

## Step 8: Select stimuli for future human work
Choose a compact stimulus set:
- low perturbation controls
- high perturbation exemplars
- interaction cases
- “minimal visible change, maximal predicted brain change” clips

That last bucket is especially cool.

---

## 6. Core hypotheses

### Hypothesis 1
Sensory perturbation dimensions will produce **dissociable** changes in predicted cortical response geometry rather than a single monotonic “more trippy” effect.

### Hypothesis 2
Perturbations involving **contour instability**, **temporal persistence**, and **figure-ground ambiguity** will produce larger and more distributed cortical shifts than simple color exaggeration alone.

### Hypothesis 3
Distinct perturbation families may converge on shared low-dimensional response manifolds, suggesting common latent axes of altered perceptual structure.

### Hypothesis 4
The sensory axes discovered on BOLD Moments will show at least partial generalization to held-out naturalistic movie datasets not used to train TRIBE.

### Hypothesis 5
A small subset of perturbations will produce disproportionately large predicted cortical changes despite only subtle visible modifications.

That is the sexy hypothesis.

---

## 7. Why this is significant

This project matters for at least four reasons.

### A. It makes “psychedelic-like” perception scientifically legible
Instead of treating altered visual phenomenology as vague vibes, we decompose it into controllable sensory dimensions.

### B. It uses TRIBE for what it is actually good at
TRIBE is a multimodal brain encoding model for naturalistic stimuli, not a mystical decoder of consciousness. The model is explicitly positioned as a tool for **in-silico experimentation** and pre-screening of neuroimaging protocols.fileciteturn0file0turn281571view3

### C. It creates a rational bridge to future human studies
Rather than collecting human data blindly, we can use model-based screening to identify the most promising perturbations first.

### D. It is workshop-friendly
It is hypothesis-driven, based on open datasets, reproducible, and naturally suited for preregistration and future collaboration. The workshop explicitly asks teams to formulate a clear scientific question using existing open datasets and to leave with a preregistered plan specifying hypotheses, dataset, and analysis pipeline.citeturn281571view0turn281571view4

---

## 8. Practical risks and how to handle them

### Risk 1: Circularity from using BOLD Moments
**Fix:** do not treat BOLD Moments as the sole confirmatory human-validation dataset.

### Risk 2: Perturbations become too out-of-distribution
**Fix:** use graded intensities and explicitly compare mild, moderate, and extreme edits.

### Risk 3: Semantic content still drives everything
**Fix:** use metadata-based controls and within-clip comparisons.

### Risk 4: The project sprawls
**Fix:** preregister a compact first-pass perturbation family and a limited set of primary metrics.

### Risk 5: We overclaim “psychedelic neuroscience”
**Fix:** frame the project as **phenomenology-inspired sensory perturbation modeling**, with psychedelic relevance as the motivating domain.

---

## 9. Best workshop-facing version of the project

For the workshop, the cleanest proposal is:

- **Open dataset:** BOLD Moments
- **Primary objective:** discover a low-dimensional sensory perturbation space using TRIBE
- **Secondary objective:** assess whether discovered axes generalize to held-out naturalistic datasets
- **Deliverable:** OSF-preregistered analysis plan plus open code for perturbation generation and model analysis

This is honest and strong.

---

## 10. Workshop application blurb draft
### Under ~300 words

We propose a preregistered open-data project using the BOLD Moments fMRI dataset to develop a computational map of sensory perturbations in naturalistic video perception. Our hypothesis is that controlled perturbations of specific sensory dimensions—especially contour instability, temporal persistence, figure-ground ambiguity, and color instability—will produce dissociable shifts in predicted cortical response geometry, rather than a single undifferentiated “more altered” effect. We will use the open BOLD Moments dataset, which contains whole-brain fMRI responses to 1,102 short 3-second naturalistic video clips across 10 participants, as the backbone stimulus set. Using TRIBE v2, a multimodal brain-encoding model trained on naturalistic video/audio/text, we will generate predicted cortical responses for original clips and systematically perturbed variants. Planned analyses include whole-cortex distance metrics, ROI-wise response shifts, temporal trajectory geometry, dimensionality reduction, and interaction modeling across perturbation dimensions. We will also use the dataset’s rich metadata to control for scene, action, object, and memorability-related confounds. The significance of the project is twofold: first, it offers a principled way to decompose altered perceptual structure into testable sensory dimensions; second, it provides a rational basis for selecting stimuli for future human experiments on altered perception and consciousness. Estimated cost for the workshop phase is low, consisting primarily of compute and storage; we estimate roughly $300–$1,000 depending on local GPU use versus cloud inference.

---

## 11. Even tighter <1500-character version

We propose an open-data project using the BOLD Moments fMRI dataset to map how controlled sensory perturbations alter model-predicted brain responses during naturalistic event perception. Our hypothesis is that perturbations of contour stability, temporal persistence, figure-ground ambiguity, and color dynamics will produce dissociable shifts in cortical response geometry, rather than a single undifferentiated “more altered” effect. We will use BOLD Moments (1,102 short 3-second naturalistic videos; 10 participants) as the stimulus backbone and apply a preregistered perturbation pipeline to generate controlled variants. Using TRIBE v2, we will estimate cortical responses to original and perturbed clips and analyze whole-cortex distances, ROI-wise shifts, temporal trajectory structure, and low-dimensional manifolds of perturbation effects. We will use BOLD Moments metadata to control for confounds related to actions, scenes, objects, and memorability. The project is significant because it offers a principled framework for decomposing altered perceptual structure into testable sensory dimensions and for selecting candidate stimuli for later human studies of altered perception and consciousness. Estimated workshop-phase cost is low, mainly compute/storage, roughly $300–$1,000.

---

## 12. Final recommendation

Move forward with this design.

But be disciplined about one thing:
**BOLD Moments is the right dataset for discovery, not the whole story for validation.**

That is not a weakness. It is just the honest structure of a good project.
