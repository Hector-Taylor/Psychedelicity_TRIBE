# TRIBE v2 × BOLD Moments × Psychedelic Visual Phenomenology
## Comprehensive project wiki

## 1. Project snapshot

This project uses **TRIBE v2** as an in-silico brain encoding model to map how controlled **sensory perturbations** of naturalistic audiovisual stimuli change predicted cortical response structure. The immediate goal is to build a preregisterable, open-data project for the workshop. The broader goal is to use that project to motivate a near-term **human validation study** using the same perturbation framework.

The project is inspired by **psychedelic visual phenomenology**, but it is not framed as a vague “trippy video” idea. The sharper scientific object is a **computational perturbation framework**: a method for parameterizing alterations in sensory structure, estimating their predicted cortical consequences, and identifying which perturbation families are most informative for future human neuroimaging work.

At the center of the project is a simple question:

**Which controlled changes to the sensory structure of naturalistic stimuli produce the largest, most systematic, and most interpretable changes in predicted cortical responses?**

---

## 2. Final one-paragraph description

We propose a collaborative project using BOLD Moments and TRIBE v2 to develop a computational framework for sensory perturbations in naturalistic audiovisual stimuli. Our hypothesis is that psychedelic visual phenomenology reflects structured shifts in sensory processing, including contextual visual computations, and that controlled perturbations of distinct sensory dimensions will therefore produce dissociable changes in predicted cortical response geometry. In particular, perturbations affecting figure-ground structure, local context, and temporal persistence may be especially informative. Using the open BOLD Moments fMRI dataset of short naturalistic video clips, we will generate graded perturbations of original stimuli, run both original and perturbed clips through TRIBE v2, and quantify changes in predicted cortical responses through multivariate similarity structure and variance decomposition across perturbation dimensions. The significance of the project is methodological and translational: it provides a framework for linking psychedelic phenomenology to computationally interpretable stimulus dimensions, and it offers a principled way to select candidate stimuli for near-term human neuroimaging validation using the same perturbation space. Estimated cost for the workshop phase is minimal, consisting primarily of compute and researcher time; we are also interested in using this project to motivate a near-term human validation study built around the same stimulus framework, which would require separate follow-on support for data collection and analysis.

---

## 3. How the project evolved

### Stage 1: initial intuition
The original intuition was exciting but broad: use TRIBE to compare neural predictions for “normal” versus more psychedelic-looking stimuli, perhaps across a parametric gradient of visual alteration, and eventually collect human data to see how those perturbations map onto brain responses and phenomenology.

This core intuition was good. What needed refinement was the scientific framing.

### Stage 2: the first open-data anchor
An early possibility was to use **Cogitate** as the open-data substrate. That had some appeal because it is a high-profile, consciousness-relevant, open neuroimaging project. But it turned out to be a poor match for the actual computational idea. The key issue was that the Cogitate stimuli are not the same kind of naturalistic multimodal videos TRIBE is best suited for. Cogitate is valuable conceptually, but not ideal as the main empirical backbone for a naturalistic perturbation project.

### Stage 3: pivot to naturalistic video
The project improved dramatically once the focus shifted toward **naturalistic audiovisual datasets**, because that aligns much more closely with the domain TRIBE was trained to model. At that point the question became:

- Which open naturalistic fMRI/video dataset is the best substrate for **sensory perturbation work**?
- How do we minimize contamination from long-range narrative, emotion, and semantic prediction while preserving ecological validity?

### Stage 4: dataset comparison
Several candidate datasets were considered:

- **StudyForrest** — iconic and rich, but dominated by a long narrative arc.
- **NNDb** — broader and powerful, but still built around full-length movies and therefore heavily confounded by narrative and semantic structure.
- **Berezutskaya / short audiovisual film datasets** — closer, but still not the cleanest fit.
- **BOLD Moments** — short naturalistic clips, high event diversity, better control, rich metadata, and crucially a much closer match to TRIBE’s training regime.

This was the turning point.

### Stage 5: identifying the circularity issue
Once BOLD Moments became the preferred dataset, an important concern surfaced: **TRIBE was trained on BoldMoments**. That is good for stimulus compatibility, but dangerous for overclaiming.

The solution was not to abandon BOLD Moments. The solution was to be precise about its role:
- use BOLD Moments for **stimulus engineering** and **in-silico discovery**
- do **not** treat it as the sole confirmatory validation dataset
- use later held-out datasets or prospective human data for stronger generalization claims

That was a mature and scientifically honest resolution.

### Stage 6: sharpening the phenomenological angle
The next improvement was conceptual. The project was initially in danger of sounding like a “psychedelic videos” concept note. That was not strong enough. The literature on psychedelic visual processing, especially the work associated with Marco Aqil and colleagues, helped sharpen the motivation.

The key insight was:
the project should not be framed as a test of generic alteredness. It should be framed as a search over **computationally meaningful sensory perturbations**, some of which may be relevant because recent work suggests that psychedelic states alter **contextual visual computations**.

This made the project:
- more mechanistic
- more rigorous
- more interpretable
- and less vulnerable to sounding hand-wavy

### Stage 7: final balance
The final shape of the project preserves the original spirit while cleaning up the scientific framing:

- **methodology first**
- **psychedelic phenomenology as motivating domain**
- **contextual computation as one important mechanistic clue**
- **TRIBE as the in-silico engine**
- **BOLD Moments as the discovery substrate**
- **future human validation as the translational payoff**

That is the project.

---

## 4. Why this route won

This route won because it solved multiple problems at once.

### It matches the actual model
TRIBE is designed for naturalistic stimuli. Using short naturalistic video clips is a far better fit than trying to force the model onto static image paradigms or overly abstract experimental tasks.

### It preserves experimental control
BOLD Moments gives enough ecological richness to matter, but the clips are short enough that perturbations can be interpreted more cleanly than in full-length narrative films.

### It creates a rational bridge to future data collection
The project is useful even before any new human data are collected. It becomes a way to identify the most promising perturbations before spending time and money on new experiments.

### It keeps the psychedelic component scientifically respectable
Instead of waving at “trippy visuals,” the project links psychedelic phenomenology to parameterizable sensory dimensions and possible computational mechanisms.

### It is workshop-friendly
It is open-data based, naturally preregistrable, methodologically clear, and collaborative by design.

---

## 5. The scientific core

## Primary aim
Develop a computational framework for parameterizing sensory perturbations in naturalistic audiovisual stimuli and characterizing their predicted cortical consequences.

## Secondary aim
Identify a low-dimensional structure in the space of perturbation-induced cortical prediction changes.

## Translational aim
Use the resulting perturbation map to choose candidate stimuli for near-term human neuroimaging validation.

---

## 6. Core hypotheses

### Hypothesis 1
Controlled perturbations of distinct sensory dimensions in naturalistic videos will produce **dissociable changes** in TRIBE-predicted cortical response geometry.

### Hypothesis 2
These perturbation effects will organize into a **low-dimensional latent structure**, rather than remaining a collection of unrelated effects.

### Hypothesis 3
Perturbations affecting **figure-ground structure**, **local context**, and **temporal persistence** may be especially informative, consistent with the possibility that psychedelic visual phenomenology involves structured changes in contextual visual processing.

### Hypothesis 4
A subset of perturbations will emerge as especially promising candidates for near-term human validation.

---

## 7. The role of psychedelic phenomenology

The psychedelic component should be neither hidden nor overplayed.

It matters because psychedelic reports and experimental work suggest that perception can change in patterned ways:
- boundaries may become unstable
- figure and ground may feel less sharply segregated
- local context may alter what stands out
- persistence, echo, or recurrence may appear in perception
- sensory experience may acquire a different structural organization

This project treats those observations not as aesthetic descriptors but as a source of **testable perturbation dimensions**.

The proposal is therefore not:
“let’s make weird videos.”

It is:
“let’s parameterize sensory alterations that may bear on psychedelic phenomenology and determine how they reorganize model-predicted cortical response structure.”

---

## 8. The role of contextual computation

Contextual computation is important, but it should not swallow the project.

It plays three jobs:

### 1. Motivation
Recent work suggests that contextual visual processing may be altered under psychedelics, which gives one principled reason to prioritize perturbations involving figure-ground relations, local surround structure, and temporal context.

### 2. Interpretation
If these perturbation families prove especially potent, contextual computation offers a principled language for understanding why.

### 3. Future hypothesis generation
A future human study can test whether participants’ phenomenology and neural data align with the perturbation families highlighted by the model.

That is exactly the right size for this piece of the literature.

---

## 9. Dataset decision

## Why BOLD Moments
BOLD Moments became the optimal dataset because it sits in the sweet spot between:
- naturalism
- control
- short duration
- metadata richness
- and fit to TRIBE’s visual regime

It allows perturbations that are still interpretable.

## Why not StudyForrest as the main substrate
StudyForrest is excellent, but the narrative structure is too dominant for the first pass of this project. It may be valuable later for generalization, but not as the main discovery substrate.

## Why not Cogitate
Cogitate is conceptually interesting, but it is not the right stimulus regime for the central computational move.

## The circularity caveat
Because TRIBE was trained on BoldMoments, BOLD Moments should be treated as the **discovery substrate**, not the sole confirmatory substrate.

This is not a fatal flaw. It is simply a design fact that has to be handled honestly.

---

## 10. Project phases

## Phase A — open-data discovery
Use BOLD Moments to generate and analyze a sensory perturbation space with TRIBE.

### Deliverables
- perturbation pipeline
- preregistered analysis plan
- model-based ranking of perturbation families
- candidate stimulus shortlist

## Phase B — generalization
Assess whether the discovered perturbation axes remain meaningful in held-out naturalistic data or in later independent analyses.

### Deliverables
- generalization checks
- refined hypotheses
- stronger basis for future funding or data collection

## Phase C — prospective human validation
Run a near-term human study using the same stimulus framework.

### Deliverables
- neural data
- phenomenology mapping
- validation of selected perturbation dimensions
- stronger mechanistic interpretation

---

## 11. The perturbation framework

The perturbation space should be broad enough to matter and constrained enough to interpret.

### Core perturbation families

#### Figure-ground structure
- boundary weakening
- unstable segmentation
- local edge ownership ambiguity

#### Local context
- altered neighborhood relationships
- increased or decreased contextual salience
- local surround interference

#### Temporal persistence
- afterimage-like carryover
- motion traces
- delayed perceptual decay

#### Color and surface dynamics
- saturation modulation
- hue drift
- local chromatic instability

#### Pattern recursion
- self-similar repetition
- repeated local motifs
- nonliteral patterned echo

#### Optional audiovisual perturbations
- mismatch
- altered synchrony
- local incongruence

The idea is not to generate every possible edit. The idea is to define a space of **graded, interpretable perturbation dimensions**.

---

## 12. Analysis language we settled on

At one stage, the project was described with generic terms like:
- cortical distance
- dimensionality reduction

Those are not wrong, but they are too generic.

The sharper language that emerged was:

- **multivariate similarity structure**
- **variance decomposition across perturbation dimensions**

This is better because it says:
- we care about the geometry of the predicted cortical patterns
- and we care about which perturbation families actually explain the differences

That is clearer, less boilerplate, and closer to the real intent of the project.

---

## 13. Cost logic

A crucial planning insight was to separate the **workshop phase** from the **follow-on human-validation phase**.

## Workshop-phase cost
Minimal:
- compute
- researcher time
- storage / infrastructure
- no new human data collection

This is what belongs in the workshop application.

## Follow-on cost
This is the future project:
- more serious compute
- stimulus development and pilot testing
- human neuroimaging
- data analysis support
- possible phenomenology measures

The application should not pretend the workshop phase and the later human study are the same budgetary object. They are not.

The final cost sentence reflects this distinction clearly.

---

## 14. Why the project matters

### Methodological value
It creates a general framework for perturbing naturalistic stimuli in computationally interpretable ways.

### Scientific value
It asks which sensory dimensions most strongly reorganize predicted cortical response structure.

### Translational value
It provides a principled route for selecting stimuli for human neuroimaging studies.

### Field value
It gives psychedelic visual phenomenology a more explicit computational handle.

---

## 15. Risks and how they are handled

### Risk 1: the project sounds vague or aesthetic
**Response:** sharpen the language around perturbation dimensions, predicted cortical consequences, and interpretable analysis structure.

### Risk 2: the model fit is circular
**Response:** use BOLD Moments for discovery, not as the only validation basis.

### Risk 3: contextual computation dominates the whole pitch
**Response:** keep it as motivation and interpretation, not as the full proposal.

### Risk 4: the analysis language sounds generic
**Response:** use multivariate similarity structure and variance decomposition across perturbation dimensions.

### Risk 5: the cost line sounds unrealistic
**Response:** separate workshop cost from follow-on validation cost.

---

## 16. Final workshop response

We propose a collaborative project using BOLD Moments and TRIBE v2 to develop a computational framework for sensory perturbations in naturalistic audiovisual stimuli. Our hypothesis is that psychedelic visual phenomenology reflects structured shifts in sensory processing, including contextual visual computations, and that controlled perturbations of distinct sensory dimensions will therefore produce dissociable changes in predicted cortical response geometry. In particular, perturbations affecting figure-ground structure, local context, and temporal persistence may be especially informative. Using the open BOLD Moments fMRI dataset of short naturalistic video clips, we will generate graded perturbations of original stimuli, run both original and perturbed clips through TRIBE v2, and quantify changes in predicted cortical responses through multivariate similarity structure and variance decomposition across perturbation dimensions. The significance of the project is methodological and translational: it provides a framework for linking psychedelic phenomenology to computationally interpretable stimulus dimensions, and it offers a principled way to select candidate stimuli for near-term human neuroimaging validation using the same perturbation space. Estimated cost for the workshop phase is minimal, consisting primarily of compute and researcher time; we are also interested in using this project to motivate a near-term human validation study built around the same stimulus framework, which would require separate follow-on support for data collection and analysis.

---

## 17. Immediate next steps

1. Decide the first perturbation families and intensity levels.
2. Define the initial BOLD Moments clip subset.
3. Specify the TRIBE inference pipeline.
4. Write the preregistered hypotheses in compact form.
5. Decide whether the workshop application should emphasize:
   - methodological contribution,
   - psychedelic phenomenology,
   - or future human validation most strongly.
6. Build the follow-on funding story for the human study.

---

## 18. Bottom line

The final project is strong because it is:
- ambitious without being ridiculous
- mechanistically motivated without being overclaimed
- open-data based without being trivial
- and genuinely useful as a bridge to real human work

It began as a cool idea.
It is now a serious project.
