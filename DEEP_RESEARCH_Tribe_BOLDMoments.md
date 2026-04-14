# TRIBE v2 × BOLD Moments × Psychedelic Visual Phenomenology

## Project thesis and what would count as a real win

This project is well-posed because it treats “psychedelic-ish” not as an aesthetic, but as a hypothesis generator for **parameterized sensory operators**—and then measures what those operators do to a **brain-encoding model’s predicted cortical response geometry**.

Technically, the workflow is straightforward:

- Run original clips and **graded perturbations** through TRIBE v2 (predicted responses are on the **fsaverage5 cortical surface** at ~20k vertices and are shifted ~5 seconds earlier to compensate for hemodynamic lag). citeturn60view0turn20view0  
- Use the **BOLD Moments** stimulus regime (1102 naturalistic 3 s videos across 10 subjects; high repeat structure; rich metadata) as the open substrate for stimulus engineering. citeturn59view1turn61view0  
- Quantify perturbation effects with geometry-first tools (RSA / RDMs, variance partitioning, latent axes).

A “real win” in the workshop phase is not “we found trippy changes.” A win is an **ordered perturbation shortlist** that is:
1) large-effect and consistent across clips,  
2) *dissociable* across perturbation families (not just “everything moves early visual cortex”),  
3) compressible into a small number of latent axes (“perturbation atlas”),  
4) explicitly usable as a stimulus-selection engine for a near-term human follow-up.

That is a coherent stepping-stone and it’s workshop-feasible because the deliverables are preregistrable and do not require new data.

## What already exists and where your project sits in that landscape

Your exact pipeline (TRIBE v2 + BOLD Moments + systematic perturbation library + ranking/latent structure + preregistered workshop deliverable) is **not something I found as a single prior package**. But the *components* all have strong precedents, and that’s good news: it means reviewers will recognize the logic, while you can still claim novelty in the synthesis.

### Naturalistic short-video fMRI + perturbation-like analyses already exist

The BOLD Moments dataset paper itself does something very close in spirit to “controlled stimulus manipulation,” just not in your psychedelic-motivated space: it uses **frame-order shuffling** as a test of whether temporal order matters for predicting fMRI responses (if prediction drops with shuffled frames, the cortical responses preserve temporal order information). citeturn59view2turn59view1  

It also explicitly motivates short (3 s) events as a sweet spot between still images and long movies, and it provides detailed experimental structure and preprocessing variants (including a version that estimates single-trial betas with GLMsingle). citeturn59view1turn59view3  

So: “perturb the stimulus; see what happens to cortical responses/predictions” is already an accepted move in the immediate neighborhood of your chosen dataset.

### Multimodal brain encoding models are already being used as in-silico testbeds

TRIBE (v1) already laid the groundwork: a tri-modal model that combines pretrained text/audio/video representations and a transformer to predict whole-brain fMRI responses, and it explicitly frames the approach as a step toward integrative models of brain representation. citeturn52view0  

TRIBE v2’s public docs describe it as a multimodal encoding model that predicts fMRI responses for naturalistic video/audio/text and maps to cortical surface space; the released inference API makes it easy to treat “stimulus → predicted cortex” as a callable function for systematic experiments. citeturn60view0turn20view0  

This is directly aligned with the broader “foundation model of neural activity enables essentially unlimited *in silico* experiments” idea that has started to appear explicitly in high-profile work—along with an important warning: models trained on naturalistic stimulus distributions often **struggle to generalize to synthetic/parametric stimuli**, so generalization needs to be treated as an empirical question, not assumed. citeturn27view0  

That warning matters for you because your perturbations occupy a spectrum from “naturalistic but altered” to “semi-synthetic.”

### Model-driven stimulus synthesis and “metamer” thinking are close cousins

Your perturbations are conceptually similar to two established families of work:

- **Closed-loop / model-driven stimulus synthesis** to probe what a representation “cares about.” For example, work that uses generative models + search procedures to evolve images that maximize neural firing in primate visual cortex is an existence proof that “stimulus engineering guided by a model” can yield interpretable discoveries about coding. citeturn44view2turn45search0  
- **Metamers**: physically different stimuli that are perceptually indistinguishable, used to identify what information a system discards. That logic (“hold X constant, vary Y, and see where the representation breaks”) is extremely compatible with a perturbation atlas mindset. citeturn47search0  
- A modern cautionary update: model metamers can reveal **idiosyncratic invariances** in neural networks that do not match humans, and “standard brain prediction metrics” may miss these mismatches. That’s directly relevant if you ever want to argue that TRIBE-based perturbation rankings are likely to transfer to human phenomenology without validation. citeturn44view0  

### Psychedelic-like video transformations already have a concrete precedent

The **Hallucination Machine** is basically a historical antecedent to your framing—except it targeted phenomenology directly rather than cortical encoding geometry. It applied a DeepDream-like transformation to panoramic videos in VR, showed that it induces subjective reports qualitatively similar to psychedelic experiences on multiple questionnaire dimensions, and emphasized that the transformation is highly parameterizable. citeturn40view0  

This is valuable precedent for reviewers because it shows that “parameterized transformations of naturalistic video” has already been taken seriously as a scientific tool in consciousness research—just not yet coupled to a modern fMRI foundation encoder and a preregistered perturbation taxonomy.

## Psychedelic vision literature that most cleanly supports your perturbation axes

If you want the project to feel mechanistic (not vibes), anchor perturbation families in the subset of psychedelic research that makes **specific, testable claims about visual computation**—especially contextual modulation and temporal dynamics.

### Contextual computation is not hand-waving anymore

A 2025 Nature Communications study explicitly tested psilocybin’s effects on **contextual perception and contextual neural responses**. Behaviorally, psilocybin increased the magnitude of the **Ebbinghaus illusion** (context-dependent size perception). citeturn32view0  

Neurally (7T), it found psilocybin reduced **surround suppression** in early visual field maps (V1/V2/V3) in timecourses where activation magnitude was otherwise similar—i.e., a relatively specific change to contextual modulation rather than a global amplitude shift. citeturn32view0  

That maps cleanly onto your “local context / figure-ground” perturbation focus and gives you a principled reason to prioritize operators that manipulate surround structure, segmentation cues, and local competition.

### There is real disagreement in the literature—and you can use it

A psychophysics pilot RCT at high-dose psilocybin (25 mg) reported **stronger** perceptual surround suppression of contrast under psilocybin than placebo, and subjective visual intensity correlated with suppression magnitude. citeturn37view0  

So you have a built-in “contrast set”:
- fMRI contextual modulation reduced in early visual cortex at lower doses in one study, citeturn32view0  
- perceptual surround suppression increased at high dose in another. citeturn37view0  

Rather than treating this as a nuisance, you can turn it into a design advantage: your perturbation atlas can deliberately include **operators that are predicted to move contextual modulation in opposite directions**, and later human validation can directly adjudicate which axis is phenomenologically and neurally relevant under which dosing/task conditions.

### Preclinical work nails both context and time

In awake mouse V1, a hallucinogenic 5‑HT2A agonist (DOI) produced:
- reduced sensory response gain,  
- reduced surround suppression (contextual modulation), and  
- altered temporal dynamics,  
while leaving basic retinotopy and tuning largely intact. citeturn39view0  

That is almost a perfect biological “permission structure” for your operator families: you’re not making up figure-ground/context/time as psychedelic-relevant dimensions; they’re explicitly implicated at the level of cortical computations.

### Early visual geometry changes show up in humans too

Inhaled DMT has been linked to changes in early visual cortex population receptive fields: mean pRF sizes in V1 increased in peripheral visual field under active condition, with an interpretation tied to tunnel vision / field blurring and gain control mechanisms. citeturn39view1  

Even if your workshop project stays in silico, this tells you that “alter the effective integration window / spatial pooling footprint” is not a random perturbation axis.

### Psychedelics and visual imagery plausibly involve altered gain/connectivity

A Molecular Psychiatry paper on psilocybin and eyes-closed imagery used effective connectivity modeling across visual and associative regions and interprets results as changes in sensitivity/gain and top-down vs bottom-up balance relevant to imagery generation. citeturn31view0  

You don’t need to turn your project into a connectivity story, but citing this gives you justification for treating “contextual computation” and “persistence/imagery-like carryover” as mechanistically motivated.

image_group{"layout":"carousel","aspect_ratio":"16:9","query":["Ebbinghaus illusion diagram","Hallucination Machine DeepDream VR video psychedelic","surround suppression contrast center surround stimulus","Klüver form constants geometric hallucinations illustration"],"num_per_query":1}

## A perturbation taxonomy that is defensible, readable, and easy to preregister

Here’s the strongest way to “beef up” the perturbation space: make it look like a **small set of operator families** that each (a) targets a known computation, (b) can be graded with 3–5 intensity levels, and (c) has at least one *positive control* and one *null/control* perturbation.

The goal is not many perturbations; the goal is **orthogonality and interpretability**.

### Context and figure-ground operators

These should instantiate “contextual modulation” in literal stimulus structure, because that’s what the human psilocybin contextual paper actually measured. citeturn32view0turn39view0  

High-value subfamilies:

- **Boundary weakening**: systematically reduce edge ownership cues by locally smoothing edges, attenuating high spatial frequencies near segmentation boundaries, or adding “border ambiguity” noise near contours.  
- **Surround competition modulation**: manipulate center–surround contrast relationships and local normalization-like statistics (e.g., amplify surround contrast while keeping center constant, or vice versa). This is the most direct bridge to surround suppression findings. citeturn32view0turn37view0  
- **Contextual size/scale illusions**: Ebbinghaus-like size-context manipulations are a clean link to the behavioral finding that psilocybin selectively changes contextual perception without altering control trials. citeturn32view0  

Design note: include at least one operator that is “context-only” (preserves central object pixels, changes only surround) to help interpret where effects localize in predicted cortex.

### Temporal persistence operators

Preclinical evidence says temporal dynamics change even when basic tuning stays intact. citeturn39view0  

High-value subfamilies:

- **Motion trails / smear**: optical-flow-weighted frame integration (past frames persist into current).  
- **Temporal low-pass / long integration**: convolve video stream with temporal kernel so events “linger” (afterimage-like).  
- **Order disruptions** as controls: frame shuffling and/or local time-jitter. This is especially strong because BOLD Moments already operationalizes frame shuffling as a temporal-order test. citeturn59view2turn59view1  

### Color and surface dynamics

Treat these as “likely informative but not your core mechanistic bet.” Make them a compact family:

- global saturation/hue drift,  
- local chromatic instability,  
- contrast/gamma perturbations.

These are easy to implement and serve as useful baselines because they should drive early visual predictions strongly; they help interpret whether your “context” operators do something *beyond* trivially exciting V1.

### Pattern recursion and hallucination-like transformations

If you include this, do it in a disciplined way: a parameterized operator with documented mapping from strength → perceptual patterning.

The Hallucination Machine is precedent for DeepDream-like transforms applied framewise to naturalistic video, explicitly pitched as parameterizable manipulation of hallucination-like phenomenology. citeturn40view0  

You can incorporate a restricted “DeepDream-style” family as:
- a *single* operator class with controlled layer/strength parameters,
- plus strong control operators that match low-level statistics (e.g., texture/noise matched) so you can argue effects are not just “more edges.”

### Audiovisual mismatch operators

BOLD Moments clips are silent in the core task design (3 s silent video + ITI), citeturn59view1 so audiovisual operators may be more relevant as a forward-looking extension than the first workshop deliverable. Still, TRIBE v2 explicitly supports multimodal inputs, citeturn60view0turn20view0 so it’s reasonable to include one small family:

- temporal asynchrony between audio and video tracks,  
- semantic mismatch (audio from another clip),  
- amplitude modulation.

If you preregister this, keep it as an “exploratory tier” so it doesn’t dominate scope.

## Analysis strategy that produces interpretable rankings instead of pretty embeddings

The analysis has to output something reviewers recognize as falsifiable: **a perturbation ranking and latent structure**, with clear primary metrics.

### What you should treat as the core “unit” of analysis

BOLD Moments is built around short, controlled events with repeated presentations and robust metadata. citeturn59view1turn61view0  

So your natural unit is:

- **clip × perturbation family × intensity × (time window / epoch)** → predicted response pattern (vertex-wise or ROI-wise).

Don’t jump straight to wholebrain UMAP plots. First produce a matrix of effect sizes and reliabilities that can be preregistered.

### Geometry-first outcome metrics

Representational Similarity Analysis (RSA) is explicitly designed to compare representational geometries (brain ↔ model ↔ behavior) via representational dissimilarity matrices (RDMs). citeturn44view4  

For your purposes, RSA is useful in three concrete ways:

1) **Within-perturbation consistency**: does a given operator produce a stable RDM change across clips?  
2) **Between-perturbation dissociation**: do two operator families induce distinguishable geometry shifts?  
3) **ROI specificity**: do those geometry shifts concentrate in early visual vs higher-order parcels?

BOLD Moments already uses RSA-style logic to compare neural RDMs to metadata-derived RDMs (including frame vs full-video captions), and it explicitly normalizes by an upper noise ceiling in some RSA pipelines. citeturn59view2  

### Variance bounds and realism checks

Any “largest effect” claim should be expressed relative to an estimate of what the data/model can support. Noise ceiling thinking is the standard way to calibrate interpretability in encoding-model evaluation: the achievable prediction accuracy is bounded by measurement noise and other unmodeled variance. citeturn58view0  

Even though your workshop phase is in silico, this logic still helps:
- it keeps you honest about what later human validation could detect,
- it gives you a principled way to decide whether a perturbation family is “big enough to be worth scanning.”

### A ranking criterion that won’t collapse into circular storytelling

A strong preregisterable perturbation ranking can be built from three axes:

- **Effect magnitude**: mean change in predicted response geometry relative to unperturbed baseline, aggregated across clips, with uncertainty intervals from clip resampling.  
- **Effect coherence**: low within-family dispersion across clips (you want operators that behave like operators, not like “sometimes it does X, sometimes Y”).  
- **Interpretability index**: degree to which effects localize to expected networks (e.g., context operators affecting early visual + mid-level areas more than language areas), and degree to which families are separable in latent space.

Then your “latent structure” claim becomes testable: if PCA/factor analysis on perturbation-induced change vectors yields a small number of stable axes that replicate across clip splits, that supports your Hypothesis 2.

### Use BOLD Moments derivatives intelligently

BOLD Moments explicitly describes versions and spaces, and the paper notes a version that estimates single-trial betas with GLMsingle. citeturn59view3turn61view0  

Even if your primary workshop deliverable is TRIBE-only, you can strengthen the story by preregistering a minimal “reality anchor” check:

- Show that TRIBE’s baseline predictions reproduce known patterns in BOLD Moments analyses (e.g., temporal-order sensitivity in early visual cortex is a plausible benchmark given the dataset’s frame-shuffling logic). citeturn59view2turn59view1  

## The big risks and the cleanest ways to strengthen the project

### Circularity is real; treat it as a feature of the workshop phase, not a bug

Your own write-up already notices the core issue: if the encoder’s training regime overlaps heavily with the dataset, you can’t sell the workshop phase as “generalizable mechanistic truth.”

The simplest honest framing is:

- The workshop project is **in-silico stimulus engineering and hypothesis generation** on a compatible substrate.
- The *scientific payoff* is the perturbation shortlist + preregistered plan for human validation.

There is also a concrete technical step you can take: TRIBE v2’s repo structure includes dataset definitions labeled “Lahner2024,” pointing directly at the BOLD Moments paper as a named study in its multi-study setup—so overlap is not a vague fear. citeturn60view0turn59view1turn61view0  

To “beef up” credibility without collecting new humans immediately, add a **generalization stress test**:
- run the same perturbation atlas on at least one *additional* naturalistic dataset later (even if it’s smaller), or
- use an aggregated preprocessing framework that explicitly aims to standardize across multiple vision fMRI datasets.

The CONFORM/MOSAIC initiative is an explicit example of this direction: MOSAIC is described as preprocessing and registering multiple event-related vision datasets (including BOLD Moments) into a shared space with curated train/test splits and GLMsingle-based single-trial betas. citeturn29view0  

You don’t need to adopt the whole CONFORM agenda—just cite the existence of cross-dataset aggregation as the correct long-term solution and commit to a small, concrete robustness check.

### Don’t let “psychedelic” become your weakest causal link

Right now, the strongest psychedelic-motivated *mechanistic anchor* is contextual computation (Ebbinghaus / surround suppression / normalization-like models), because it is explicitly tested in humans under psilocybin with psychophysics + 7T fMRI + computational modeling. citeturn32view0  

Back this up by making “context operators” your Tier-1 family and treating “DeepDream / recursion” and “color warps” as Tier-2.

If you do include hallucination-style transforms, keep one sentence in the preregistration rationale that says: this family is inspired by parameterizable hallucination simulation work in naturalistic video/VR, and cite Hallucination Machine. citeturn40view0  

### Add one high-leverage “metamer-style” control: it will sharpen interpretability fast

A single metamer-like idea can dramatically clarify interpretation:

- construct paired perturbations that are matched on low-level statistics (e.g., luminance/contrast histograms, power spectra, motion energy) but differ in a targeted structure (e.g., segmentation ambiguity).  
- see whether TRIBE predicts cortical changes that track the targeted structure, not the low-level match.

This is directly aligned with the logic of “metamers reveal what information the system discards,” citeturn47search0 and it also protects you from the modern critique that models can have idiosyncratic invariances that don’t map to humans. citeturn44view0  

### Pragmatic “beef-ups” that are cheap and will read as rigorous

- **Hard-code null perturbations** (identity transform, shuffle-within-clip that preserves per-frame statistics, etc.) as preregistered baselines; frame shuffling already has an interpretability precedent in BOLD Moments. citeturn59view2turn59view1  
- **Exploit temporal epochs**: BOLD Moments explicitly analyzes temporal delays and “first vs third epoch” dynamics; mirroring this in TRIBE-predicted deltas will make your analysis feel native to the dataset, not bolted on. citeturn59view1turn59view2  
- **Pin down preprocessing/reporting conventions** early: BOLD Moments versions and GLMsingle-derived betas are described, and their repo strongly recommends using the higher-quality version. citeturn59view3turn61view0  
- **Calibrate against known psychedelic visual computation findings**: use the directionality conflicts in surround suppression (reduced vs enhanced) as a motivation to include bidirectional context operators. citeturn32view0turn37view0turn39view0  
- **Keep the “future human validation” extremely concrete**: the perturbation shortlist is the deliverable; the validation is a small stimulus set, a limited number of perturbation families, and a narrow set of preregistered primary outcomes (e.g., contextual modulation signatures in early visual ROIs).

### Where to mention infrastructure and provenance once, cleanly

TRIBE v2 is released and documented by entity["company","Meta","meta platforms inc"] with public code and usage examples hosted on entity["company","GitHub","code hosting platform"] and model distribution/docs through entity["company","Hugging Face","ml model hub company"]. citeturn60view0turn20view0 The BOLD Moments dataset is distributed via entity["organization","OpenNeuro","open neuroimaging repository"] with companion starter code and download guidance. citeturn61view0  

## Bottom line

There is absolutely precedent for:
- short naturalistic video fMRI + temporal-order perturbation analyses, citeturn59view2turn59view1  
- treating multimodal encoding models as engines for *in silico* experiments (with explicit warnings about stimulus-distribution generalization), citeturn27view0turn52view0  
- and parameterizable hallucination-like transformations of naturalistic video as a consciousness-science tool. citeturn40view0  

What’s new—and worth doing—is combining those into a *preregistered perturbation atlas* that produces a ranked shortlist of sensory operators, explicitly motivated by the tightest mechanistic psychedelic vision findings (contextual modulation and temporal dynamics). citeturn32view0turn39view0turn39view1