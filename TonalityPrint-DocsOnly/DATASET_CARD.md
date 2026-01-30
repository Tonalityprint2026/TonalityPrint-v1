# TonalityPrint Voice Dataset v1.0 - Dataset Card

## Dataset Summary

**Name:** TonalityPrint Voice Dataset v1.0  
**DOI:** https://doi.org/10.5281/zenodo.17913895  
**Version:** 1.0.0  
**Release Date:** January 24, 2026  
**License:** CC BY-NC 4.0 (Academic/Research Free; Commercial Licensing Available)

TonalityPrint is a specialized single-speaker prosody dataset designed for precision-tuning functional tonal intents that govern complex human conversation in voice AI systems. The corpus provides 144 human-verified audio samples across 18 utterances, each recorded in 8 parallel prosodic states.

**Core Innovation:**

1. **Ambivalence Annotation:** Unlike traditional emotion datasets that treat mixed or transitional signals as noise, TonalityPrint systematically annotates ambivalence as a perceptual entropy cross-intent feature, providing an operational reference signal for AI systems navigating real-world tonal complexity.

2. **Differential Latent Analysis (DLA):** Maintaining speaker identity and lexical content constant across parallel prosodic states (the "Fixed-Phrase Octet"), TonalityPrint enables researchers to perform contrastive approximation of tonal intent vectors—analogous to established activation-steering methods in LLMs but applied to voice prosody.

---

## Motivation

### Purpose

TonalityPrint addresses a critical gap in voice AI training data by moving beyond discrete emotion recognition to capture **functional tonal intent**—what speakers *do* with tone, not just what they *feel*.

**Research Questions:**
- Can prosodic patterns function as steerable intent vectors during inference?
- How can AI systems detect and navigate tonal ambivalence?
- What acoustic features correlate with functional tonal intents?
- Can "AI-adjacent" vocal qualities co-occur with trust-building?

### Theoretical Foundation

TonalityPrint operationalizes the **Tonality as Attention** framework (Polhill, 2025), which proposes that human vocal prosody serves as an active attention mechanism functionally analogous to computational attention mechanisms in AI architectures—a shared signaling system that may bridge human-machine communication.

**Key Hypothesis:** Prosodic patterns function as steerable intent vectors during inference, enabling fine-grained control over conversational AI tone.

### Empirical Context

Annotations are grounded in ecological feasibility derived from 8,873+ consequential customer interactions (observational context, not causal proof), where observed tonal patterns correlated with:
- ~35.85% average conversion rate (correlation, not causation)
- 68 spontaneous listener reports (~0.76% of interactions) describing speaker's voice as "AI-adjacent" while maintaining high trust

**Critical Caveat:** These observations are confounded by numerous variables and cannot establish causation. They motivated the hypothesis that certain prosodic patterns merit systematic investigation, particularly the counterintuitive finding that "AI-adjacent" vocal qualities may co-occur with trust-building rather than triggering uncanny valley effects.

---

## Dataset Composition

### What Data is in the Dataset?

**Total Files:** 446 files
- **144 audio files** (WAV format, 48kHz, 16-bit, mono)
- **144 JSON annotations** (individual files with full metadata)
- **144 CSV annotations** (tabular format, 23 columns)
- **1 combined CSV** (ALL_TONALITY_DATA_COMBINED.csv)
- **13 documentation files**

**Total Duration:** ~11 minutes 5 seconds  
**Duration Range:** 3-6 seconds per utterance  
**Recording Period:** December 2025 - January 2026

### Fixed-Phrase Octet Structure

**Design:** 18 utterances × 8 parallel prosodic states = 144 samples

Each utterance recorded in:
1. **Baseline/Neutral** - Control sample, default prosody
2. **Trust (Trus)** - Conveying reliability and credibility
3. **Attention (Att)** - Directing focus and engagement
4. **Reciprocity (Reci)** - Expressing mutual exchange
5. **Empathy Resonance (Emre)** - Demonstrating empathetic connection
6. **Cognitive Energy (Cogen)** - Showing mental engagement
7. **Sub-modified variants** - 24 optional sub-modifiers (e.g., calm, analytical)
8. **Ambivalence variants** - Cross-intent complexity marker (`ambivalex`)

**Example Utterances:**
- "I want to make sure I understand what you need"
- "Just let me know where you'd like to start, and we'll go from there"
- "Would you like me to explain how this works?"
- "I will help you, but this feels risky" (ambivalence-designed)

### What Data is Represented?

**Speaker Demographics:**
- **Single speaker:** Ronda Polhill (annotator and dataset creator)
- **Age:** Mid-life
- **Gender:** Female
- **Language:** Native English speaker
- **Accent:** Neutral/mobile American (Northeastern US baseline, influenced by residency in Okinawa, Las Vegas, Seattle, Phoenix)
- **Vocal Characteristics:** Balanced dynamic attention range, tonal precision with human warmth

**Professional Context:** Customer-facing dialogue work in high-volume, high-stakes service environment (8,873+ interactions during dataset development period)

**Distinctive Quality:** Speaker's voice represents a rare profile bridging computational precision and human relational warmth, potentially making it valuable for human-AI voice alignment research investigating "AI-adjacent yet trusted" anomaly.

### Data Splits

**No official train/validation/test splits provided.**

This is a single-speaker controlled corpus designed for:
- Architectural development
- Feature extraction research
- Transfer learning evaluation
- Hypothesis generation

Researchers should create splits appropriate for their specific use case while accounting for:
- Utterance-level dependencies (same text across intents)
- Batch effects (temporal recording structure)
- Speaker-specific characteristics

**Recommended Approach:**
- Leave-one-utterance-out cross-validation
- Stratified sampling by Primary_Intention
- Temporal holdout (later batches as test set)

---

## Annotation Process

### Who Annotated the Data?

**Annotator:** Ronda Polhill (speaker and dataset creator)  
**Role:** Expert practitioner, architect of "Tonality as Attention" framework  
**Annotation Method:** Expert perceptual assessment combined with acoustic analysis

**Practitioner Background:**
- **Experience Base:** 8,873+ high-stakes customer interactions (July 2024 - March 2025)
- **Performance Context:** ~35.85% average conversion rate during observation period (observational metric, not causal proof)
- **Tonality Expertise:** Documented ability to modulate tonality adaptively in consequential interactions
- **Framework Application:** Practical experience developing/implementing "Tonality as Attention" principles in real-time

**Ecological Provenance:** Annotations reflect tonality patterns motivated by real-world deployment rather than theoretical constructs. The practitioner's annotation decisions are informed by observed correlations between specific tonal patterns and interaction outcomes across thousands of high-stakes conversations.

**Practitioner Note:** A subset of interactions (*n*=68) involved spontaneous listener feedback describing the voice as "AI-adjacent" or "robotic" while maintaining high trust. This counter-intuitive finding—that "robotic" precision can co-occur with trust—motivated the rigorous isolation of TonalityPrint's functional Primary Tonal Intent states.

### Annotation Guidelines

**Functional Tonal Intents (5 Primary):**

| Intent | Code | Definition | What It Does |
|--------|------|------------|--------------|
| **Trust** | Trus | Conveying reliability, credibility, safety | Establishes foundation for interaction |
| **Attention** | Att | Directing focus, maintaining engagement | Commands perceptual priority |
| **Reciprocity** | Reci | Expressing mutual exchange, inviting response | Balances conversational dynamics |
| **Empathy Resonance** | Emre | Demonstrating empathetic connection | Attunes to listener emotional state |
| **Cognitive Energy** | Cogen | Showing mental activation, engagement | Signals processing intensity |

**Sub-Modifiers (24 Optional):**
- Trust: Authoritative, Calm, Confident, Formal/Respectful, Reassuring
- Attention: Certainty, Clarity, Curious, Focused, Urgent/Pressure
- Reciprocity: Affirming, Collaborative, Engaged, Open, Reflective
- Empathy Resonance: Casual, Compassion, Corrective (softened), Sympathetic, Warm
- Cognitive Energy: Analytical, Dynamic, Enthusiastic, Skeptical

**Ambivalence (Cross-Intent Modifier):**
- **Code:** `ambivalex`
- **Definition:** Two or more contradictory/competing sub-modifier layers present simultaneously
- **Purpose:** Treat tonal complexity as perceptual entropy feature rather than annotation noise

### Continuous Intensity Indices (0-100 Scale)

Each utterance scored on five dimensions:

| Index | Range | Interpretation |
|-------|-------|----------------|
| **Trust (TR)** | 0-100 | 0-30: Low/Minimal, 31-60: Moderate, 61-85: High, 86-100: Very High |
| **Attention (AT)** | 0-100 | Perceptual score of attentional focus |
| **Reciprocity (RE)** | 0-100 | Perceptual score of collaborative tone |
| **Empathy Resonance (ER)** | 0-100 | Perceptual score of empathetic attunement |
| **Cognitive Energy (CE)** | 0-100 | Perceptual score of mental activation |

**Important:** These are annotator perceptual scores, not empirically validated scales.

### Quality Control Process

**1. Proprietary Heuristic Audit (Primary QC)**

After initial annotation, all 144 samples underwent blind acoustic validation:
- Acoustic profiles analyzed without access to practitioner labels
- Script evaluated spectral variance (pitch contour, energy dynamics)
- Samples flagged when acoustic features diverged from stated intention labels

**Audit Results:**
- **~80+% alignment rate:** Acoustic profiles matched intended tonal intent categories
- **~18.05% re-recorded:** Samples with acoustic-intent divergence re-recorded for consistency
- **Cross-intent patterns detected:** Cognitive Energy systematically elevated across corpus

**2. Cross-Batch Consistency Checks**
- Similar intentions compared across batches for temporal stability
- Baseline/Neutral samples verified for consistent reference point
- Internal consistency of tonality indices reviewed
- Systematic patterns (e.g., CE elevation) identified and documented

**3. Technical Validation**
- Audio integrity checked for corruption or artifacts
- Metadata completeness verified (all 23 variables present and valid)
- File naming compliance: 100% systematic convention adherence
- Segment timestamps validated against audio duration
- JSON structure verified for correct format and values

---

## Personal and Sensitive Information

### Speaker Consent

- **100% of recordings are of the author** (Ronda Polhill) with explicit informed consent for research use
- No recordings of third parties
- Full consent for public dataset release under CC BY-NC 4.0

### Biometric Data

**Voice Biometrics:**
- The dataset contains voice recordings that could be used for speaker identification
- Single speaker (Ronda Polhill) with explicit consent
- No synthetic voices, clones, or generative AI audio used
- Dataset is 100% authentic human recordings

**Prohibited Uses:**
- **Researchers are strictly prohibited from** creating unauthorized voice clones or deepfakes of the speaker
- Do not use dataset to train voice synthesis models for impersonation
- Commercial voice cloning requires explicit permission beyond CC BY-NC 4.0 license

### Privacy Considerations

- No personally identifiable information beyond speaker identity
- Speaker voluntarily provided all recordings
- No sensitive content in utterances
- Professional context utterances (customer service scenarios)

---

## Considerations for Using the Data

### Known Biases and Limitations

**1. Single-Speaker Limitation**

**Bias:** All 144 files from same speaker (Ronda Polhill, mid-life female, native English)

**Impact:**
- Findings may not generalize across genders, ages, accents, cultures, languages
- Speaker-specific vocal characteristics present in all samples
- Prosodic patterns may reflect individual rather than universal patterns

**Mitigation:**
- Clearly state single-speaker limitation in research
- Do not make population-level claims without multi-speaker validation
- Use as controlled substrate, not representative sample
- Combine with multi-speaker datasets for broader applicability

**2. Cognitive Energy Systematic Bias**

**Bias:** Cognitive Energy Index shows systematic elevation across corpus

**Possible Causes:**
- Speaker's natural ecological style (high-energy delivery)
- Lexical content effects (professional service language)
- Practitioner annotation bias (perceptual calibration)

**Impact:**
- May affect Trust and Empathy Resonance indices
- Suggests need for speaker-specific normalization in some applications
- Does not invalidate other tonality measures

**Mitigation:**
- Documented in Notes field for affected utterances
- Intentionally retained for transparency
- Researchers should account for this bias in analyses
- Consider relative comparisons within-speaker rather than absolute thresholds

**3. Controlled Environment Bias**

**Bias:** Professional studio recordings under controlled conditions

**Impact:**
- May not reflect naturalistic speech conditions
- Scripted content (not spontaneous speech)
- Single recording environment (home studio)
- Minimal acoustic variation across samples

**Mitigation:**
- Acknowledge controlled nature in publications
- Do not generalize to noisy, real-world conditions
- Useful for architectural development, less so for robustness testing
- Combine with naturalistic datasets for production deployment

**4. Annotation Subjectivity**

**Bias:** Single expert annotator (speaker = annotator)

**Impact:**
- No inter-rater reliability measures
- Perceptual scores, not objective measurements
- Potential annotator drift over recording period
- Ambivalence definitions may be subjective

**Mitigation:**
- Transparency about annotation methodology
- Quality control with proprietary heuristic audit (~80+% alignment)
- 18.05% re-recording rate for consistency
- Use as hypothesis-generating, not hypothesis-confirming

**5. Observational Context Limitations**

**Bias:** Empirical grounding references 8,873+ interactions with observational metrics

**Impact:**
- Correlation ≠ causation (multiple confounding variables)
- ~35.85% conversion rate reflects numerous factors beyond tonality
- 68 "AI-adjacent" listener reports are anecdotal, not controlled
- Professional context may not generalize to other domains

**Mitigation:**
- Explicitly state observational nature in README
- Do not claim causal relationships
- Present as hypothesis-generating context only
- Independent validation required

### Recommended Uses

**Appropriate Applications:**
- Inference-time prosodic alignment research
- Differential Latent Analysis (DLA) for tonal intent extraction
- Ambivalence-aware dialogue system development
- Style-conditioned speech synthesis experiments
- Human-AI voice calibration studies
- Transfer learning for expressive speech
- Architectural development for voice AI
- Feature extraction research
- Controlled validation studies

**Non-Recommended Applications:**
- Population-level emotion recognition (single speaker)
- Production deployment without multi-speaker validation
- Real-world robustness testing (controlled environment)
- Cross-cultural generalization (single speaker, single language)
- Benchmarking general-purpose models (specialized corpus)

---

## Supported Tasks

### 1. Inference-Time Prosodic Alignment

**Task:** Fine-tune voice models to align prosodic features with functional intent

**Metrics:**
- Intent classification accuracy (5-class)
- Continuous index prediction (MSE, MAE)
- Ambivalence detection (binary classification)
- Prosodic similarity (MFCC distance, pitch contour correlation)

**Baseline Approaches:**
- Speech emotion recognition models (adapted for functional intent)
- Prosody prediction from text
- Style transfer models

### 2. Differential Latent Analysis (DLA)

**Task:** Extract tonal intent vectors by contrasting identical utterances across prosodic states

**Approach:**
- Encode audio with self-supervised models (e.g., Wav2Vec 2.0, HuBERT)
- Compute embedding differences: Vector(Trust) - Vector(Neutral)
- Analyze latent space geometry of intent vectors

**Research Questions:**
- Are intent vectors linearly separable?
- Can vectors be composed (Trust + Calm)?
- Do vectors generalize across utterances?

### 3. Ambivalence Detection

**Task:** Classify samples as containing ambivalence (`ambivalex`) or single intent

**Dataset Split:**
- Positive class: Samples with `Ambivalex == 'ambivalex'`
- Negative class: Samples with `Ambivalex == ''`

**Metrics:**
- Precision, Recall, F1 for `ambivalex` class
- ROC-AUC for ambivalence probability

**Challenges:**
- Class imbalance (ambivalence is minority class)
- Ambivalence is continuous, not discrete
- Requires modeling tonal complexity, not just variance

### 4. Style-Conditioned Synthesis

**Task:** Generate speech with target prosodic style from text + style label

**Input:** Text + Primary_Intention + Optional Sub_Modifier  
**Output:** Audio with target tonality

**Evaluation:**
- Prosodic similarity to reference samples
- Intent classification accuracy on synthesized audio
- Human evaluation of naturalness and intent perception

### 5. Continuous Tonality Regression

**Task:** Predict five tonality indices (0-100) from audio

**Targets:** Trust, Attention, Reciprocity, Empathy Resonance, Cognitive Energy  
**Metrics:** MSE, MAE, Pearson correlation per index

**Considerations:**
- Cognitive Energy bias (systematically elevated)
- Speaker-specific calibration needed
- Perceptual scores, not ground truth

---

## Curation Rationale

### Why This Structure?

**Fixed-Phrase Octet Design:**
- **Holds lexical content constant** across prosodic variations
- **Eliminates semantic confounds** when analyzing prosody
- **Enables contrastive learning** (same text, different intent)
- **Supports Differential Latent Analysis** (isolate prosodic features)

**Single-Speaker Design:**
- **Removes speaker variability** (controlled comparison)
- **Isolates prosodic differences** from voice quality
- **Enables precise intent extraction** without identity confounds
- **Mirrors activation steering in LLMs** (single model, varying prompts)

**Ambivalence as Feature:**
- **Reflects real-world complexity** (mixed signals are common)
- **Challenges AI safety** (detecting uncertainty is critical)
- **Complements pure intent samples** (full spectrum of tonality)
- **Enables nuanced modeling** (not just categorical classification)

### Why These Utterances?

**Selection Criteria:**
- Professional service language (customer-facing scenarios)
- Neutral semantic content (avoids strong affective words)
- Varied syntactic structures (statements and questions)
- Utterances 16-18 designed explicitly for ambivalence

**Example Design:**
- "I will help you, but this feels risky" (Trust + Ambivalence)
- "Sure, I'm in… unless it all goes wrong" (Reciprocity + Doubt)
- "I'm excited, but this also may fail" (Cognitive Energy + Uncertainty)

### Why 8 Parallel States?

**Coverage:** 6 primary states (1 baseline + 5 intents) + 1-2 modified/ambivalent variants

**Rationale:**
- Sufficient variation for contrastive analysis
- Manageable annotation burden (144 total samples)
- Balances coverage and depth
- Enables within-utterance comparisons

---

## Data Collection Process

### Recording Environment

**Location:** Controlled home studio  
**Acoustic Treatment:** Minimal ambient noise, consistent conditions  
**Speaker Position:** Seated, consistent positioning throughout

**Recording Equipment:**
- **Microphone:** Blue Yeti USB microphone (cardioid mode, ~6-8" distance)
- **Software:** Audacity (48kHz, 32-bit float, real-time effects disabled)
- **Environment:** Consistent preset settings, minimal background noise

### Recording Protocol

1. **Pre-Recording Setup:** Speaker reviews utterance text and mentally prepares tonality intention
2. **Recording Capture:** Speaker delivers utterance with intended tonality at 48kHz, 32-bit float
3. **Immediate Quality Check:** Playback review for technical issues (clipping, noise, artifacts)
4. **Export & Naming:** Export as 16-bit PCM WAV (48kHz, mono) with systematic file naming

### Post-Processing Policy

**Processing:** **None.** No EQ, compression, normalization, or noise reduction applied.

**Rationale:** To preserve 100% human tonality variance and support maximum fidelity for micro-tonal expression analysis, this dataset provides raw, unprocessed audio files.

**Note:** Minimal background noise may be present in some recordings. This was intentional to avoid altering nuanced vocal tonality through post-processing artifacts.

### Timeline

- **First recordings:** December 2025
- **Final recordings:** January 2026
- **Total collection period:** ~1 month
- **Recording batches:** 6 (B1-B6)
- **Quality audit & re-recording:** ~18.05% of corpus

---

## Dataset Statistics

### Composition

| Statistic | Value |
|-----------|-------|
| **Total Utterances** | 144 |
| **Unique Texts** | 18 |
| **Prosodic States per Text** | 8 |
| **Total Batches** | 6 |
| **Utterances per Batch** | 18 |
| **Speakers** | 1 (Ronda Polhill) |
| **Language** | English (American) |
| **Total Duration** | ~11 minutes 5 seconds |
| **Duration Range** | 3-6 seconds per file |

### Primary Intention Distribution

| Intention | Count (Expected) | Percentage |
|-----------|------------------|------------|
| **Attention** | 24 | 16.7% |
| **Trust** | 24 | 16.7% |
| **Reciprocity** | 24 | 16.7% |
| **Empathy Resonance** | 24 | 16.7% |
| **Cognitive Energy** | 24 | 16.7% |
| **Baseline/Neutral** | 18 | 12.5% |
| **Modified/Ambivalent** | 6 | 4.2% |

*Note: Exact counts may vary based on sub-modifier and ambivalence annotations*

### Utterance Type Distribution

| Type | Description | Distribution |
|------|-------------|--------------|
| **Statement (S)** | Declarative sentences | ~83% |
| **Question (Q)** | Interrogative sentences | ~17% |

---

## Maintenance and Updates

### Version History

**v1.0.0 (January 24, 2026)** - Initial public release
- 144 audio files (WAV format)
- 144 JSON annotations
- 144 CSV annotations + 1 combined CSV
- 13 documentation files
- Complete quality control audit (~18.05% re-recorded)

### Future Plans

**Potential Extensions:**
- Multi-speaker validation with diverse demographics
- Naturalistic speech conditions (spontaneous dialogue)
- Cross-cultural adaptation (multiple languages, accents)
- Expanded utterance set (more semantic domains)
- Independent annotation validation (inter-rater reliability)
- Longitudinal speaker analysis (temporal stability)

**Community Contributions:**
- Collaborative validation studies welcomed
- Multi-speaker extensions actively sought
- Derivative datasets encouraged (with proper attribution)

### Reporting Issues

**For:**
- Technical errors in files
- Annotation discrepancies
- Documentation clarifications
- Usage questions

**Contact:** ronda@TonalityPrint.com

---

## License and Attribution

### License

**CC BY-NC 4.0** (Creative Commons Attribution-NonCommercial 4.0 International)

**You are free to:**
- **Share:** Copy and redistribute the material in any medium or format
- **Adapt:** Remix, transform, and build upon the material

**Under the following terms:**
- **Attribution:** Must give appropriate credit, provide link to license, indicate if changes were made
- **NonCommercial:** May not use material for commercial purposes
- **No additional restrictions:** May not apply legal terms or technological measures that legally restrict others

**Commercial Licensing:** Contact ronda@TonalityPrint.com for commercial use permissions.

### Citation

**Required Citation:**

```bibtex
@dataset{polhill_2026_tonalityprint,
  author       = {Polhill, Ronda},
  title        = {TonalityPrint: A Contrast-Structured Voice Dataset 
                  for Exploring Functional Tonal Intent, Ambivalence, 
                  and Inference-Time Prosodic Alignment v1.0},
  year         = 2026,
  publisher    = {Zenodo},
  version      = {1.0.0},
  doi          = {10.5281/zenodo.17913895},
  url          = {https://doi.org/10.5281/zenodo.17913895}
}
```

### Acknowledgment

Please acknowledge the dataset in publications:

> "This research uses the TonalityPrint Voice Dataset v1.0 (Polhill, 2026), available at https://doi.org/10.5281/zenodo.17913895."

---

## Contact Information

**Dataset Curator:** Ronda Polhill  
**Email:** ronda@TonalityPrint.com  
**Website:** https://TonalityPrint.com  
**DOI:** https://doi.org/10.5281/zenodo.17913895

**For Questions About:**
- Dataset usage → README.md or QUICK_START.txt
- Variable definitions → CODEBOOK.md
- Methodology → METHODOLOGY.md
- Ethical use → ETHICAL_USE_AND_LIMITATIONS.md
- Technical issues → ronda@TonalityPrint.com

---

**Version:** 1.0.0  
**Last Updated:** January 24, 2026  
**License:** CC BY-NC 4.0  
**© 2026 Ronda Polhill**
