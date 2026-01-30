# Ethical Use and Limitations - TonalityPrint Voice Dataset v1.0

## Table of Contents

1. [Ethical Framework](#ethical-framework)
2. [Speaker Consent and Biometric Integrity](#speaker-consent-and-biometric-integrity)
3. [Prohibited Uses](#prohibited-uses)
4. [Responsible Use Guidelines](#responsible-use-guidelines)
5. [Known Limitations](#known-limitations)
6. [Bias Documentation](#bias-documentation)
7. [Privacy Considerations](#privacy-considerations)
8. [Commercial Use Policy](#commercial-use-policy)
9. [Reporting Misuse](#reporting-misuse)

---

## Ethical Framework

TonalityPrint Voice Dataset v1.0 was created with rigorous ethical standards to ensure:
- Full speaker consent and transparency
- Protection of biometric privacy
- Prevention of harmful applications
- Transparency about limitations and biases
- Responsible research practices

### Core Ethical Principles

1. **Informed Consent:** 100% of recordings are of the author (Ronda Polhill) with explicit informed consent for research use and public dataset release.

2. **Biometric Integrity:** No synthetic voices, clones, or generative AI audio were used. The dataset is 100% authentic human recordings.

3. **Transparency:** All known biases, limitations, and methodological constraints are fully documented.

4. **Research Integrity:** Observational context is clearly distinguished from causal claims.

5. **Privacy Protection:** No third-party recordings or personally identifiable information beyond speaker identity.

---

## Speaker Consent and Biometric Integrity

### Explicit Consent

**Speaker:** Ronda Polhill (dataset creator and annotator)

**Consent Scope:**
- ✓ Audio recording for research purposes
- ✓ Annotation and metadata creation
- ✓ Public dataset release under CC BY-NC 4.0
- ✓ Academic and non-commercial research use
- ✓ Derivative works with proper attribution
- ✗ Unauthorized voice cloning or deepfakes
- ✗ Commercial use without explicit licensing

### Biometric Data Handling

**Voice Biometrics:**
- The dataset contains voice recordings that could be used for speaker identification
- Single speaker (Ronda Polhill) with full awareness and explicit consent
- No recordings of third parties or individuals without consent

**Biometric Integrity Commitment:**
- **100% human recordings** - No synthetic voices, voice clones, or AI-generated audio
- **Unprocessed audio** - Raw recordings preserve authentic human tonality
- **Single source** - All recordings by dataset creator with informed consent
- **Transparent provenance** - Clear documentation of recording methods and speaker identity

---

## Prohibited Uses

### Strictly Forbidden Applications

**Researchers and users are explicitly prohibited from:**

1. **Unauthorized Voice Cloning**
   - Creating voice clones or synthetic versions of the speaker's voice
   - Training voice synthesis models to impersonate the speaker
   - Generating deepfakes or deceptive audio attributed to the speaker
   - Any biometric replication without explicit written permission

2. **Deceptive Purposes**
   - Using recordings to deceive listeners about speaker identity
   - Creating misleading content falsely attributed to the speaker
   - Impersonation or identity fraud
   - Social engineering or phishing attacks

3. **Harmful Applications**
   - Surveillance or tracking of the speaker or others
   - Biometric identification systems without consent
   - Discriminatory profiling based on voice characteristics
   - Weaponized voice technologies
   - Any use that violates speaker's privacy or dignity

4. **License Violations**
   - Commercial use without explicit licensing (CC BY-NC 4.0)
   - Failure to provide proper attribution
   - Removing or obscuring license information
   - Sublicensing without authorization

### Consequences of Misuse

**Violation of these prohibitions may result in:**
- Legal action under applicable laws
- Revocation of access to dataset
- Academic misconduct reporting
- Intellectual property infringement claims
- Privacy violation claims

---

## Responsible Use Guidelines

### Best Practices for Ethical Research

**1. Acknowledge Limitations**
- Clearly state single-speaker constraint in publications
- Do not make population-level claims without multi-speaker validation
- Report systematic biases when using dataset
- Distinguish observational context from causal claims

**2. Proper Attribution**
- Cite dataset using provided BibTeX citation
- Include DOI in references: https://doi.org/10.5281/zenodo.17913895
- Acknowledge "Tonality as Attention" framework (Polhill, 2025)
- Credit speaker consent explicitly

**3. Transparent Reporting**
- Document which subset of dataset was used
- Report any filtering or preprocessing steps
- Disclose known biases (e.g., Cognitive Energy elevation)
- Share code and methods for reproducibility

**4. Privacy Protection**
- Do not use dataset for biometric identification beyond research
- Protect speaker identity in sensitive contexts
- Do not combine with other datasets to de-anonymize (though speaker is known)
- Respect speaker's biometric privacy rights

**5. Responsible Dissemination**
- Share findings in open-access venues when possible
- Make derivative datasets available with proper licensing
- Contribute back to research community
- Report potential misuse to dataset curator

---

## Known Limitations

### 1. Single-Speaker Constraint

**Limitation:** All 144 files from same speaker (Ronda Polhill)

**Implications:**
- Findings may not generalize across genders, ages, accents, cultures, languages
- Speaker-specific vocal characteristics present in all samples
- Prosodic patterns may reflect individual rather than universal patterns
- Multi-speaker validation required for broader claims

**Responsible Use:**
- State explicitly in abstracts: "single-speaker dataset"
- Do not claim findings apply to "humans" or "speakers" in general
- Combine with multi-speaker datasets for population-level research
- Frame as controlled substrate, not representative sample

### 2. Controlled Environment Bias

**Limitation:** Professional studio recordings under controlled conditions

**Implications:**
- May not reflect naturalistic speech conditions
- Scripted content (not spontaneous speech)
- Minimal acoustic variation across samples
- Single recording environment (home studio)

**Responsible Use:**
- Do not generalize to noisy, real-world conditions without validation
- Acknowledge controlled nature limits ecological validity
- Combine with naturalistic datasets for robustness testing
- Use for architectural development, not production deployment guarantees

### 3. Annotation Subjectivity

**Limitation:** Single expert annotator (speaker = annotator)

**Implications:**
- No inter-rater reliability measures
- Perceptual scores, not objective ground truth
- Potential annotator drift over recording period
- Ambivalence definitions may be subjective

**Responsible Use:**
- Treat indices as perceptual scores, not validated scales
- Do not claim "ground truth" tonality annotations
- Use as hypothesis-generating, not hypothesis-confirming
- Seek independent validation for high-stakes applications

### 4. Observational Context Limitations

**Limitation:** Empirical grounding references 8,873+ interactions (observational, not experimental)

**Implications:**
- Correlation ≠ causation (multiple confounding variables)
- ~35.85% conversion rate reflects numerous factors beyond tonality
- 68 "AI-adjacent" listener reports are anecdotal, not controlled
- Professional context may not generalize to other domains

**Responsible Use:**
- Never claim causal relationships without additional evidence
- Explicitly state "observational" or "correlational" when citing context
- Present conversion rates as motivating hypothesis, not validating evidence
- Seek controlled experimental validation

### 5. Temporal Constraint

**Limitation:** Recorded over ~1 month period (Dec 2025 - Jan 2026)

**Implications:**
- Speaker's voice may change over longer timeframes
- Seasonal or health-related vocal variations not captured
- Does not represent speaker's vocal range across years
- Limited temporal generalization

**Responsible Use:**
- Acknowledge temporal snapshot nature
- Do not assume findings stable across speaker's lifespan
- Consider temporal validation for longitudinal applications

---

## Bias Documentation

### Systematic Biases (Known and Documented)

**1. Cognitive Energy Elevation**

**Nature:** Cognitive Energy Index shows systematic elevation across corpus

**Magnitude:** Most samples score 86-100 on Cognitive Energy scale

**Causes:**
- Speaker's natural ecological style (high-energy delivery)
- Lexical content effects (professional service language)
- Potential annotator perceptual bias

**Impact:**
- May affect Trust and Empathy Resonance indices
- Limits dynamic range for Cognitive Energy modeling
- Suggests need for speaker-specific normalization

**Mitigation:**
- Documented in Notes field for affected utterances
- Intentionally retained for transparency
- Researchers should account for bias in analyses
- Consider relative comparisons within-speaker

**2. Professional Language Bias**

**Nature:** All utterances use professional service language

**Impact:**
- Tonality patterns may be domain-specific
- May not generalize to casual conversation, academic discourse, etc.
- Semantic content influences prosodic affordances

**Mitigation:**
- Clearly state "professional service domain" in publications
- Do not generalize beyond customer-facing scenarios
- Expand to multiple domains for broader applicability

**3. Gender and Age Bias**

**Nature:** Single speaker (mid-life female)

**Impact:**
- Vocal characteristics reflect specific gender and age
- May not generalize across demographic groups
- Lacks diversity in speaker representation

**Mitigation:**
- Explicitly state speaker demographics
- Multi-speaker datasets needed for demographic fairness
- Avoid making claims about "universal" prosodic patterns

### Undocumented Potential Biases

**Researchers should investigate:**
- Cultural bias (single speaker's cultural background)
- Accent bias (neutral/mobile American accent)
- Health status (speaker's vocal health during recording)
- Literacy bias (scripted, written utterances)
- Technology bias (specific microphone and recording setup)

---

## Privacy Considerations

### Speaker Identity

**Public Information:**
- Speaker identity is **not anonymous** (Ronda Polhill, dataset creator)
- Speaker voluntarily disclosed identity and provided recordings
- No expectation of anonymity

**Privacy Protections:**
- No third-party recordings or personally identifiable information beyond speaker
- No sensitive content in utterances (professional service language)
- Speaker maintains control over commercial licensing

### Data Minimization

**Only Included:**
- Audio recordings with explicit consent
- Annotation metadata (tonality scores, timestamps)
- Technical metadata (recording date, file format)
- Documentation necessary for dataset use

**Not Included:**
- Personal contact information (beyond curator email)
- Location data beyond general recording environment description
- Health information beyond vocal characteristics
- Financial information
- Social relationships or personal history

### GDPR and Privacy Law Compliance

**For EU Users:**
- Speaker has provided explicit consent (GDPR Article 6)
- Biometric data processed with informed consent (GDPR Article 9)
- Dataset creator retains data subject rights
- No automated decision-making based on dataset

**Data Subject Rights:**
- Right to access: All data publicly available
- Right to rectification: Contact ronda@TonalityPrint.com
- Right to erasure: Speaker may withdraw consent (would affect future versions)
- Right to restrict processing: CC BY-NC 4.0 limits commercial processing

---

## Commercial Use Policy

### Non-Commercial License (CC BY-NC 4.0)

**Permitted Non-Commercial Uses:**
- Academic research and education
- Non-profit organization projects
- Personal learning and experimentation
- Open-source software development (non-commercial)
- Publication in academic journals

**Prohibited Commercial Uses:**
- Training commercial voice AI products
- Integration into commercial applications
- Selling or licensing derivatives for profit
- Using in for-profit research and development
- Commercial voice cloning services

### Commercial Licensing

**For Commercial Use:**
- **Contact:** ronda@TonalityPrint.com
- **Subject Line:** "TonalityPrint Commercial License Inquiry"
- **Provide:** Intended use case, organization details, scope

**Commercial License May Include:**
- Custom terms for specific applications
- Attribution requirements
- Usage restrictions
- Royalty or licensing fees
- Derivative work rights

---

## Reporting Misuse

### How to Report

**If you observe misuse of this dataset:**

1. **Document the misuse:** Screenshots, URLs, dates, descriptions
2. **Contact dataset curator:** ronda@TonalityPrint.com
3. **Subject line:** "TonalityPrint Dataset Misuse Report"
4. **Include:**
   - Description of misuse
   - Evidence (links, screenshots, etc.)
   - Your contact information (optional)
   - Suggested action

### Types of Misuse to Report

- Unauthorized voice cloning or deepfakes
- Commercial use without licensing
- Deceptive applications
- Privacy violations
- License violations (missing attribution, etc.)
- Harmful applications
- Biometric exploitation

### Curator Responsibilities

**Upon receiving misuse report, curator will:**
1. Investigate reported misuse
2. Contact responsible parties if identifiable
3. Request removal or compliance
4. Escalate to legal counsel if necessary
5. Update documentation with lessons learned

---

## Responsible AI Alignment Use

### Safety-Critical Applications

**For AI Safety Research:**
- Dataset designed to help AI systems express uncertainty (ambivalence)
- Useful for "truthfulness calibration" - aligning confidence with vocal doubt
- Applicable to healthcare, autonomous systems, high-stakes decision support

**Safety Considerations:**
- Do not rely solely on this dataset for production safety systems
- Single-speaker data insufficient for population safety guarantees
- Validate findings across diverse speakers and contexts
- Consider failure modes and edge cases

### Ambivalence Detection Ethics

**Appropriate Uses:**
- Detecting when AI should express uncertainty
- Modeling human emotional complexity
- Training nuanced dialogue systems

**Inappropriate Uses:**
- Lie detection or deception identification (not validated)
- Emotional manipulation or exploitation
- Mental health diagnosis (not clinical data)
- Coercive persuasion systems

---

## Accessibility and Inclusion

### Dataset Limitations for Inclusion

**This dataset does not represent:**
- Multiple genders (single female speaker)
- Multiple age groups (mid-life only)
- Multiple accents (neutral American only)
- Multiple languages (English only)
- Multiple cultural backgrounds (single speaker)
- Voice disorders or atypical speech
- Children or elderly speakers

**Recommendations for Inclusive Research:**
- Combine with diverse multi-speaker datasets
- Acknowledge lack of representativeness
- Seek complementary data for underrepresented groups
- Do not make universal claims based on single speaker

---

## Researcher Responsibilities

### Ethical Checklist for Dataset Users

Before using TonalityPrint, researchers should:

- [ ] Read and understand CC BY-NC 4.0 license terms
- [ ] Review prohibited uses and commit to ethical compliance
- [ ] Acknowledge single-speaker limitation in research design
- [ ] Plan proper attribution in publications
- [ ] Document known biases in analysis
- [ ] Obtain commercial license if needed
- [ ] Consider multi-speaker validation for generalizable claims
- [ ] Protect speaker's biometric privacy
- [ ] Report any misuse encountered
- [ ] Share findings and code openly when possible

### Institutional Review

**For Academic Institutions:**
- IRB review may not be required (publicly available, consented data)
- Consult your institution's policies on secondary data use
- Some applications (e.g., voice cloning research) may require oversight
- Ensure compliance with institutional ethics guidelines

---

## Updates and Versioning

### Ethical Guidelines Versioning

**Current Version:** 1.0.0 (January 24, 2026)

**Future Updates May Include:**
- Additional prohibited uses based on emerging threats
- Updated privacy considerations
- Refined responsible use guidelines
- Lessons learned from community feedback

**How to Stay Informed:**
- Monitor Zenodo record for updates: https://doi.org/10.5281/zenodo.17913895
- Subscribe to dataset announcements (contact ronda@TonalityPrint.com)
- Check GitHub repository for latest guidelines

---

## Contact for Ethical Questions

**Dataset Curator:** Ronda Polhill  
**Email:** ronda@TonalityPrint.com

**For Questions About:**
- Ethical use guidance
- Commercial licensing
- Misuse reporting
- Privacy concerns
- Bias documentation
- Responsible AI applications

---

## Acknowledgment of Limitations

This document represents the dataset creator's best effort to anticipate and address ethical considerations. However:

- Ethical guidelines may evolve as new applications emerge
- Unforeseen misuse scenarios may arise
- Community feedback will inform future updates
- Researchers bear ultimate responsibility for ethical use

**The dataset creator cannot be held liable for:**
- Misuse by third parties
- Unintended consequences of research
- Applications beyond stated intentions
- Derivative works that violate ethical guidelines

**Researchers are encouraged to:**
- Think critically about potential harms
- Engage with AI ethics community
- Publish findings on ethical challenges
- Contribute to responsible AI development

---

## Conclusion

TonalityPrint Voice Dataset v1.0 was created with careful attention to ethical considerations, speaker consent, and transparency about limitations. Users of this dataset inherit the responsibility to:

1. **Respect speaker consent** by adhering to prohibited use restrictions
2. **Acknowledge limitations** in research and publications
3. **Protect privacy** and biometric integrity
4. **Use responsibly** for beneficial research applications
5. **Report misuse** to support community accountability

By using this dataset, you agree to uphold these ethical principles and contribute to responsible voice AI research.

---

**Version:** 1.0.0  
**Last Updated:** January 24, 2026  
**License:** CC BY-NC 4.0  
**© 2026 Ronda Polhill**
