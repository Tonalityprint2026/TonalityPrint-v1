# 📥 Download Dataset Files

## ⚠️ AUDIO AND ANNOTATION FILES NOT INCLUDED IN THIS REPOSITORY

This GitHub repository contains **documentation only**. The actual dataset files (audio and annotations) are hosted on Zenodo for permanent archival storage and official download tracking.

---

## 🎯 Download Complete Dataset

### Official Download Source: Zenodo
**DOI:** https://doi.org/10.5281/zenodo.17913895

**Direct Download Link:** https://zenodo.org/records/17913895/files/DATACARD.zip

---

## 📦 What You'll Get from Zenodo

### DATACARD.zip (42.9 MB) Contains:

**Audio Files:**
- 144 WAV files (48kHz, 16-bit, mono)
- ~11 minutes 5 seconds total duration
- Unprocessed, high-fidelity recordings
- Format: `TPV1_B1_UTT1_S_Att_SP-Ronda.wav`

**Annotation Files:**
- 144 JSON files (complete metadata)
- 144 CSV files (23 columns each)
- 1 combined CSV (ALL_TONALITY_DATA_COMBINED.csv)
- Total: 289 annotation files

**Documentation:**
- All files in this GitHub repository
- Plus additional technical specifications

---

## 🚀 Quick Download Steps

### Step 1: Visit Zenodo
Go to: https://doi.org/10.5281/zenodo.17913895

### Step 2: Download DATACARD.zip
Click "Download" on the DATACARD.zip file (42.9 MB)

### Step 3: Extract Files
Unzip DATACARD.zip to access:
```
DATACARD/
├── audio/                  # 144 WAV files
├── annotations/
│   ├── json/              # 144 JSON files
│   ├── csv/               # 144 CSV files
│   └── ALL_TONALITY_DATA_COMBINED.csv
└── documentation/         # Technical docs
```

### Step 4: Start Using
Load the combined CSV or individual files:
```python
import pandas as pd
df = pd.read_csv('annotations/ALL_TONALITY_DATA_COMBINED.csv')
```

---

## 📊 Why Zenodo?

**Official Download Tracking:**
- Zenodo provides official download statistics
- Geographic distribution tracking
- Citation metrics via DOI
- Permanent archival storage

**You can trust Zenodo metrics in:**
- Grant applications
- Academic impact reports
- Funding justification
- Research publications

**Current Statistics:**
Visit the Zenodo page to see real-time download counts and usage metrics.

---

## 📚 What's In This GitHub Repository

This repository contains comprehensive documentation:

**Root Documentation:**
- README.md - Dataset overview
- DATASET_CARD.md - ML dataset card
- CITATION.cff - Machine-readable citation
- LICENSE - CC BY-NC 4.0 full text
- ETHICAL_USE_AND_LIMITATIONS.md - Ethical guidelines
- CHANGELOG.md - Version history
- QUICK_START.txt - Quick start guide
- REPOSITORY_GUIDE.md - Deployment guide

**Technical Documentation (documentation/ folder):**
- CODEBOOK.md - Variable definitions
- METHODOLOGY.md - Data collection procedures
- MANIFEST.txt - File inventory
- annotations.txt - Annotation guidelines
- continuous_indices.txt - Rating scales
- scripts.txt - Utterance scripts
- speaker_profile.txt - Speaker information
- tech_specs.txt - Technical specifications
- transcripts.txt - Transcriptions

---

## 🔗 Links

**Dataset Download (Zenodo):** https://doi.org/10.5281/zenodo.17913895  
**Documentation (GitHub):** https://github.com/YOUR_USERNAME/TonalityPrint-v1  
**White Paper:** https://doi.org/10.5281/zenodo.17410581  
**Website:** https://TonalityPrint.com  
**Contact:** ronda@TonalityPrint.com

---

## ⚖️ License

**CC BY-NC 4.0** (Creative Commons Attribution-NonCommercial 4.0 International)

- ✅ Academic and research use: FREE
- ✅ Proper attribution required
- ❌ Commercial use: Requires licensing

**Commercial licensing:** Contact ronda@TonalityPrint.com

---

## 📖 Citation

When using this dataset, please cite:

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

---

**Need Help?**
- 📧 Email: ronda@TonalityPrint.com
- 🌐 Website: https://TonalityPrint.com
- 📚 Full Documentation: See files in this repository

---

**Version:** 1.0.0  
**Last Updated:** January 30, 2026  
**License:** CC BY-NC 4.0
