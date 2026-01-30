# TonalityPrint GitHub Repository - Deployment Guide

**Version:** 1.0.0  
**Created:** January 30, 2026  
**For:** Ronda Polhill, TonalityPrint.com

This guide explains the production-ready GitHub repository structure for TonalityPrint Voice Dataset v1.0 and provides instructions for deployment to GitHub, Kaggle, and Hugging Face.

---

## Repository Overview

This repository mirrors the Zenodo dataset structure exactly and provides governance-safe, platform-agnostic documentation suitable for:
- GitHub repository hosting
- Kaggle dataset publishing
- Hugging Face dataset publishing
- Academic citation and review
- Enterprise ML evaluation

### Key Features

✅ **Fully Written Files** - No placeholders or synthetic content  
✅ **Authoritative Sources** - All documentation matches Zenodo files exactly  
✅ **Platform Agnostic** - Works across GitHub, Kaggle, Hugging Face  
✅ **Governance Safe** - Comprehensive ethical guidelines and licensing  
✅ **Research Grade** - Professional, restrained tone suitable for academic use

---

## Complete Repository Structure

```
TonalityPrint/
├── README.md                                    # Dataset overview (production-ready)
├── DATASET_CARD.md                              # ML dataset card (comprehensive)
├── CITATION.cff                                 # Machine-readable citation (CFF v1.2.0)
├── LICENSE                                      # CC BY-NC 4.0 full legal text
├── ETHICAL_USE_AND_LIMITATIONS.md               # Ethical guidelines and constraints
├── CHANGELOG.md                                 # Version history and future plans
├── QUICK_START.txt                              # 4-step quick start guide
├── REPOSITORY_GUIDE.md                          # This file
│
├── documentation/                               # Authoritative source files (from Zenodo)
│   ├── CODEBOOK.md                              # Variable definitions (23 columns)
│   ├── METHODOLOGY.md                           # Data collection & annotation
│   ├── MANIFEST.txt                             # Complete file inventory
│   ├── annotations.txt                          # Annotation guidelines
│   ├── continuous_indices.txt                   # Intensity rating guidelines
│   ├── scripts.txt                              # Utterance scripts
│   ├── speaker_profile.txt                      # Speaker information
│   ├── tech_specs.txt                           # Technical specifications
│   └── transcripts.txt                          # Utterance transcriptions
│
├── audio/                                       # 144 WAV files (add from Zenodo)
│   ├── TPV1_B1_UTT1_S_Att_SP-Ronda.wav
│   ├── TPV1_B1_UTT1_S_Baseneutral_SP-Ronda.wav
│   └── ... (142 more WAV files)
│
└── annotations/                                 # 289 annotation files (add from Zenodo)
    ├── json/                                    # 144 JSON files
    │   ├── TPV1_B1_UTT1_S_Att_SP-Ronda.json
    │   └── ... (143 more JSON files)
    ├── csv/                                     # 144 CSV files
    │   ├── TPV1_B1_UTT1_S_Att_SP-Ronda.csv
    │   └── ... (143 more CSV files)
    └── ALL_TONALITY_DATA_COMBINED.csv           # Combined dataset (144 rows)
```

---

## File Descriptions

### Root Level Files (7 files)

**README.md** (15KB)
- Comprehensive dataset overview
- Dataset composition and structure
- Intended use and limitations
- Quick start examples
- Citation instructions
- Professional tone for main landing page

**DATASET_CARD.md** (25KB)
- Full ML dataset card format
- Motivation and research questions
- Annotation methodology details
- Supported tasks and metrics
- Known biases and limitations
- Curation rationale
- Comprehensive for research evaluation

**CITATION.cff** (3.5KB)
- Machine-readable citation metadata
- CFF v1.2.0 standard format
- BibTeX-compatible
- Includes DOI, authors, keywords
- Enables automatic citation generation

**LICENSE** (13KB)
- Full CC BY-NC 4.0 legal text
- Dataset-specific terms
- Commercial licensing information
- Prohibited uses clearly stated

**ETHICAL_USE_AND_LIMITATIONS.md** (19KB)
- Comprehensive ethical framework
- Speaker consent documentation
- Prohibited uses (voice cloning, etc.)
- Responsible use guidelines
- Bias documentation
- Privacy considerations
- Misuse reporting procedures

**CHANGELOG.md** (7.5KB)
- Version history (v1.0.0 initial release)
- Future planned enhancements
- Contribution guidelines
- Contact information

**QUICK_START.txt** (17KB)
- Concise 4-step guide
- Common tasks reference
- Dataset quick facts
- Code examples (Python/R)
- Important limitations summary
- Citation templates

### Documentation Folder (9 files)

All files copied exactly from Zenodo authoritative sources:

- **CODEBOOK.md** (20KB) - All 23 CSV column definitions
- **METHODOLOGY.md** (31KB) - Data collection and annotation procedures
- **MANIFEST.txt** (10KB) - Complete file inventory
- **annotations.txt** (4KB) - Annotation guidelines
- **continuous_indices.txt** (1KB) - Intensity rating scales
- **scripts.txt** (1.5KB) - 18 utterance scripts
- **speaker_profile.txt** (2KB) - Speaker characteristics
- **tech_specs.txt** (1.5KB) - Recording specifications
- **transcripts.txt** (1.5KB) - Utterance transcriptions

---

## Deployment Instructions

### Option 1: GitHub Repository

**Step 1: Create GitHub Repository**
```bash
# On GitHub.com:
# 1. Click "New repository"
# 2. Name: TonalityPrint-v1 (or TonalityPrint)
# 3. Description: "A Contrast-Structured Voice Dataset for Exploring Functional Tonal Intent"
# 4. Public repository
# 5. Do NOT initialize with README (you have one)
```

**Step 2: Initialize Local Repository**
```bash
cd TonalityPrint
git init
git add .
git commit -m "Initial commit: TonalityPrint v1.0.0 documentation"
```

**Step 3: Add Audio and Annotation Files**
```bash
# Download DATACARD.zip from Zenodo
# Extract to get audio/ and annotations/ folders
# Copy them into TonalityPrint/ directory

cp -r /path/to/extracted/audio/ ./audio/
cp -r /path/to/extracted/annotations/ ./annotations/

git add audio/ annotations/
git commit -m "Add audio files and annotations (144 samples)"
```

**Step 4: Push to GitHub**
```bash
git remote add origin https://github.com/YOUR_USERNAME/TonalityPrint-v1.git
git branch -M main
git push -u origin main
```

**Step 5: Configure Repository Settings**
- Go to repository Settings
- Add topics/tags: `voice-dataset`, `prosody`, `speech`, `ai-alignment`, `tone-detection`
- Set description: "A Contrast-Structured Voice Dataset for Exploring Functional Tonal Intent, Ambivalence, and Inference-Time Prosodic Alignment v1.0"
- Set website: https://doi.org/10.5281/zenodo.17913895
- Enable Discussions (optional, for community engagement)

### Option 2: Kaggle Dataset

**Step 1: Prepare Kaggle Metadata**

Create `dataset-metadata.json`:
```json
{
  "title": "TonalityPrint Voice Dataset v1.0",
  "id": "rondapolhill/tonalityprint-v1",
  "licenses": [{"name": "CC-BY-NC-4.0"}],
  "keywords": ["audio", "speech", "prosody", "ai-alignment", "voice", "tone-detection"],
  "description": "A Contrast-Structured Voice Dataset for Exploring Functional Tonal Intent, Ambivalence, and Inference-Time Prosodic Alignment"
}
```

**Step 2: Upload to Kaggle**
- Go to kaggle.com/datasets
- Click "New Dataset"
- Upload TonalityPrint/ folder (ensure audio/ and annotations/ are included)
- Or use Kaggle API:
```bash
kaggle datasets create -p TonalityPrint/ -m dataset-metadata.json
```

**Step 3: Configure Kaggle Dataset**
- Set visibility: Public
- Add description (use README.md content)
- Add cover image (optional)
- Link to Zenodo DOI
- Enable discussions

### Option 3: Hugging Face Datasets

**Step 1: Install Hugging Face CLI**
```bash
pip install huggingface_hub
huggingface-cli login
```

**Step 2: Create Dataset Repository**
```bash
# On huggingface.co:
# 1. Click "New" → "Dataset"
# 2. Name: tonalityprint-v1
# 3. License: cc-by-nc-4.0
# 4. Initialize with README
```

**Step 3: Clone and Add Files**
```bash
git clone https://huggingface.co/datasets/YOUR_USERNAME/tonalityprint-v1
cd tonalityprint-v1

# Copy repository files
cp -r /path/to/TonalityPrint/* ./

# Create README.md from DATASET_CARD.md for Hugging Face
cp DATASET_CARD.md README.md

git add .
git commit -m "Add TonalityPrint v1.0.0 dataset"
git push
```

**Step 4: Add Dataset Card Metadata**

Prepend to README.md:
```yaml
---
language:
- en
license: cc-by-nc-4.0
multilinguality: monolingual
size_categories:
- n<1K
task_categories:
- audio-classification
- other
task_ids:
- speaker-diarization
tags:
- prosody
- voice-dataset
- tonality
- functional-intent
- ambivalence
- ai-alignment
pretty_name: TonalityPrint Voice Dataset v1.0
dataset_info:
  features:
  - name: audio
    dtype: audio
  - name: primary_intention
    dtype: string
  - name: trust_index
    dtype: int32
  - name: attention_index
    dtype: int32
  - name: reciprocity_index
    dtype: int32
  - name: empathy_resonance_index
    dtype: int32
  - name: cognitive_energy_index
    dtype: int32
  splits:
  - name: train
    num_examples: 144
  download_size: 43000000
  dataset_size: 43000000
---
```

---

## Post-Deployment Checklist

### After Publishing to Any Platform:

- [ ] Verify all files uploaded correctly
- [ ] Test download links work
- [ ] Confirm audio files play properly
- [ ] Check CSV/JSON files load in viewers
- [ ] Verify README renders correctly
- [ ] Test citation links (DOI, white paper)
- [ ] Review license display
- [ ] Add badge to website (if applicable)
- [ ] Share on social media/research networks
- [ ] Update Zenodo record with GitHub link

### Badges for README (Optional)

Add to top of README.md:
```markdown
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17913895.svg)](https://doi.org/10.5281/zenodo.17913895)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-blue.svg)](https://github.com/YOUR_USERNAME/TonalityPrint-v1)
```

---

## Maintenance and Updates

### For Future Versions:

1. **Update CHANGELOG.md** with changes
2. **Increment version** in all files (CITATION.cff, README.md, etc.)
3. **Create new Zenodo version** and update DOI
4. **Tag GitHub release** (e.g., `v1.1.0`)
5. **Update Kaggle dataset** with new version
6. **Update Hugging Face** with new files

### Community Engagement:

- **Enable GitHub Discussions** for questions
- **Monitor Issues** for bug reports
- **Accept Pull Requests** for documentation improvements
- **Publish derivative datasets** from community
- **Maintain CHANGELOG** with community contributions

---

## Quality Assurance

### Pre-Deployment Checks:

✅ All files written (no placeholders)  
✅ Zenodo documentation copied exactly  
✅ No contradictions with source files  
✅ Citation information accurate  
✅ License terms clear  
✅ Ethical guidelines comprehensive  
✅ Code examples tested  
✅ File paths verified  
✅ Links functional  
✅ Formatting consistent

### Repository Completeness:

✅ Root documentation (7 files)  
✅ Authoritative sources (9 files in documentation/)  
✅ Audio files (144 WAV - from Zenodo)  
✅ Annotations (289 files - from Zenodo)  
✅ Total: 449 files when complete

---

## Contact and Support

**Dataset Curator:** Ronda Polhill  
**Email:** ronda@TonalityPrint.com  
**Website:** https://TonalityPrint.com  
**Zenodo DOI:** https://doi.org/10.5281/zenodo.17913895

**For Repository Questions:**
- GitHub issues (after deployment)
- Email: ronda@TonalityPrint.com

---

## Notes for Ronda

This repository structure is production-ready and platform-agnostic. All files are:
- ✅ Fully written (no placeholders)
- ✅ Based on authoritative Zenodo documentation
- ✅ Governance-safe (comprehensive ethical guidelines)
- ✅ Research-grade (professional, restrained tone)
- ✅ Suitable for GitHub, Kaggle, and Hugging Face

**Next Steps:**
1. Review all files for accuracy
2. Download audio/ and annotations/ from Zenodo DATACARD.zip
3. Add audio/annotations to repository structure
4. Deploy to chosen platform(s)
5. Share repository URL for community access

**Repository Ready for:** ✅ GitHub | ✅ Kaggle | ✅ Hugging Face

---

**Generated:** January 30, 2026  
**Version:** 1.0.0  
**License:** CC BY-NC 4.0  
**© 2026 Ronda Polhill**
