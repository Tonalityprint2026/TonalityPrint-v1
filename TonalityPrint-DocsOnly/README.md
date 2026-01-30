# TonalityPrint Voice Dataset v1.0

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17913895.svg)](https://doi.org/10.5281/zenodo.17913895)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

**A Contrast-Structured Voice Dataset for Exploring Functional Tonal Intent, Ambivalence, and Inference-Time Prosodic Alignment**

---

## 📥 DOWNLOAD DATASET FILES

> **⚠️ This GitHub repository contains DOCUMENTATION ONLY.**
> 
> **Download audio and annotation files from Zenodo:**  
> **https://doi.org/10.5281/zenodo.17913895**
>
> See [DOWNLOAD_DATA.md](DOWNLOAD_DATA.md) for detailed instructions.

---

## Overview

TonalityPrint is a specialized single-speaker speech corpus designed to enable exploration of fine-tuning **functional tonal intents** in voice AI systems. Unlike emotion recognition datasets, TonalityPrint annotates functional tonal intents (what speakers *do* with tone), not just what they *feel*.

**Key Features:**
- **144 high-fidelity WAV files** (48kHz, 16-bit, mono, unprocessed)
- **18 unique utterances** across **8 parallel prosodic states**
- **5 functional tonal intents**: Trust, Attention, Reciprocity, Empathy Resonance, Cognitive Energy
- **Continuous intensity indices** (0-100 scale) for each intent
- **Ambivalence annotation** (perceptual entropy cross-intent feature)
- **100% authentic human voice** with explicit consent
- **Single-speaker design** eliminates speaker variability for controlled analysis

**What This Dataset Is:**
- A precision-tuning resource for prosodic AI alignment research
- A controlled substrate for investigating functional tonal intent
- An experimental framework for ambivalence-aware dialogue systems
- A hypothesis-generating tool for human-AI voice calibration

**What This Dataset Is Not:**
- A general-purpose emotion recognition training corpus
- A multi-speaker dataset for population-level generalization
- A substitute for large-scale speech datasets
- A validated benchmark for production systems

---

## Dataset Composition

### Structure

```
TonalityPrint/
├── audio/                              # 144 WAV files
├── annotations/
│   ├── json/                          # 144 JSON files
│   ├── csv/                           # 144 CSV files
│   └── ALL_TONALITY_DATA_COMBINED.csv # Combined dataset
└── documentation/                      # Technical references
```

### Audio Specifications

| Specification | Value |
|--------------|-------|
| **Format** | WAV (uncompressed PCM) |
| **Sample Rate** | 48,000 Hz (48kHz) |
| **Bit Depth** | 16-bit |
| **Channels** | Mono (1 channel) |
| **Duration per File** | 3-6 seconds |
| **Total Duration** | ~11 minutes 5 seconds |
| **Processing** | None (raw, unprocessed) |
| **Total Files** | 144 audio samples |

### Fixed-Phrase Octet Design

The dataset uses a **Fixed-Phrase Octet** structure: 18 utterances × 8 parallel prosodic states.

Each utterance is recorded in:
1. **Baseline/Neutral** (control sample)
2. **Trust** (Trus) - conveying reliability and credibility
3. **Attention** (Att) - directing focus and engagement
4. **Reciprocity** (Reci) - expressing mutual exchange
5. **Empathy Resonance** (Emre) - demonstrating empathetic connection
6. **Cognitive Energy** (Cogen) - showing mental engagement
7. **Sub-modified variants** (e.g., Trust + Calm)
8. **Ambivalence variants** (optional cross-intent complexity)

This design enables:
- **Differential Latent Analysis (DLA)**: Isolate prosodic features while holding lexical content constant
- **Contrastive learning**: Compare prosodic variations across identical text
- **Intent vector extraction**: Model functional intent as steerable features

---

## Controlled Semantic Design

### Functional Tonal Intents (Not Emotions)

TonalityPrint distinguishes between **functional intent** and **affective state**:

| Functional Intent | What It Does | Not The Same As |
|------------------|--------------|-----------------|
| **Trust** | Establishes credibility, reliability | "Happiness" or "Confidence" |
| **Attention** | Directs focus, maintains engagement | "Excitement" or "Urgency" |
| **Reciprocity** | Invites response, balances exchange | "Friendliness" or "Agreement" |
| **Empathy Resonance** | Attunes to listener state | "Sympathy" or "Sadness" |
| **Cognitive Energy** | Signals mental activation | "Enthusiasm" or "Anxiety" |

**Why This Matters:**
- Traditional emotion datasets label *what speakers feel*
- TonalityPrint annotates *what speakers do with their voice*
- This functional framing aligns with conversational AI goals

### Ambivalence as Feature (Not Noise)

Unlike traditional datasets that discard mixed signals as annotation errors, TonalityPrint systematically annotates **ambivalence** (`ambivalex`) as:
- A perceptual entropy transitional state
- A cross-intent feature where competing tonal cues co-occur
- An essential signal for real-world inference-time alignment

**Example Applications:**
- Detecting when AI should express uncertainty
- Modeling tonal complexity in high-stakes interactions
- Training systems to navigate mixed emotional states

---

## Annotation Methodology

### Expert Practitioner Annotation

**Annotator:** Ronda Polhill (speaker and dataset creator)  
**Method:** Expert perceptual assessment combined with acoustic analysis  
**Expertise:** 8,873+ high-stakes customer interactions (observational context, not causal proof)

### Continuous Indices (0-100 Scale)

Each utterance includes five tonality indices:

| Index | Abbreviation | Interpretation |
|-------|--------------|----------------|
| **Trust** | TR | 0-30: Low/Minimal, 31-60: Moderate, 61-85: High, 86-100: Very High |
| **Attention** | AT | Perceptual score of attentional focus |
| **Reciprocity** | RE | Perceptual score of collaborative tone |
| **Empathy Resonance** | ER | Perceptual score of empathetic attunement |
| **Cognitive Energy** | CE | Perceptual score of mental activation |

**Important:** These are annotator perceptual scores, not empirically validated scales.

### Quality Control

- **Proprietary heuristic audit**: ~80+% acoustic-intent alignment verified
- **Re-recording rate**: ~18.05% of corpus re-recorded for consistency
- **Known bias**: Cognitive Energy shows systematic elevation (documented and retained)

---

## Intended Use

### Primary Applications

1. **Inference-Time Prosodic Alignment**
   - Fine-tuning reasoning-based voice models
   - Aligning model confidence with vocal uncertainty
   - Calibrating trust signals in AI responses

2. **Differential Latent Analysis**
   - Extracting tonal intent vectors (analogous to LLM activation steering)
   - Contrastive learning with fixed lexical content
   - Isolating prosodic features from semantic content

3. **Ambivalence-Aware Systems**
   - Training dialogue systems to detect mixed signals
   - Modeling uncertainty in safety-critical applications
   - Navigating tonal complexity in nuanced interactions

4. **Style-Conditioned Synthesis**
   - Controlling prosodic style in TTS systems
   - Evaluating voice quality metrics
   - Transfer learning for expressive speech

5. **Human-AI Voice Calibration**
   - Investigating "AI-adjacent yet trusted" vocal profiles
   - Studying uncanny valley effects in voice
   - Exploring voice-appearance synchrony in embodied AI

### Appropriate Use Cases

- Academic research on prosody and speech synthesis
- Architectural development for voice AI systems
- Feature extraction and transfer learning experiments
- Controlled validation studies
- Exploratory analysis of functional tonal intent

### Non-Intended Uses

- **Do NOT use for:**
  - Population-level emotion recognition (single speaker only)
  - Production deployment without multi-speaker validation
  - Creating unauthorized voice clones or deepfakes of the speaker
  - Commercial applications without licensing (CC BY-NC 4.0)
  - Generalizing findings beyond this specific speaker profile

---

## Known Biases and Limitations

### Single-Speaker Constraint

- **All 144 files from same speaker** (Ronda Polhill)
- Findings may not generalize across:
  - Genders
  - Ages
  - Accents
  - Cultures
  - Languages
- Multi-speaker validation required for broader applicability

### Cognitive Energy Systematic Bias

**Known Issue:** Cognitive Energy Index shows systematic elevation across corpus.

**Possible Causes:**
- Speaker's natural ecological style (high-energy delivery)
- Lexical content effects
- Practitioner annotation bias

**Resolution:** Intentionally retained for transparency. Researchers should account for this bias in analyses.

**Impact:**
- May affect Trust and Empathy Resonance indices
- Suggests need for speaker-specific normalization
- Does not invalidate other tonality measures

### Controlled Environment

- Professional studio recordings (not naturalistic)
- Scripted content (not spontaneous speech)
- May not reflect real-world acoustic conditions
- Single recording period (Dec 2025 - Jan 2026)

### Observational Context (Not Causal Proof)

The annotation methodology references 8,873+ customer interactions with observed correlations:
- ~35.85% average conversion rate (observational metric)
- 68 spontaneous reports of "AI-adjacent" voice quality with high trust ratings

**Critical Caveat:** These are observational correlations, not causal relationships. Multiple confounding variables present. Provided as hypothesis-generating context only.

### Annotation Subjectivity

- Continuous indices are perceptual scores, not validated scales
- Single annotator (no inter-rater reliability)
- Ambivalence definitions may require field-specific interpretation

---

## Ethical Considerations

### Speaker Consent and Biometric Integrity

- **100% human recordings** by author (Ronda Polhill)
- Explicit informed consent for recording, annotation, and public release
- No synthetic voices, clones, or generative AI audio
- Speaker demographics: Mid-life female, native English speaker

### Prohibited Uses

**Researchers are strictly prohibited from:**
- Creating unauthorized voice clones of the speaker
- Generating deepfakes using this dataset
- Using recordings for deceptive purposes
- Violating CC BY-NC 4.0 license terms

### Responsible Use Guidelines

- Acknowledge single-speaker limitation in publications
- Do not make population-level claims
- Report systematic biases when using dataset
- Obtain commercial license for non-academic use
- Cite dataset properly (see [Citation](#citation))

---

## Quick Start

### 1. Download Dataset

```bash
# Download from Zenodo
wget https://zenodo.org/records/17913895/files/DATACARD.zip
unzip DATACARD.zip
```

### 2. Load Annotations (Python)

```python
import pandas as pd
import json

# Load combined CSV
df = pd.read_csv('annotations/ALL_TONALITY_DATA_COMBINED.csv')

# Parse segment-level data
df['Segments_Parsed'] = df['Segments'].apply(json.loads)

# Filter by intention
trust_samples = df[df['Primary_Intention'] == 'Trust']
ambivalent_samples = df[df['Ambivalex'] == 'ambivalex']
```

### 3. Access Audio Files

```python
import librosa

# Load audio file
audio_path = 'audio/TPV1_B1_UTT1_S_Att_SP-Ronda.wav'
audio, sr = librosa.load(audio_path, sr=48000, mono=True)

# Extract features
mfcc = librosa.feature.mfcc(y=audio, sr=sr, n_mfcc=13)
```

### 4. Explore Tonality Indices

```python
# Compare Trust scores across utterances
trust_scores = df.groupby('Utterance_Number')['Trust_Index'].mean()

# Analyze Cognitive Energy bias
ce_by_intent = df.groupby('Primary_Intention')['Cognitive_Energy_Index'].describe()
```

---

## File Structure Summary

### Documentation Files

| File | Description |
|------|-------------|
| `README.md` | This file - Dataset overview and usage |
| `DATASET_CARD.md` | Comprehensive ML dataset card |
| `CODEBOOK.md` | Variable definitions and file naming |
| `METHODOLOGY.md` | Data collection and annotation procedures |
| `CITATION.cff` | Machine-readable citation metadata |
| `LICENSE` | CC BY-NC 4.0 license text |
| `ETHICAL_USE_AND_LIMITATIONS.md` | Ethical guidelines and constraints |
| `QUICK_START.txt` | 4-step quick start guide |
| `MANIFEST.txt` | Complete file inventory |

### Annotation Files (289 total)

- **144 JSON files**: Original annotations with full metadata
- **144 CSV files**: Tabular format (23 columns)
- **1 combined CSV**: `ALL_TONALITY_DATA_COMBINED.csv` (all 144 rows)

### Audio Files (144 total)

**File Naming Convention:**
```
TPV1_[Batch]_[Utterance]_[Type]_[Intent]_[Modifier]_[Ambivalex]_SP-Ronda.wav
```

**Examples:**
- `TPV1_B1_UTT1_S_Att_SP-Ronda.wav` (Single - Attention only)
- `TPV1_B1_UTT1_S_Reci_affi_SP-Ronda.wav` (Compound - Reciprocity + Affirming)
- `TPV1_B1_UTT1_S_Reci_affi_ambivalex_SP-Ronda.wav` (Complex - with Ambivalence)

---

## Citation

### BibTeX

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

### APA

Polhill, R. (2026). *TonalityPrint: A Contrast-Structured Voice Dataset for Exploring Functional Tonal Intent, Ambivalence, and Inference-Time Prosodic Alignment v1.0* [Data set]. Zenodo. https://doi.org/10.5281/zenodo.17913895

### Related Work

**Supplement to:** Polhill, R. (2025). "Tonality as Attention" white paper. Zenodo. https://doi.org/10.5281/zenodo.17410581

---

## Contact and Licensing

**Dataset Curator:** Ronda Polhill  
**Email:** ronda@TonalityPrint.com  
**Website:** https://TonalityPrint.com

**License:** CC BY-NC 4.0 (Non-commercial use)  
**Commercial Licensing:** Contact ronda@TonalityPrint.com

**For Questions About:**
- Dataset usage → This README or QUICK_START.txt
- Variable definitions → CODEBOOK.md
- Methodology → METHODOLOGY.md
- Ethical use → ETHICAL_USE_AND_LIMITATIONS.md
- Technical issues → ronda@TonalityPrint.com

---

## Version Information

**Version:** 1.0.0  
**Release Date:** January 24, 2026  
**DOI:** https://doi.org/10.5281/zenodo.17913895  
**Last Updated:** January 24, 2026

---

## Acknowledgments

This work emerges from independent practitioner-research conducted without institutional funding and is released for academic research use under CC BY-NC 4.0.

TonalityPrint aims to address a critical gap in voice AI training data by moving beyond discrete emotion recognition to capture functional tonal intent, including ambivalent prosodic signals as essential nuances for inference-time alignment.

---

**© 2026 Ronda Polhill | Licensed under CC BY-NC 4.0**
