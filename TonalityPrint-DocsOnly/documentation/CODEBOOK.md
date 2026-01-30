# CODEBOOK - TonalityPrint Voice Dataset v1.0

## Overview

This codebook provides  definitions for variables, file naming conventions, and data structures in the TonalityPrint Voice Dataset v1.0.

**Dataset Information**:
- **Total Files**: 144 audio files + 144 JSON + 144 CSV + 1 combined CSV
- **DOI**: https://doi.org/10.5281/zenodo.17913895
- **License**: CC BY-NC 4.0
- **Contact**: ronda@TonalityPrint.com

**Quick Navigation**:
- [File Naming Convention](#file-naming-convention)
- [CSV Variables](#csv-variables-23-columns)
- [Tonality Indices](#tonality-indices-0-100-scale)
- [Intention Categories](#intention-categories)
- [Modifier Codes](#modifier-codes-24-optional-sub-modifiers)
- [Segment-Level Data](#segment-level-data-structure)

---

## File Naming Convention

### Audio Files (.wav)

**Structure**:
```
[Version]_[Batch]_[Utterance]_[Type]_[Intention]_[Modifier]_[Ambivalence]_[Speaker].wav
```

**Examples**:
1. **Single** (Primary Intent only):  
   `TPV1_B1_UTT1_S_Att_SP-Ronda.wav`
   
2. **Compound** (Primary Intent + Sub-modifier):  
   `TPV1_B1_UTT1_S_Reci_affi_SP-Ronda.wav`
   
3. **Complex** (Primary Intent + Sub-modifier + Ambivalence):  
   `TPV1_B1_UTT1_S_Reci_affi_ambivalex_SP-Ronda.wav`

### Component Definitions

| Component | Description | Valid Values | Example |
|-----------|-------------|--------------|---------|
| **Version** | Dataset version | `TPV1` | TPV1 |
| **Batch** | Batch number (1-6) | `B1`, `B2`, `B3`, `B4`, `B5`, `B6` | B1 |
| **Utterance** | Utterance ID (1-18) | `UTT1` through `UTT18` | UTT1 |
| **Type** | Statement/Question | `S` (Statement), `Q` (Question) | S |
| **Intention** | Primary tonal intent | `Att`, `Trus`, `Reci`, `Emre`, `Cogen`, `Baseneutral` | Att |
| **Modifier** | Optional sub-modifier | See [Modifier Codes](#modifier-codes-24-optional-sub-modifiers) | affi, calm |
| **Ambivalence** | Ambivalence marker | `ambivalex` (or omitted) | ambivalex |
| **Speaker** | Speaker identifier | `SP-Ronda` | SP-Ronda |

---

## CSV Variables (23 Columns)

### Complete Variable List

The combined CSV file (`ALL_TONALITY_DATA_COMBINED.csv`) and individual CSV files contain these 23 variables:

| # | Variable Name | Type | Description |
|---|--------------|------|-------------|
| 1 | `Version` | String | Dataset version identifier |
| 2 | `Batch_Number` | String | Batch identifier (B1-B6) |
| 3 | `Utterance_Number` | String | Utterance identifier (UTT1-UTT18) |
| 4 | `Utterance_Type` | String | S (Statement) or Q (Question) |
| 5 | `File_Name` | String | Complete audio filename |
| 6 | `Primary_Intention` | String | Primary tonal intent category |
| 7 | `Sub_Modifier` | String | Optional sub-modifier (or empty) |
| 8 | `Ambivalex` | String | Ambivalence marker (or empty) |
| 9 | `Speaker` | String | Speaker name |
| 10 | `Utterance_Text` | String | Transcribed utterance text |
| 11 | `Trust_Index` | Integer | Trust tonality score (0-100) |
| 12 | `Reciprocity_Index` | Integer | Reciprocity score (0-100) |
| 13 | `Empathy_Resonance_Index` | Integer | Empathy resonance score (0-100) |
| 14 | `Cognitive_Energy_Index` | Integer | Cognitive energy score (0-100) |
| 15 | `Attention_Index` | Integer | Attention score (0-100) |
| 16 | `Notes` | String | Annotation notes and observations |
| 17 | `Duration` | Time | Utterance duration (MM:SS format) |
| 18 | `Date_Recorded` | Date | Recording date (YYYY-MM-DD) |
| 19 | `Source` | String | Data source description |
| 20 | `Segments` | JSON String | Time-aligned segment data |
| 21 | `Start_Time` | Time | Utterance start time (MM:SS) |
| 22 | `End_Time` | Time | Utterance end time (MM:SS) |
| 23 | `Timestamp` | DateTime | ISO 8601 timestamp |

---

## Variable Definitions (Detailed)

### Metadata Variables

#### 1. Version
- **Type**: String
- **Description**: Dataset version identifier
- **Values**: `"TPV1"` (TonalityPrint Version 1)
- **Example**: `TPV1`

#### 2. Batch_Number
- **Type**: String
- **Description**: Recording batch identifier
- **Values**: `B1`, `B2`, `B3`, `B4`, `B5`, `B6`
- **Total Batches**: 6
- **Utterances per Batch**: 18
- **Example**: `B1`

#### 3. Utterance_Number
- **Type**: String
- **Description**: Unique utterance identifier within each batch
- **Values**: `UTT1`, `UTT2`, ..., `UTT18`
- **Example**: `UTT1`

#### 4. Utterance_Type
- **Type**: String (Categorical)
- **Description**: Syntactic type of the utterance
- **Values**:
  - `S` = Statement (declarative sentence)
  - `Q` = Question (interrogative sentence)
- **Distribution**: ~83% Statements, ~17% Questions
- **Example**: `S`

#### 5. File_Name
- **Type**: String
- **Description**: Complete audio filename with extension
- **Format**: `TPV1_[Batch]_[Utterance]_[Type]_[Intention]_[Modifier]_[Ambivalence]_SP-Ronda.wav`
- **Example**: `TPV1_B1_UTT1_S_Att_SP-Ronda.wav`

#### 6. Primary_Intention
- **Type**: String (Categorical)
- **Description**: Primary functional tonal intent category
- **Values**:
  - `Attention` (directing focus and engagement)
  - `Trust` (conveying reliability and credibility)
  - `Reciprocity` (expressing mutual exchange)
  - `Empathy Resonance` (demonstrating empathetic connection)
  - `Cognitive Energy` (showing mental engagement)
  - `Baseline Neutral` (neutral control sample)
- **Note**: Full word used in CSV (e.g., "Attention"), abbreviated in filename (e.g., "Att")
- **Example**: `Attention`

#### 7. Sub_Modifier
- **Type**: String (Optional)
- **Description**: Optional sub-modifier providing nuanced tonality descriptor
- **Values**: See [Modifier Codes](#modifier-codes-24-optional-sub-modifiers) table
- **Missing Data**: Empty string if not applicable
- **Example**: `affi` (Affirming), empty string `""`

#### 8. Ambivalex
- **Type**: String (Optional)
- **Description**:  Cross-modifier Ambivalence marker indicating mixed or transitional tonality
- **Values**: 
  - `ambivalex` = Ambivalence present
  - Empty string = No ambivalence
- **Definition**: Two or more contradictory/competing sub-modifier layers present simultaneously
- **Example**: `ambivalex`, empty string `""`

#### 9. Speaker
- **Type**: String
- **Description**: Speaker identifier
- **Values**: `Ronda`
- **Note**: Single-speaker dataset (all 144 files same speaker)
- **Example**: `Ronda`

#### 10. Utterance_Text
- **Type**: String
- **Description**: Verbatim transcription of spoken utterance
- **Encoding**: UTF-8
- **Max Length**: ~200 characters
- **Example**: `"I want to make sure I understand what you need"`

---

### Tonality Indices (0-100 Scale)

All five tonality indices are measured on a continuous 0-100 scale where higher values indicate stronger presence of the measured tonal quality.

#### 11. Trust_Index
- **Type**: Integer
- **Range**: 0-100
- **Description**: Quantified measure of trust tonality (perceived safety, authenticity, credibility)
- **Interpretation**:
  - **Low (0-33)**: Uncertain, hesitant tonality
  - **Moderate (34-66)**: Moderately reliable tonality
  - **High (67-100)**: Highly trustworthy tonality
- **Example**: `75`

#### 12. Reciprocity_Index
- **Type**: Integer
- **Range**: 0-100
- **Description**: Quantified measure of reciprocal/collaborative tonality (inviting response, conversational balance)
- **Interpretation**:
  - **Low (0-33)**: Unilateral communication
  - **Moderate (34-66)**: Somewhat collaborative
  - **High (67-100)**: Highly collaborative, balanced
- **Example**: `93`

#### 13. Empathy_Resonance_Index
- **Type**: Integer
- **Range**: 0-100
- **Description**: Quantified measure of empathetic tonality (emotional attunement, mirroring listener state)
- **Interpretation**:
  - **Low (0-33)**: Detached, impersonal
  - **Moderate (34-66)**: Moderately attuned
  - **High (67-100)**: Highly empathetic, warm
- **Example**: `76`

#### 14. Cognitive_Energy_Index
- **Type**: Integer
- **Range**: 0-100
- **Description**: Quantified measure of cognitive engagement and mental energy (activation, momentum, pacing)
- **Interpretation**:
  - **Low (0-33)**: Low engagement, slow pacing
  - **Moderate (34-66)**: Moderate engagement
  - **High (67-100)**: High mental energy, dynamic
- **Known Issue**: Shows systematic elevation across corpus (see Notes)
- **Example**: `96`

#### 15. Attention_Index
- **Type**: Integer
- **Range**: 0-100
- **Description**: Quantified measure of attentional focus (directing perceptual priority, maintaining engagement)
- **Interpretation**:
  - **Low (0-33)**: Unfocused, diffuse attention
  - **Moderate (34-66)**: Moderately engaged
  - **High (67-100)**: Highly focused, commanding attention
- **Example**: `80`

**Scoring Methodology**: All indices were scored by expert practitioner trained in "Tonality as Attention" framework based on perceptual assessment and acoustic analysis.

---

### Additional Variables

#### 16. Notes
- **Type**: String (Free text)
- **Description**: Annotation notes, quality observations, and systematic bias documentation
- **Common Note**: "Cognitive Energy (CE) seemingly exhibits systemic leaks/dominance, possibly due to speaker ecological style, lexical content and /or practitioner bias. Intentionally retained for transparency."
- **Missing Data**: Empty string if no notes
- **Example**: `"Cognitive Energy (CE) seemingly exhibits systemic leaks/dominance..."`

#### 17. Duration
- **Type**: Time (MM:SS format)
- **Description**: Total duration of audio utterance
- **Format**: `M:SS` or `MM:SS`
- **Range**: ~3-6 seconds per utterance
- **Total Duration**: ~10 minutes (all 144 files)
- **Example**: `0:04` (4 seconds)

#### 18. Date_Recorded
- **Type**: Date (YYYY-MM-DD)
- **Description**: Date the audio was recorded
- **Date Range**: December 19, 2025 - January 23, 2026
- **Example**: `2026-01-20`

#### 19. Source
- **Type**: String
- **Description**: Data source and annotation method
- **Values**: `"Recording - Expert Practitioner Annotator"`
- **Note**: All annotations performed by single expert practitioner
- **Example**: `Recording - Expert Practitioner Annotator`

#### 20. Segments
- **Type**: JSON Array (stored as string in CSV)
- **Description**: Time-aligned segment-level tonality data with millisecond precision
- **Structure**: Array of objects with `startTime`, `endTime`, and five tonality indices
- **See**: [Segment-Level Data Structure](#segment-level-data-structure) section
- **Example**: `[{"startTime":0,"endTime":4284.083333333333,"trust":75,"reciprocity":93,"empathy":76,"cognitive":96,"attention":80}]`

#### 21. Start_Time
- **Type**: Time (MM:SS format)
- **Description**: Utterance start time (typically 0:00)
- **Example**: `0:00`

#### 22. End_Time
- **Type**: Time (MM:SS format)
- **Description**: Utterance end time (matches Duration)
- **Example**: `0:04`

#### 23. Timestamp
- **Type**: DateTime (ISO 8601 format)
- **Description**: Precise timestamp of annotation creation
- **Format**: `YYYY-MM-DDTHH:MM:SS.sssZ`
- **Timezone**: UTC (Z suffix)
- **Example**: `2026-01-20T16:45:24.342Z`

---

## Intention Categories

### Primary Functional Tonal Intent States (6 Categories)

| Category | Code (Filename) | Full Name (CSV) | Description |
|----------|----------------|-----------------|-------------|
| **Attention** | `Att` | `Attention` | Directing focus, capturing and maintaining listener engagement |
| **Trust** | `Trus` | `Trust` | Conveying trustworthiness, reliability, credibility, and authenticity |
| **Reciprocity** | `Reci` | `Reciprocity` | Expressing mutual exchange, collaborative communication, inviting response |
| **Empathy Resonance** | `Emre` | `Empathy Resonance` | Demonstrating empathetic connection, emotional attunement, warmth |
| **Cognitive Energy** | `Cogen` | `Cognitive Energy` | Showing mental engagement, cognitive processing, activation, momentum |
| **Baseline Neutral** | `Baseneutral` | `Baseline Neutral` | Neutral control sample, default prosody for comparative analysis |

**Capitalization Rules**:
- First letter capitalized in filenames: `Att`, `Cogen`
- Full words in CSV: `Attention`, `Cognitive Energy`
- Baseline: `Baseneutral` (one word, capital B)

---

## Modifier Codes (24 Optional Sub-Modifiers)

### 1. Trust Modifiers (5)

| Code | Full Name | Description |
|------|-----------|-------------|
| `auth` | Authoritative | Commanding, expert tone |
| `calm` | Calm | Soothing, measured tone |
| `conf` | Confident | Self-assured, certain tone |
| `rest` | Formal/Respectful | Professional, courteous tone |
| `reas` | Reassuring | Comforting, supportive tone |

### 2. Attention Modifiers (5)

| Code | Full Name | Description |
|------|-----------|-------------|
| `cert` | Certainty | Confident, definite tone |
| `clar` | Clarity | Clear, precise communication |
| `curi` | Curious | Inquisitive, interested tone |
| `focu` | Focused | Concentrated, directed attention |
| `urge` | Urgent/Pressure | Time-sensitive, pressing tone |

### 3. Reciprocity Modifiers (5)

| Code | Full Name | Description |
|------|-----------|-------------|
| `affi` | Affirming | Validating, confirming tone |
| `colla` | Collaborative | Cooperative, team-oriented tone |
| `enga` | Engaged | Active, participatory tone |
| `open` | Open | Receptive, non-defensive tone |
| `refl` | Reflective | Thoughtful, contemplative tone |

### 4. Empathy Resonance Modifiers (5)

| Code | Full Name | Description |
|------|-----------|-------------|
| `casu` | Casual | Informal, relaxed tone |
| `comp` | Compassion | Kind, caring tone |
| `corr` | Corrective (softened) | Gentle correction or guidance |
| `symp` | Sympathetic | Understanding, supportive tone |
| `warm` | Warm | Friendly, approachable tone |

### 5. Cognitive Energy Modifiers (4)

| Code | Full Name | Description |
|------|-----------|-------------|
| `ana` | Analytical | Logical, reasoning-oriented tone |
| `dyna` | Dynamic | Energetic, active tone |
| `enth` | Enthusiastic | Excited, passionate tone |
| `skep` | Skeptical | Questioning, doubtful tone |

### Cross-Intent Modifier (1)

| Code | Full Name | Description |
|------|-----------|-------------|
| `ambivalex` | Ambivalence | Mixed, transitional, or competing tonal cues present simultaneously |

**Capitalization Rule**: All modifier codes are lowercase in filenames: `affi`, `warm`, `ana`, `ambivalex`

---

## Segment-Level Data Structure

### JSON Structure in "Segments" Field

Each utterance includes time-aligned segment-level tonality data stored as a JSON array string in the CSV.

**Structure**:
```json
[
  {
    "startTime": <milliseconds>,
    "endTime": <milliseconds>,
    "trust": <0-100>,
    "reciprocity": <0-100>,
    "empathy": <0-100>,
    "cognitive": <0-100>,
    "attention": <0-100>
  }
]
```

**Real Example**:
```json
[{
  "startTime": 0,
  "endTime": 4284.083333333333,
  "trust": 75,
  "reciprocity": 93,
  "empathy": 76,
  "cognitive": 96,
  "attention": 80
}]
```

### Segment Field Definitions

| Field | Type | Unit | Description |
|-------|------|------|-------------|
| `startTime` | Float | Milliseconds | Segment start time from utterance beginning |
| `endTime` | Float | Milliseconds | Segment end time from utterance beginning |
| `trust` | Integer | 0-100 | Trust tonality score for this segment |
| `reciprocity` | Integer | 0-100 | Reciprocity score for this segment |
| `empathy` | Integer | 0-100 | Empathy resonance score for this segment |
| `cognitive` | Integer | 0-100 | Cognitive energy score for this segment |
| `attention` | Integer | 0-100 | Attention score for this segment |

**Notes**:
- Most utterances contain a single segment (entire utterance)
- Times in milliseconds with decimal precision
- Segment scores may differ from utterance-level indices in multi-segment utterances
- To convert milliseconds to seconds: `seconds = milliseconds / 1000`

---

## Missing Data Codes

### How Missing Data is Represented

| Field Type | Missing Data Representation |
|-----------|----------------------------|
| String fields (Sub_Modifier, Ambivalex, Notes) | Empty string `""` |
| Numeric fields | No missing data (all utterances fully annotated) |
| Segments | No missing data (all utterances have segment data) |

**Important**: 
- There is **NO use of** `-999`, `NULL`, `NA`, or other special missing data codes
- Empty string `""` indicates "not applicable" for optional fields
- All tonality indices are complete (no missing values)

---

## Statistical Summary

### Dataset Overview

| Statistic | Value |
|-----------|-------|
| Total Utterances | 144 |
| Total Batches | 6 |
| Utterances per Batch | 18 |
| Single Speaker | Yes (Ronda) |
| Language | English (American) |
| Recording Period | Dec 19, 2025 - Jan 23, 2026 |
| Total Duration | ~10 minutes |

### Audio Specifications

| Specification | Value |
|---------------|-------|
| Sample Rate | 48,000 Hz |
| Bit Depth | 16-bit |
| Channels | Mono (1) |
| Format | WAV (uncompressed PCM) |
| Duration Range | 3-6 seconds per file |

### Index Distributions

*Note: Actual statistical summaries (mean, SD, min, max) should be calculated from the complete dataset.*

**Expected Patterns**:
- Cognitive_Energy_Index: Known systematic elevation (typically 90-100)
- Other indices: Expected to vary by Primary_Intention category
- See METHODOLOGY.md for quality control discussion

---

## Known Issues & Limitations

### Cognitive Energy Systematic Bias

**Issue**: Cognitive_Energy_Index shows systematic elevation across most utterances, regardless of Primary_Intention category.

**Possible Causes** (as noted in dataset documentation):
1. Speaker's ecological style (natural high-energy delivery)
2. Lexical content effects
3. Practitioner bias in scoring

**Resolution**: Intentionally retained for transparency and to reflect ecological reality of speech production. Researchers should account for this bias in analyses.

**Impact**: 
- Trust and Empathy Resonance indices most affected
- Suggests need for speaker-specific normalization in some applications
- Does not invalidate other tonality measures

### Single-Speaker Limitation

- All 144 files from same speaker (Ronda)
- Findings may not generalize to other speakers
- Multi-speaker extension needed for broader applicability

### Controlled Environment

- Professional studio recordings
- May not reflect naturalistic speech conditions
- Scripted content (not spontaneous speech)

---

## Usage Notes

### Loading Data in Python

```python
import pandas as pd
import json

# Load combined CSV
df = pd.read_csv('ALL_TONALITY_DATA_COMBINED.csv')

# Parse Segments JSON
df['Segments_Parsed'] = df['Segments'].apply(json.loads)

# Access first segment's trust score
first_segment_trust = df['Segments_Parsed'].iloc[0][0]['trust']
```

### Loading Data in R

```r
library(readr)
library(jsonlite)

# Load CSV
data <- read_csv('ALL_TONALITY_DATA_COMBINED.csv')

# Parse Segments JSON
data$Segments_Parsed <- lapply(data$Segments, fromJSON)

# Access segment data
first_segment <- data$Segments_Parsed[[1]][[1]]
```

### Filtering by Intention

```python
# Get all Attention utterances
attention_data = df[df['Primary_Intention'] == 'Attention']

# Get all utterances with ambivalence
ambivalent_data = df[df['Ambivalex'] == 'ambivalex']

# Get Trust utterances with calm modifier
trust_calm = df[
    (df['Primary_Intention'] == 'Trust') & 
    (df['Sub_Modifier'] == 'calm')
]
```

---

## Citation

When using this dataset, please cite:

```bibtex
@dataset{polhill_2026_tonalityprint,
  author       = {Polhill, Ronda},
  title        = {TonalityPrint: A Contrast-Structured Voice Dataset for Exploring Functional Tonal Intent, Ambivalence, and Inference-Time Prosodic Alignment v1.0},
  year         = 2026,
  publisher    = {Zenodo},
  version      = {1.0.0},
  doi          = {10.5281/zenodo.17913895},
  url          = {https://doi.org/10.5281/zenodo.17913895}
}
```

---

## Contact

**Dataset Curator**: Ronda Polhill  
**Email**: ronda@TonalityPrint.com  
**DOI**: https://doi.org/10.5281/zenodo.17913895

For questions about:
- Variable definitions → This codebook
- Annotation methodology → METHODOLOGY.md
- Dataset usage → DATACARD.md
- Technical issues → ronda@TonalityPrint.com

---

**Version**: 1.0.0  
**Last Updated**: January 24, 2026  
**License**: CC BY-NC 4.0
