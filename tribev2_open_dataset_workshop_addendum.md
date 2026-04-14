# TRIBE v2 × Open Consciousness Data: Workshop-Fit Addendum

## Why this addendum exists

The Consciousness Commons workshop is not just asking for a cool idea. It is asking for a project that is **explicitly grounded in an openly available dataset**, built with a reproducible analysis plan, and suitable for OSF preregistration and FAIR reuse. The workshop materials say participating teams should formulate a hypothesis-driven project using **existing open datasets**, develop a rigorous analysis plan, and produce an OSF preregistration; prize eligibility also requires that the project be **based on an openly available dataset at the time of submission** and demonstrate FAIR data reuse. citeturn778667view0turn168789view0turn838684search2

That means the right move is to **split the broader TRIBE v2 psychedelic-stimuli program into two layers**:

1. **Workshop-compatible open-data project:** a hypothesis-driven reuse study based on a currently open consciousness dataset.
2. **Future extension:** the full prospective data-collection project using psychedelic-like videos and new neural recordings.

This is not a compromise. It is actually cleaner.

---

## The blunt truth

Your original idea is strong, but in its raw form it is **not yet workshop-perfect**, because it is mainly a **new stimulus-generation and future data-collection concept**. The workshop wants an **open dataset now**. citeturn168789view0turn778667view0

So the smart version is:

> Use the workshop application to propose an **open-data validation project** that extracts a “computational psychedelicity” or “perceptual perturbation” metric from stimuli and tests whether that metric predicts neural signatures in an openly available consciousness dataset.

That gives you a legitimate open-science project now, while preserving the larger psychedelic-video agenda for later.

---

## Best dataset choice right now

### Primary recommendation: Cogitate open iEEG dataset

The cleanest currently open fit is the **Cogitate open multi-center iEEG dataset**. According to the Scientific Data release, it includes intracranial EEG from **38 patients** across **three research centers**, collected under a standardized protocol designed to test competing theories of consciousness. Participants viewed suprathreshold visual stimuli from **four categories** — **faces, objects, letters, and false fonts** — presented at **three orientations** and **three durations**, with behavioral, eye-tracking, and electrode reconstruction data included. The dataset is de-identified, converted to **BIDS**, and comes with code for preprocessing and analysis. citeturn296952view2turn838684search0

That is exactly the kind of dataset the workshop is pointing people toward: open, consciousness-relevant, BIDS-structured, and computationally tractable. The workshop materials also explicitly mention Cogitate datasets and note that brainlife.io provides free compute resources and hosts Cogitate data in an accessible BIDS environment. citeturn778667view0turn838684search2

### Why this is the best fit

Because it lets you ask a real consciousness question using a real open dataset, instead of waving vaguely at “future data we’ll collect later.” Also: iEEG is high signal, high prestige, and less mushy than pretending weak fNIRS correlations will save you.

---

## The key reframing

Your original plan was:

> normal video vs psychedelic-edited video, then TRIBE v2, then maybe collect data.

For the workshop, the best reframing is:

> derive a **stimulus perturbation metric** from phenomenology-inspired transformations, then test whether that metric predicts neural signatures of conscious visual processing in an open consciousness dataset.

That is the bridge.

---

## The project I would actually pitch

## Working workshop title

**Stimulus Perturbation Geometry and Conscious Visual Processing: An Open-Data Test Using the Cogitate iEEG Dataset**

## One-sentence pitch

We will derive a computational metric of phenomenology-inspired perceptual perturbation from controlled transformations of visual stimuli and test whether this metric predicts the strength, distribution, or temporal profile of conscious visual processing signals in the open Cogitate iEEG dataset. 

---

## Why this still preserves your psychedelic angle

Because the core intellectual move survives:

- You are still interested in **psychedelic-like phenomenology**.
- You are still defining a **parameterized perceptual perturbation space**.
- You are still using a model-driven or feature-driven approach rather than a dumb binary “trippy vs normal” contrast.
- You are just testing the framework first on **open consciousness data** rather than on your own future custom dataset.

That is not a retreat. That is a proper launchpad.

---

## The most defensible open-data version

### Project logic

1. Start from the open Cogitate stimulus structure: visual category contrasts, visibility/task-relevance structure, timing, and high-quality iEEG.
2. Build a **perturbation engine** that applies controlled phenomenology-inspired edits to matched image sets or reconstructed stimulus analogues.
3. Use those perturbations to derive per-stimulus features such as:
   - contour instability
   - color instability
   - pattern recursion
   - temporal persistence proxies
   - semantic destabilization
4. Reduce these features into one or more compact metrics:
   - perturbation magnitude
   - perceptual instability index
   - computational psychedelicity index
5. Ask whether those metrics predict:
   - stronger category decodability
   - altered temporal dynamics
   - broader recruitment across electrodes/regions
   - differences in task-relevant versus task-irrelevant processing
   - interaction with stimulus duration or category

The crucial point is that the **open dataset supplies the neural data**, while your transformation pipeline supplies the **hypothesis-generating stimulus-space model**.

---

## What exactly you can do with the Cogitate iEEG dataset

The Cogitate iEEG release includes:
- visual stimulus categories,
- multiple stimulus durations,
- task relevance manipulations,
- behavioral performance,
- eye tracking,
- electrode reconstruction,
- preprocessing/analysis code,
- and BIDS formatting for reproducible reuse. citeturn296952view2turn838684search0

That means you can test questions like:

### Option A: category sensitivity
Do stimuli or matched image exemplars with higher perturbation scores yield stronger or more prolonged category-selective neural responses?

### Option B: temporal thresholding
Do perturbation-sensitive stimulus features interact with stimulus duration, suggesting that some feature classes gain access to conscious processing more efficiently than others?

### Option C: task relevance
Are perturbation-linked stimulus properties more strongly expressed when stimuli are task-relevant than when they are task-irrelevant?

### Option D: posterior versus distributed effects
Do perturbation metrics preferentially relate to posterior category-selective responses, or to broader distributed signatures?

That last one is especially workshop-friendly because Cogitate was built to test contrasting consciousness-theory predictions using fMRI, M-EEG, and iEEG. citeturn296952view0turn296952view2

---

## The one problem you need to admit honestly

The Cogitate open iEEG dataset does **not** contain psychedelic videos. It contains a controlled visual consciousness paradigm with image categories and task structure. citeturn296952view2turn296952view0

So your pitch should not pretend otherwise.

Instead, say this plainly:

> We use open consciousness data to test whether a computationally defined perceptual perturbation framework captures neural response properties relevant to conscious visual processing. This open-data stage is intended as a principled precursor to future work using naturalistic psychedelic-style videos and new neural recordings.

That sentence saves the whole thing.

---

## Two realistic routes

## Route 1: Conservative and strongest for acceptance

### Dataset
Cogitate open iEEG.

### Project
Use open neural data only. Build perturbation metrics from matched or surrogate stimulus sets representing the same categories as the Cogitate paradigm.

### Main claim
Not “psychedelic neuroscience” directly, but:
**a computational altered-perception framework can be tested against open consciousness data.**

### Why this route is strong
- It satisfies the workshop cleanly.
- It is easy to preregister.
- It is hard for reviewers to call bullshit.

---

## Route 2: Slightly bolder and cooler

### Dataset
Cogitate open iEEG plus a companion open visual stimulus set.

Possible companion sources could be openly licensed face/object image corpora or naturalistic image/video sets used only for feature extraction and matched transformations. The open dataset doing the heavy scientific lifting for the workshop would still be Cogitate. 

### Project
Learn a perturbation manifold on an open visual corpus, then project Cogitate stimulus categories into that feature space and test whether neural signatures scale with that projection.

### Why this route is interesting
It preserves more of the original computational ambition.

### Why this route is riskier
It is easier to make it sound too complicated and underpowered if you are not brutally clear.

---

## The strongest hypotheses for the workshop

Here are hypotheses that are sharp, testable, and not overcooked.

### Hypothesis 1
Stimulus perturbation metrics derived from phenomenology-inspired transformations will explain variance in neural response strength and/or duration within category-selective iEEG signals beyond coarse stimulus category labels alone. 

### Hypothesis 2
Perturbation metrics linked to contour instability, recursion, and perceptual ambiguity will show stronger relationships with sustained or distributed neural responses than simple color exaggeration metrics. 

### Hypothesis 3
Perturbation-sensitive features will interact with stimulus duration, such that some classes of visual perturbation are associated with more robust neural differentiation at shorter presentation durations.

### Hypothesis 4
If perturbation metrics capture aspects of access-relevant visual processing, their explanatory value should differ across task-relevant and task-irrelevant conditions.

Those are sane. They do not promise magic.

---

## A clean preregistration structure

The workshop wants teams to leave with a preregistered plan on OSF. citeturn778667view0turn168789view0

So your project should already sound like a preregistration.

### Preregistered components

#### 1. Research question
Can a computational metric of phenomenology-inspired perceptual perturbation explain neural signatures of conscious visual processing in an openly available consciousness dataset?

#### 2. Dataset
Cogitate open iEEG dataset, BIDS-formatted, with associated behavioral and eye-tracking data. citeturn296952view2turn838684search2

#### 3. Planned predictors
- stimulus category
- duration
- task relevance
- perturbation magnitude
- perturbation subdimensions

#### 4. Planned outcomes
- amplitude or decoding strength of category-selective neural responses
- temporal extent / persistence of responses
- electrode-level spatial distribution
- task-condition interactions

#### 5. Planned controls
- category label
- duration
- subject/site
- electrode coverage
- eye-movement covariates where feasible

#### 6. Reproducibility outputs
- public OSF preregistration
- open analysis code
- containerized or notebook-based workflow
- DOI-minted code release
- explicit data provenance / PIDs / ORCIDs as required by the workshop prize criteria. citeturn168789view0

---

## FAIR/open-science language for the application

You should absolutely say some version of this:

> Our proposed workshop project is intentionally designed around existing open consciousness data. We will reuse the openly available Cogitate iEEG dataset in BIDS format, leverage shared preprocessing resources and documented analysis code, preregister the full analysis plan on OSF, and release all derived code and metadata in a FAIR, reusable form aligned with the workshop’s emphasis on reproducible science. citeturn778667view0turn168789view0turn838684search2

That hits their checkbox cluster in one shot.

---

## How to explain the psychedelic connection without sounding unserious

Use this framing:

> Psychedelic phenomenology provides the conceptual inspiration for the perturbation space, but the workshop project itself is a theory-driven open-data study of conscious visual processing. Our goal is to determine whether computationally defined dimensions of altered perceptual structure map onto neural signatures in an existing open consciousness dataset. This open-data phase would then motivate a future prospective study using naturalistic psychedelic-style videos and newly collected neural data.

That sounds like adults are in the room.

---

## What not to do

Do **not** say:
- “We will use Cogitate to study psychedelic states.”
- “The dataset contains psychedelic-like stimuli.”
- “TRIBE v2 can directly infer psychedelic consciousness from open iEEG.”
- “We will validate psychedelic brain states with task-irrelevant object images.”

That would be unserious, and they will smell it.

---

## My actual recommendation

For the workshop application, pitch the project as:

### Final workshop-ready title
**Phenomenology-Inspired Stimulus Perturbation Metrics as Predictors of Conscious Visual Processing in the Open Cogitate iEEG Dataset**

### Final workshop-ready abstract
We propose an open-data project testing whether computationally defined dimensions of perceptual perturbation predict neural signatures of conscious visual processing. Using the openly available Cogitate intracranial EEG dataset — a large, BIDS-formatted, multi-center dataset collected to study conscious visual perception — we will examine whether stimulus perturbation metrics derived from controlled, phenomenology-inspired image transformations explain variance in neural response strength, temporal persistence, and spatial distribution beyond coarse stimulus category labels alone. Our perturbation framework is inspired by altered perceptual phenomenology, including contour instability, recursion, ambiguity, and temporal persistence, but the project is explicitly framed as a theory-driven open-data study of visual consciousness rather than a direct assay of pharmacological psychedelic states. The project is designed for full reproducibility, including preregistration on OSF, open analysis code, and FAIR reuse of shared datasets.

That is tight. That works.

---

## Best one-line strategy

Use the workshop to validate your **computational altered-perception framework on open consciousness data**, then use that result as the springboard for the full TRIBE v2 psychedelic-video study later.

That is the move.
