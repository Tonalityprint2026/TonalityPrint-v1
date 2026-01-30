# Changelog - TonalityPrint Voice Dataset

All notable changes to the TonalityPrint Voice Dataset will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] - 2026-01-24

### Initial Public Release

**Release Date:** January 24, 2026  
**DOI:** https://doi.org/10.5281/zenodo.17913895

#### Added

**Dataset Core:**
- 144 audio files (WAV format, 48kHz, 16-bit, mono, unprocessed)
- 18 unique utterances across 8 parallel prosodic states
- Fixed-Phrase Octet design for Differential Latent Analysis (DLA)
- 100% authentic human voice recordings with explicit consent

**Annotations:**
- 144 individual JSON annotation files with full metadata
- 144 individual CSV annotation files (23 columns each)
- 1 combined CSV file (ALL_TONALITY_DATA_COMBINED.csv)
- 5 functional tonal intents: Trust, Attention, Reciprocity, Empathy Resonance, Cognitive Energy
- Baseline/Neutral control samples
- 24 optional sub-modifiers for fine-grained tonality descriptors
- Systematic ambivalence annotation (perceptual entropy cross-intent feature)
- Continuous intensity indices (0-100 scale) for each tonal intent
- Segment-level temporal data with millisecond precision

**Documentation:**
- README.md (comprehensive dataset overview)
- DATASET_CARD.md (ML dataset card format)
- CODEBOOK.md (variable definitions and file naming conventions)
- METHODOLOGY.md (data collection and annotation procedures)
- CITATION.cff (machine-readable citation metadata)
- LICENSE (CC BY-NC 4.0 legal text)
- ETHICAL_USE_AND_LIMITATIONS.md (ethical guidelines and constraints)
- QUICK_START.txt (4-step quick start guide)
- MANIFEST.txt (complete file inventory)
- annotations.txt (annotation guidelines)
- continuous_indices.txt (continuous intensity rating guidelines)
- scripts.txt (utterance scripts)
- speaker_profile.txt (speaker information)
- tech_specs.txt (technical specifications)
- transcripts.txt (utterance transcriptions)

**Quality Assurance:**
- Proprietary heuristic audit: ~80+% acoustic-intent alignment verified
- Re-recording: ~18.05% of corpus re-recorded for consistency
- Cross-batch consistency checks implemented
- Technical validation (audio integrity, metadata completeness, file naming compliance)
- Known bias documentation (Cognitive Energy systematic elevation)

**Features:**
- Single-speaker design eliminates speaker variability
- Controlled semantic design (functional intent vs. emotion)
- Ambivalence treated as feature, not noise
- Ecological provenance (grounded in 8,873+ real-world interactions)
- Unprocessed audio preserves authentic human tonality
- Comprehensive metadata (23 variables per utterance)

**License:**
- CC BY-NC 4.0 (Creative Commons Attribution-NonCommercial 4.0 International)
- Academic and research use free
- Commercial licensing available upon request

**Theoretical Framework:**
- Operationalizes "Tonality as Attention" framework (Polhill, 2025)
- Supplements white paper DOI: 10.5281/zenodo.17410581

#### Known Issues

**Documented Biases:**
- **Cognitive Energy Elevation:** Systematic elevation across corpus (intentionally retained for transparency)
  - Possible causes: Speaker's ecological style, lexical content effects, practitioner annotation bias
  - Impact: May affect Trust and Empathy Resonance indices
  - Mitigation: Documented in Notes field, researchers should account for bias in analyses

**Limitations:**
- Single speaker (Ronda Polhill) - findings may not generalize across demographics
- Controlled environment (professional studio) - may not reflect naturalistic conditions
- Single annotator (no inter-rater reliability)
- Observational context (8,873+ interactions) - correlation, not causation
- Temporal snapshot (~1 month recording period)

#### Notes

**Recording Period:** December 2025 - January 2026  
**Total Duration:** ~11 minutes 5 seconds  
**Speaker:** Ronda Polhill (mid-life female, native English, neutral/mobile American accent)  
**Recording Environment:** Controlled home studio (Blue Yeti microphone, Audacity 48kHz/32-bit float)  
**Post-Processing:** None (raw, unprocessed audio)

**Empirical Context:**
- Annotations grounded in 8,873+ consequential customer interactions
- Observed correlation with ~35.85% average conversion rate (observational, not causal)
- 68 spontaneous listener reports of "AI-adjacent" voice quality with high trust ratings

**Research Applications:**
- Inference-time prosodic alignment
- Differential Latent Analysis (DLA) for tonal intent extraction
- Ambivalence-aware dialogue systems
- Style-conditioned speech synthesis
- Human-AI voice calibration
- Embodied AI and humanoid robotics

---

## [Unreleased]

### Planned Future Enhancements

#### Under Consideration

**Dataset Expansion:**
- Multi-speaker validation with diverse demographics
- Naturalistic speech conditions (spontaneous dialogue)
- Cross-cultural adaptation (multiple languages, accents)
- Expanded utterance set (more semantic domains)
- Longitudinal speaker analysis (temporal stability)

**Annotation Improvements:**
- Independent annotation validation (inter-rater reliability)
- Expanded sub-modifier taxonomy
- Fine-grained temporal segmentation (phrase-level analysis)
- Acoustic feature extraction and documentation
- Automated quality control tools

**Documentation:**
- Usage tutorials and code examples
- Benchmark evaluation protocols
- Derivative dataset guidelines
- Research findings bibliography
- Community contributions showcase

**Community Engagement:**
- Collaborative validation studies
- Multi-speaker extension partnerships
- Derivative dataset tracking
- Research workshop organization
- Open-source tooling development

#### Seeking Contributions

**We welcome:**
- Multi-speaker validation studies
- Cross-cultural replication attempts
- Independent annotation validation
- Acoustic analysis contributions
- Derivative dataset publications (with attribution)
- Bug reports and documentation improvements

**To Contribute:**
- Email: ronda@TonalityPrint.com
- Subject: "TonalityPrint Contribution"
- Provide: Description of contribution, timeline, attribution preferences

---

## Version History Summary

| Version | Release Date | DOI | Changes |
|---------|--------------|-----|---------|
| 1.0.0 | 2026-01-24 | 10.5281/zenodo.17913895 | Initial public release |

---

## Citation

When using this dataset, please cite the current version:

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

## Contact

**Dataset Curator:** Ronda Polhill  
**Email:** ronda@TonalityPrint.com  
**Website:** https://TonalityPrint.com  
**DOI:** https://doi.org/10.5281/zenodo.17913895

**For:**
- Bug reports → ronda@TonalityPrint.com
- Feature requests → ronda@TonalityPrint.com
- Collaboration inquiries → ronda@TonalityPrint.com
- Commercial licensing → ronda@TonalityPrint.com

---

**Changelog Format:** Based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)  
**Versioning:** [Semantic Versioning](https://semver.org/spec/v2.0.0.html)  
**Last Updated:** January 24, 2026  
**License:** CC BY-NC 4.0
