# TRIBE v2 × BOLD Moments × Psychedelic Visual Phenomenology
## Comprehensive project wiki

## 1. Project snapshot

This project uses **TRIBE v2**, an **in-silico brain encoding model for naturalistic audiovisual stimuli**, to ask how controlled **sensory perturbations** of short naturalistic videos alter predicted cortical response structure.

The immediate goal is to build a **collaborative, preregistered workshop project** using open data. The broader goal is to use that project as a principled stepping stone toward a near-term **human validation study** using the same perturbation framework.

The project is inspired by **psychedelic visual phenomenology**, but it is not framed as a vague “trippy video” idea. The scientific object is a **computational perturbation framework**: a method for parameterizing structured alterations in sensory input, estimating their predicted cortical consequences, and identifying which perturbation families are most informative for future human neuroimaging work.

At the center of the project is a simple question:

**Which controlled changes to the sensory structure of naturalistic audiovisual stimuli produce the largest, most systematic, and most interpretable changes in predicted cortical responses?**

---

## 2. One-paragraph project description

We propose a collaborative project using **TRIBE v2**, an in-silico brain encoding model for naturalistic audiovisual stimuli, together with the **BOLD Moments** dataset to develop a computational framework for sensory perturbations in naturalistic video. Our hypothesis is that psychedelic visual phenomenology reflects structured shifts in sensory processing, including contextual visual computations, and that controlled perturbations of distinct sensory dimensions will therefore produce dissociable changes in predicted cortical response geometry. In particular, perturbations affecting figure-ground structure, local context, and temporal persistence may be especially informative. Using the open BOLD Moments fMRI dataset of short naturalistic video clips, we will generate graded perturbations of original stimuli and quantify their effects on TRIBE-predicted cortical responses. During the workshop, we aim to collaboratively develop a preregistration specifying perturbation families, clip subset, perturbation intensities, primary outcome metrics, and model-comparison criteria. This project is methodologically useful on its own and can generate a ranked shortlist of perturbation families for near-term human neuroimaging validation. Estimated cost for the workshop phase is low, consisting primarily of compute, storage, and researcher time.

---

## 3. How the project evolved

### Stage 1: initial intuition
The original intuition was exciting but broad: use TRIBE to compare neural predictions for “normal” versus more psychedelic-looking stimuli, perhaps across a parametric gradient of visual alteration, and eventually collect human data to see how those perturbations map onto brain responses and phenomenology.

This was a good starting point. What it needed was **scientific sharpening**.

### Stage 2: the first open-data anchor
An early possibility was to use **Cogitate** as the empirical substrate. That had conceptual appeal because it is open, consciousness-relevant, and high profile. But it turned out to be a poor fit for the actual computational move. The core issue was that the stimulus regime was not the same kind of naturalistic multimodal video TRIBE is best suited to model.

### Stage 3: pivot to naturalistic video
The project improved dramatically once the focus shifted toward **naturalistic audiovisual datasets**, because that aligns much better with the kind of inputs TRIBE is designed to process.

At that point the real questions became:
- Which open naturalistic fMRI/video dataset is best suited for **sensory perturbation work**?
- How do we preserve ecological validity while minimizing contamination from long-form narrative and semantic confounds?

### Stage 4: dataset comparison
Several candidate datasets were considered:

- **StudyForrest** — rich and important, but too dominated by long-range narrative structure.
- **NNDb** — powerful, but still heavily shaped by full-length movie semantics.
- **Other short audiovisual datasets** — closer in spirit, but less obvious a fit.
- **BOLD Moments** — short naturalistic clips, diverse events, strong control, rich metadata, and close alignment with TRIBE’s operating regime.

This was the turning point.

### Stage 5: the circularity issue
Once **BOLD Moments** emerged as the preferred dataset, an important concern surfaced: **TRIBE was trained in a regime closely matched to BOLD Moments**, which is good for compatibility but creates a risk of overclaiming.

The mature solution was not to abandon the dataset, but to be precise about its role. For the purposes of the workshop application, this does **not** need to dominate the pitch. It is enough to know internally that:
- BOLD Moments is an excellent substrate for **stimulus engineering and in-silico discovery**
- stronger generalization claims would later benefit from held-out data or prospective human validation

This caveat matters scientifically, but it should not swallow the application.

### Stage 6: sharpening the phenomenological angle
The next improvement was conceptual. The project was initially in danger of sounding like a “psychedelic videos” concept note. That was not strong enough.

The better framing is:
this is **not** a test of generic alteredness. It is a search over **computationally meaningful sensory perturbations**, some of which may be relevant because psychedelic states may alter **contextual visual computations** and other structured aspects of perception.

That made the project:
- more mechanistic
- more rigorous
- more interpretable
- less vulnerable to sounding hand-wavy

### Stage 7: workshop-specific refinement
The most recent refinement was to make the project fit the **actual workshop prompt** more cleanly.

The application is not just asking for an interesting idea. It is asking for a **collaborative, preregistered project to develop during the workshop**. That means the proposal should clearly communicate:
- what the hypothesis is
- what open dataset will be used
- what analysis family will be preregistered
- what concrete deliverables will be produced during the workshop
- why the project matters for consciousness science
- and what the cost profile looks like

This pushed the project toward a clearer structure without changing its scientific spine.

---

## 4. Why this route won

This route won because it solved multiple problems at once.

### It matches the actual model
TRIBE is designed for naturalistic audiovisual stimuli. Using short naturalistic video clips is a far better fit than trying to force the model onto static image paradigms or more abstract experimental designs.

### It preserves interpretability
BOLD Moments provides enough ecological richness to matter, while keeping clips short enough that perturbations remain interpretable.

### It creates a rational bridge to future data collection
The project becomes useful **before** any new human data are collected. It can identify the most promising perturbation families before time and money are spent on new experiments.

### It keeps the psychedelic component scientifically respectable
Instead of hand-waving at “trippy visuals,” the project links psychedelic phenomenology to **parameterizable sensory dimensions** and possible computational mechanisms.

### It is workshop-friendly
It is open-data based, naturally preregistrable, collaborative by design, methodologically clear, and feasible within a workshop setting.

---

## 5. The scientific core

### Primary aim
Develop a computational framework for parameterizing sensory perturbations in naturalistic audiovisual stimuli and characterizing their predicted cortical consequences.

### Secondary aim
Identify a lower-dimensional structure in the space of perturbation-induced cortical prediction changes.

### Translational aim
Use the resulting perturbation map to nominate candidate stimuli and perturbation families for near-term human neuroimaging validation.

### Workshop aim
Collaboratively produce a **preregisterable project skeleton**: perturbation taxonomy, clip-selection rules, analysis plan, and primary model-comparison criteria.

---

## 6. Core hypotheses

### Hypothesis 1
Controlled perturbations of distinct sensory dimensions in naturalistic videos will produce **dissociable changes** in TRIBE-predicted cortical response geometry.

### Hypothesis 2
These perturbation effects will organize into a **lower-dimensional latent structure**, rather than remaining a loose collection of unrelated effects.

### Hypothesis 3
Perturbations affecting **figure-ground structure**, **local context**, and **temporal persistence** may be especially informative, consistent with the possibility that psychedelic visual phenomenology involves structured changes in contextual visual processing.

### Hypothesis 4
A subset of perturbation families will emerge as especially strong candidates for near-term human neuroimaging validation.

---

## 7. The role of psychedelic phenomenology

The psychedelic component should be neither hidden nor overplayed.

It matters because psychedelic reports and experimental work suggest that perception can change in patterned ways:
- boundaries may become unstable
- figure and ground may feel less sharply segregated
- local context may alter what stands out
- persistence, echo, or recurrence may appear in perception
- sensory experience may acquire a different structural organization

This project treats those observations not as aesthetic descriptions but as a source of **testable perturbation dimensions**.

The proposal is therefore not:
**“let’s make weird videos.”**

It is:
**“let’s parameterize sensory alterations that may bear on psychedelic phenomenology and determine how they reorganize model-predicted cortical response structure.”**

---

## 8. Why this matters for consciousness science

The project matters for consciousness science because it offers a computationally explicit way to study how **altered conscious perception** might relate to structured changes in sensory input and cortical response organization.

That matters in at least three ways:

### 1. It gives altered experience a more formal handle
Rather than treating psychedelic phenomenology as purely descriptive, it asks whether specific perceptual features can be tied to interpretable stimulus dimensions.

### 2. It links phenomenology to model-based predictions
The project builds a bridge between reported experience, controlled stimulus manipulations, and predicted neural consequences.

### 3. It supports later empirical validation
Even if the workshop phase is entirely in silico, it creates a principled basis for future human studies of altered perception.

---

## 9. The role of contextual computation

Contextual computation is important, but it should not swallow the project.

It plays three jobs:

### 1. Motivation
Recent work suggests that contextual visual processing may be altered under psychedelics, which gives one principled reason to prioritize perturbations involving figure-ground relations, local surround structure, and temporal context.

### 2. Interpretation
If these perturbation families prove especially potent, contextual computation offers a principled language for understanding why.

### 3. Future hypothesis generation
A future human study can test whether participants’ phenomenology and neural data align with the perturbation families highlighted by the model.

That is exactly the right size for this part of the literature.

---

## 10. Dataset decision

### Why BOLD Moments
BOLD Moments sits in the sweet spot between:
- naturalism
- control
- short duration
- diversity of events
- metadata richness
- fit to TRIBE’s visual regime

It allows perturbations that remain interpretable and computationally tractable.

### Why not StudyForrest as the main substrate
StudyForrest is excellent, but long-form narrative structure is too dominant for a first-pass perturbation project.

### Why not Cogitate
Cogitate is conceptually interesting, but it does not match the central computational move as well as short naturalistic video data.

### How to handle the caveat
The application does not need to belabor the circularity issue. The right stance is simple:
- use BOLD Moments because it is a strong fit
- avoid overclaiming what the workshop phase alone can prove
- treat future human validation as the stronger downstream test

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
- local audiovisual mismatch
- altered synchrony
- sensory incongruence

The goal is not to generate every imaginable edit. The goal is to define a space of **graded, interpretable perturbation dimensions**.

---

## 12. Analysis strategy

One of the most important refinements in recent passes was to make the analysis language more specific without becoming bloated.

Earlier language like:
- cortical distance
- dimensionality reduction

was not wrong, but it was too generic.

The sharper analysis plan is:

### Core analysis family
- run original and perturbed clips through **TRIBE v2**
- compare predicted cortical responses across perturbation families and intensities

### Primary analysis language
- **representational similarity analysis**
- **multivariate similarity structure**
- **variance partitioning / variance decomposition across perturbation dimensions**

### Additional analytic goal
- test whether perturbation effects organize into a **lower-dimensional latent structure**

This is better because it says:
- we care about the **geometry** of predicted cortical patterns
- we care about which perturbation families explain that structure
- and we care whether those changes cluster into interpretable latent axes

That is more concrete, more preregisterable, and more legible to reviewers.

---

## 13. What should be preregistered

A major improvement in the project is that the preregistration target is now clearer.

During the workshop, the collaborative goal would be to specify:

- the initial **perturbation families**
- the exact **clip subset** or clip-selection criteria
- the **perturbation intensity levels**
- the **primary outcome metrics**
- the **model-comparison criteria**
- the criteria for ranking perturbation families for future follow-up

This matters because saying a project is “preregisterable” is weaker than saying **what, exactly, will be preregistered**.

---

## 14. Workshop-phase deliverables

A useful refinement from recent passes is to make the outputs of the workshop explicit.

### Deliverables
- a draft preregistration
- a perturbation taxonomy
- a clip-selection strategy
- a candidate analysis plan
- a ranked set of candidate perturbation families
- a clear rationale for near-term human validation

This helps the project read as something that can actually be **developed during the workshop**, rather than merely discussed.

---

## 15. Cost logic

A crucial planning insight was to separate the **workshop phase** from the **future validation phase**.

### Workshop-phase cost
Low:
- open data
- modest compute / GPU time
- storage
- researcher effort
- no new human data collection

This is what belongs in the workshop application.

### Future validation cost
A later human study would likely require:
- more serious compute
- stimulus development and piloting
- neuroimaging or behavioral data collection
- phenomenology measures
- analysis support

The application should not blur these into one budgetary object. They are not the same thing.

### Is the current cost statement good enough?
Yes. The current cost framing is strong enough for the application. It is concrete enough to sound plausible without dragging the reader into unnecessary budgeting trivia.

---

## 16. Why the project matters

### Methodological value
It creates a general framework for perturbing naturalistic stimuli in computationally interpretable ways.

### Scientific value
It asks which sensory dimensions most strongly reorganize predicted cortical response structure.

### Consciousness-science value
It offers a computational route for studying altered conscious perception in a more explicit and testable way.

### Translational value
It provides a principled route for selecting perturbation families and candidate stimuli for human neuroimaging studies.

### Field value
It gives psychedelic visual phenomenology a more formal and computational handle.

---

## 17. Risks and how they are handled

### Risk 1: the project sounds vague or aesthetic
**Response:** sharpen the language around perturbation dimensions, predicted cortical consequences, and interpretable analysis structure.

### Risk 2: the project sounds too much like generic “psychedelic visuals”
**Response:** foreground the perturbation framework and the computational logic.

### Risk 3: the analysis methods sound generic
**Response:** use representational similarity analysis, multivariate similarity structure, and variance partitioning language.

### Risk 4: the proposal does not clearly answer the application prompt
**Response:** explicitly structure the proposal around hypothesis, dataset, likely analyses, significance, and estimated cost.

### Risk 5: the proposal sounds like a future grant rather than a workshop project
**Response:** make the workshop deliverables explicit: preregistration, perturbation taxonomy, clip subset, analysis plan.

### Risk 6: the model/data fit caveat becomes a distraction
**Response:** acknowledge it internally and handle it honestly, but do not let it dominate the short application answer.

---

## 18. Final workshop response (formatted version)

### 1. Hypothesis
We propose a collaborative project using **TRIBE v2**, an in-silico brain encoding model for naturalistic audiovisual stimuli, together with the **BOLD Moments** dataset to develop a computational framework for sensory perturbations in naturalistic video. Our hypothesis is that psychedelic visual phenomenology reflects structured shifts in sensory processing, including contextual visual computations, and that controlled perturbations of distinct sensory dimensions will therefore produce dissociable changes in predicted cortical response geometry. In particular, perturbations affecting figure-ground structure, local context, and temporal persistence may be especially informative.

### 2. Dataset
We will use the open **BOLD Moments** fMRI dataset of short naturalistic video clips and generate graded perturbations of the original stimuli.

### 3. Likely analysis methods
During the workshop, we aim to collaboratively develop a preregistration specifying perturbation families, clip subset, perturbation intensities, primary outcome metrics, and model-comparison criteria. Original and perturbed clips will be passed through TRIBE v2, and perturbation effects will be quantified using representational similarity analysis, multivariate similarity structure, and variance partitioning across perturbation dimensions. We will also test whether these effects organize into a lower-dimensional latent structure.

### 4. Significance
This project provides a preregistered computational framework for linking psychedelic phenomenology to interpretable stimulus dimensions and altered conscious perception. It is methodologically useful on its own and can generate a ranked shortlist of perturbation families for near-term human neuroimaging validation.

### 5. Estimated Cost
Low for the workshop phase: open data, modest compute/GPU time, storage, and researcher effort. No new human data collection is required at this stage.

---

## 19. Optional alternate final response (single-paragraph version)

We propose a collaborative project using **TRIBE v2**, an in-silico brain encoding model for naturalistic audiovisual stimuli, together with the **BOLD Moments** dataset to develop a computational framework for sensory perturbations in naturalistic video. Our hypothesis is that psychedelic visual phenomenology reflects structured shifts in sensory processing, including contextual visual computations, and that controlled perturbations of distinct sensory dimensions will therefore produce dissociable changes in predicted cortical response geometry. In particular, perturbations affecting figure-ground structure, local context, and temporal persistence may be especially informative. Using the open BOLD Moments fMRI dataset of short naturalistic video clips, we will generate graded perturbations of original stimuli and quantify their effects on TRIBE-predicted cortical responses. During the workshop, we aim to collaboratively develop a preregistration specifying perturbation families, clip subset, perturbation intensities, primary outcome metrics, and model-comparison criteria. This project provides a computational framework for linking psychedelic phenomenology to interpretable stimulus dimensions and altered conscious perception, and can generate a ranked shortlist of perturbation families for near-term human neuroimaging validation. Estimated cost for the workshop phase is low, consisting primarily of compute, storage, and researcher time.

---

## 20. Immediate next steps

1. Decide the first perturbation families and intensity levels.
2. Define the initial BOLD Moments clip subset or clip-selection rules.
3. Specify the TRIBE inference pipeline.
4. Decide the exact primary outcome metrics.
5. Write the preregistration skeleton.
6. Decide whether the application should emphasize:
   - methodological contribution,
   - altered conscious perception,
   - psychedelic phenomenology,
   - or the bridge to future human validation most strongly.

---

## 21. Bottom line

The final project is strong because it is:
- ambitious without being ridiculous
- mechanistically motivated without overclaiming
- open-data based without being trivial
- workshop-feasible without being small
- and genuinely useful as a bridge to real human work

It started as a cool idea.

It is now a serious, preregisterable project.