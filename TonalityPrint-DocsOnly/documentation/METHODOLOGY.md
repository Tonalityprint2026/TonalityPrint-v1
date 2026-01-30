\# METHODOLOGY \- TonalityPrint Voice Dataset v1.0

\#\# Research Framework

\#\#\# Theoretical Foundation: "Tonality as Attention"

The TonalityPrint Voice Dataset supports the *Tonality as Attention* theoretical framework, developed by researcher Ronda Polhill, which proposes that human vocal tonality may serve as a primary mechanism for directing and modulating attention in human-AI communications.

Further, unlike traditional emotion datasets that ssuccessfully categorize static affective states (e.g., "Happy," "Sad"), the TonalityPrint specialized corpus focuses on **Functional Tonal Intents** \- active signals used to orient focus, calibrate trust, regulate reciprocity, and signal cognitive state during complex dialogue. The dataset is designed to support **Differential Latent Analysis (DLA)**, a hypothesized protocol for isolating these socio-pragmatic features by holding lexical content and speaker identity for existing contrastive steering methods .

\---

\#\# Data Collection

\#\#\# Recording Environment

\*\*Location\*\*: Controlled home studio    
\*\*Acoustic Treatment\*\*: Minimal ambient noise, consistent conditions across all recordings    
\*\*Speaker Position\*\*: Seated, consistent positioning maintained throughout recording sessions

\*\*Recording Equipment\*\*:  
\- \*\*Microphone\*\*: Blue Yeti USB microphone  
  \- Mode: Cardioid (directional)  
  \- Distance: \~6-8 inches from speaker  
\- \*\*Recording Software\*\*: Audacity  
  \- Real-time effects: Disabled (to preserve original tonality signal)  
  \- Preset settings: Consistent across all recordings

\*\*Technical Specifications\*\*:  
\- \*\*Recording Format\*\*: 48kHz, 32-bit float WAV (captured in Audacity)  
\- \*\*Output Format\*\*: 48kHz, 16-bit PCM WAV (uncompressed)  
\- \*\*Sample Rate\*\*: 48,000 Hz (48 kHz)  
\- \*\*Bit Depth\*\*: 16-bit (final output)  
\- \*\*Channels\*\*: Mono (1 channel)  
\- \*\*File Format\*\*: WAV (uncompressed PCM)

\*\*Post-Processing Policy\*\*:  
To preserve 100% human tonality variance and support maximum fidelity for micro-tonal expression analysis, this dataset provides \*\*raw, unprocessed audio files\*\*:

* **Processing:** **None.** No EQ, compression, or noise reduction was applied. Real-time effects were intentionally disabled to preserve raw tonal fidelity for analysis.

\*\*Note\*\*: Minimal background noise may be present in some recordings. This was intentional to avoid altering nuanced vocal tonality through post-processing artifacts.

\#\#\# Speaker Information

\*\*Speaker\*\*: Ronda (single speaker dataset)    
\*\*Language\*\*: Native English speaker, Neutral/Mobile American Accent    
\*\*Speaker Characteristics\*\*:  
\- Experienced in vocal tonality modulation  
\- Developed the "Tonality as Attention" framework

\*\*Speaker Consent\*\*: Full informed consent obtained for recording, annotation, and public dataset release.

\#\#\# Recording Procedure

\#\#\#\# Utterance   
The dataset was collected across \*\*6 batches\*\* (B1-B6), with each batch containing \*\*18 utterances\*\*.

\*\*Timeline\*\*:  
\- First recordings: December 2025  
\- Final recordings: January 2026  
\- Total collection period: \~1 month

\*\*Dataset Statistics\*\*:  
\- \*\*Total Files\*\*: 144 audio samples  
\- \*\*Duration per File\*\*: 3-6 seconds (approximately)  
\- \*\*Total Duration\*\*: \~11 minutes 5 seconds  
\- \*\*Single Speaker\*\*: All files recorded by Ronda

\#\#\#\# Utterance Design:

## 

The core structure of the corpus is the "**Fixed-Phrase Octet**." This design explores lexical and biometric variability to isolate prosodic intent as the primary variable.

* **Structure:** 18 utterances X 8 parallel prosodic states.

Each utterance was deliberately crafted to express specific tonality intentions, the **8 Parallel States,** recorded as follows::

1\. \*\*Baseline Creation\*\*:  (1) Neutral baseline utterances established for comparison  
2\. \*\*Intention Targeting\*\*: (5) Utterances designed to emphasize specific tonality dimensions:  
   \- Attention (Att)  
   \- Trust (Trus)  
   \- Reciprocity (Reci)  
   \- Empathy Resonance (Emre)  
   \- Cognitive Energy (Cogen)

3\. \*\*Modifier Application\*\*: (1) Sub-category modifiers added nuance:  
   \- Affirmative, collaborative, calm, corrective, engaged, etc.

4\. \*\*Ambivalence Encoding\*\*: (1) Select utterances intentionally crafted to express complex or mixed tonality (marked as "ambivalex")

\#\#\#\# Recording Protocol

1\. \*\*Pre-Recording Setup\*\*:  
   \- Blue Yeti microphone positioned 6-8 inches from speaker  
   \- Cardioid mode selected for directional recording  
   \- Audacity configured: 48kHz, 32-bit float, mono  
   \- Real-time effects disabled to preserve natural tonality  
   \- Audio levels calibrated to avoid clipping  
   \- Speaker reviews utterance text  
   \- Speaker mentally prepares tonality intention (Primary \+ Modifier \+ Ambivalence if applicable)

2\. \*\*Recording Capture\*\*:  
   \- Speaker delivers utterance with intended tonality  
   \- Recording captured at 48kHz, 32-bit float in Audacity  
   \- Minimal silence at beginning and end (natural speech boundaries)  
   \- No real-time processing applied during capture  
   \- Raw audio preserved without noise reduction or effects

3\. \*\*Immediate Quality Check\*\*:  
   \- Playback review immediately after recording  
   \- Check for technical issues (clipping, background noise, mic artifacts)  
   \- Re-recording if necessary to meet quality standards  
   \- Final approval by speaker/researcher

4\. \*\*Export & File Naming\*\*:  
   \- Export from Audacity as 16-bit PCM WAV (48kHz, mono)  
   \- No post-processing, normalization, or effects applied  
   \- Files named using systematic convention:  
     \- Format: \`TPV1\_\[Batch\]\_\[Utterance\]\_\[Type\]\_\[Intent\]\_\[Modifier\]\_\[Ambivalex\]\_SP-Ronda.wav\`  
   \- Names encode: Version, Batch, Utterance number, Type, Intention, Modifier, Ambivalence, Speaker  
\---

\#\# Annotation Methodology

### **A. Functional \-** Defined not by *feeling*, but by *doing*

* **Functional Tonal Intents:**  5 primary functional tonal intents  
* Sub-modifiers:  24 optional sub-modifiers   
* **Cross modifier:**   Ambivalence (annotated ambivalex when applicable), treated as perceptual entropy, cross-intent feature rather than "noise." It represents transitional states where the speaker simultaneously expresses competing intentions (e.g., "Trust" but "Guarded"), effectively modeling uncertainty.

**B. Multi-layered, Human-in-the-Loop (HITL**) \- TonalityPrint v1.0 utilizes an annotation architecture. This process aims to ensure that primary Functional Tonal Intent labels are grounded in both real-world performance capability and objective spectral data.

\#\#\# Expert Practitioner Annotation  
Annotations were not derived from post-hoc labeling of random speech, rather from a **practitioner-verified forward protocol** grounded in high-stakes interaction outcomes.

\*\*Annotator\*\*: Ronda Polhill (speaker and dataset creator)    
\*\*Expertise\*\*: Expert practitioner, architect of the "Tonality as Attention" framework with real-world application

\*\*Further Practitioner Background\*\*:  
\- \*\*Experience Base\*\*: 8,873+ high-stakes customer interactions (July 2024 \- March 2025\)  
\- ***Generative Hypothesis, Not Causal Proof:*** \*\*Performance Context\*\*: \~35.85% average conversion rate during observation period  
\- \*\*Tonality Expertise\*\*: Documented ability to modulate tonality adaptively in consequential interactions  
\- \*\*Framework Application\*\*: Practical experience developing/implementing "Tonality as Attention" principles in real-time

\*\*Ecological Provenance\*\*:

This dataset is grounded in **ecological feasibility**.

Annotations reflect tonality patterns motivated by real-world deployment rather than theoretical constructs. The practitioner's annotation decisions are informed by:  
\- Observed correlations between specific tonal patterns and interaction outcomes  
\- Trial-and-error refinement across thousands of high-stakes conversations  
\- Direct feedback from 168+ customer interactions with 68 unsolicited comments about *’AI-adjacent, yet trusted’* voice tone quality

* **Practitioner Note:** A subset of interactions (*n=68*) involved spontaneous listener feedback describing the voice as "AI-adjacent" or "robotic" while maintaining high trust. This counter-intuitive finding \- that "robotic" precision can co-occur with trust \- motivated the rigorous isolation of TonalityPrint’s specific functional Primary Tonal Intent states.

\*\*Annotation Method\*\*: Expert perceptual assessment combined with acoustic analysis    
\*\*Source Designation\*\*: "Recording \- Expert Practitioner Annotator"

\#\#\# Annotation Process

\#\#\#\# 1\. Practitioner Perceptual Scoring

\*\*Primary Method\*\*: Expert perceptual assessment    
The practitioner (Ronda) scored each utterance based on:  
\- Intensive familiarity with tonality dimensions from real-world application  
\- Perceptual assessment of tonal intent as expressed in the recording  
\- Reference to internal calibration developed through 8,873+ customer interactions

\*\*Scoring Protocol\*\*:  
\- Each utterance reviewed immediately after recording  
\- All five tonality indices scored independently on 0-100 scale  
\- Primary intention category and modifiers assigned  
\- Ambivalence marker applied when competing tonal cues detected  
\- Notes added for quality observations or systematic patterns

\#\#\#\# 2\. Acoustic Analysis Support

While primary scoring was perceptual, acoustic features were considered including:  
\- Fundamental frequency (F0) patterns and pitch contours  
\- Speech rate and temporal dynamics  
\- Energy contours and amplitude variations  
\- Vocal quality and resonance characteristics

\#\#\#\# 3\. Quality Control \- Proprietary Heuristic Audit

\*\*Audit Process\*\*:  
After initial annotation, all samples underwent blind, proprietary heuristic audit to verify consistency:  
\- Acoustic profiles analyzed without access to practitioner labels  
\- Samples flagged when acoustic features diverged from stated intention  
\- Flagged samples reviewed for potential re-recording

\*\*Audit Results\*\*:  
\- \*\*\~80+% alignment rate\*\*: Acoustic profiles matched intended tonal intent categories  
\- \*\*\~18.05% re-recorded\*\*: Samples where acoustic features diverged were re-recorded  
\- \*\*Cross-intent patterns\*\*: Cognitive Energy systematically elevated (intentionally retained)

\*\*Resolution Process\*\*:  
\- Samples with acoustic-intent misalignment were reviewed  
\- If acoustic profile didn't support intended tonality, utterance was re-recorded  
\- Some divergences retained as genuine ambivalence or tonal complexity  
\- All decisions documented in Notes field

\#\#\#\# 4\. Tonality Index Scoring

Each utterance receives five tonality index scores (0-100 scale) based on expert practitioner assessment:

\*\*Trust Index (0-100)\*\*:  
\- \*\*Definition\*\*: Perceived safety, authenticity, stability, or credibility conveyed through tonal authority and controlled resonance  
\- \*\*Perceptual Indicators\*\*: Vocal steadiness, warm resonance, consistent pitch, relaxed quality  
\- \*\*Interpretation\*\*:   
  \- Low (0-33): Uncertain, hesitant  
  \- Moderate (34-66): Moderately reliable  
  \- High (67-100): Highly trustworthy

\*\*Reciprocity Index (0-100)\*\*:  
\- \*\*Definition\*\*: How tonality invites response, signals openness, and creates conversational balance rather than dominance  
\- \*\*Perceptual Indicators\*\*: Invitational intonation, cooperative prosody, turn-taking signals  
\- \*\*Interpretation\*\*:  
  \- Low (0-33): Unilateral, one-sided  
  \- Moderate (34-66): Somewhat collaborative  
  \- High (67-100): Highly collaborative, balanced

\*\*Empathy Resonance Index (0-100)\*\*:  
\- \*\*Definition\*\*: Function of emotional attunement where vocal tone mirrors or harmonizes to perceived listener state  
\- \*\*Perceptual Indicators\*\*: Warm tone, gentle inflections, emotional openness, attuned quality  
\- \*\*Interpretation\*\*:  
  \- Low (0-33): Detached, impersonal  
  \- Moderate (34-66): Moderately attuned  
  \- High (67-100): Highly empathetic, resonant

\*\*Cognitive Energy Index (0-100)\*\*:  
\- \*\*Definition\*\*: Activation and momentum; tonal pacing, rhythm, and emphasis patterns signaling cognitive load or intent  
\- \*\*Perceptual Indicators\*\*: Speech rate, articulation precision, dynamic energy, mental engagement  
\- \*\*Interpretation\*\*:  
  \- Low (0-33): Low engagement, slow pacing  
  \- Moderate (34-66): Moderate processing  
  \- High (67-100): High mental energy, dynamic  
\- \*\*Known Issue\*\*: Shows systematic elevation (\~90-100) across most utterances, possibly due to speaker's natural "AI-adjacent" prosodic style. Intentionally retained for transparency.

\*\*Attention Index (0-100)\*\*:  
\- \*\*Definition\*\*: How effectively tonality orients focus, directs perceptual priority, and maintains engagement  
\- \*\*Perceptual Indicators\*\*: Clarity, emphasis patterns, salience markers, commanding quality  
\- \*\*Interpretation\*\*:  
  \- Low (0-33): Unfocused, diffuse  
  \- Moderate (34-66): Moderately engaging  
  \- High (67-100): Highly focused, attention-commanding

\*\*Scoring Notes\*\*:  
\- All scores reflect practitioner's expert perceptual assessment  
\- Scores informed by 8,873+ customer interactions where similar patterns correlated with measurable outcomes  
\- Not algorithmically derived; represent human expert judgment  
\- Continuous 0-100 scale enables gradient analysis beyond categorical classification

\---

\#\#\# Ambivalence Annotation

Most prosody and emotion recognition datasets treat mixed or contradictory tonal signals as \*\*annotation errors\*\* or \*\*noise to be eliminated\*\*. TonalityPrint takes the opposite approach: \*\*ambivalence is systematically annotated as a feature, not a bug\*\*.

This represents a fundamental shift in how vocal tonality complexity is captured and understood in voice AI. Real-world communication frequently involves simultaneous, competing tonal intentions \-  e.g., warmth mixed with caution, confidence mixed with uncertainty, engagement mixed with reservation. By explicitly and systematically marking and preserving these ambivalent states, TonalityPrint potentially provides researchers with the substrate to study tonal complexity as it naturally occurs.

\#\#\#\# What is Ambivalence in the TonalityPrint Framework?

\*\*Definition\*\*:  
Tonalityprint proposes to define Ambivalence as occurring when \*\*two or more contradictory or competing tonal sub-modifier layers are present almost simultaneously\*\* within a single utterance. These competing signals are expressed subtly and realistically through micro-mixed acoustic cues that create tonal complexity.

\*\*Key Characteristics\*\*:  
\- Not a binary "mixed emotion" but \*\*nuanced layering\*\* of competing prosodic signals  
\- Present at the sub-modifier level (e.g., warm \+ cautious, engaged \+ hesitant)  
\- Reflects \*\*authentic human communication\*\* where intentions are rarely pure or singular  
\- Occurs across all five primary tonal intents (Trust, Attention, Reciprocity, Empathy Resonance, Cognitive Energy)

\*\*Examples of Ambivalent Tonality\*\*:  
1\. \*\*Reciprocity \+ Engaged \+ Caution\*\*: Warm, invitational prosody with subtle markers of reservation or uncertainty  
2\. \*\*Trust \+ Confident \+ Doubt\*\*: Authoritative tone with micro-hesitations or slight pitch instability  
3\. \*\*Empathy Resonance \+ Warm \+ Concern\*\*: Emotionally attuned with underlying worry or apprehension  
4\. \*\*Attention \+ Focused \+ Reluctance\*\*: Clear, directed communication with subtle withdrawal cues  
5\. \*\*Cognitive Energy \+ Enthusiastic \+ Skeptical\*\*: High energy with questioning or disbelief undertones

\*\*Nuanced Cues Captured\*\*:  
Ambivalence annotation captures subtle acoustic markers including:  
\- Concern (empathetic worry layered into otherwise neutral delivery)  
\- Disbelief (skepticism mixed with engagement)  
\- Doubt (uncertainty within otherwise confident tonality)  
\- Hesitancy (pause or tempo markers within fluid speech)  
\- Regret (backward-looking tonality mixed with forward action)  
\- Reluctance (resistance cues within cooperative prosody)  
\- Worry (anticipatory concern within supportive tonality)

\#\#\#\# Ambivalence Detection Methodology  
\*\*How Ambivalence is Hypothetically Identified\*\*:

The practitioner (Ronda) identifies ambivalence through a combination of:

1\. \*\*Intentional Design\*\* (Pre-Recording):  
   \- Some utterances deliberately crafted to express ambivalent tonality  
   \- Complex utterances designed with: Primary Intent \+ Sub-modifier \+ Ambivalence layer  
   \- Example: "Trust \+ Calm \+ Ambivalence" requires delivering trustworthy, calm prosody with subtle competing uncertainty cues

2\. \*\*Real-Time Perceptual Assessment\*\* (During Recording):  
   \- Practitioner monitors for unintended competing tonal signals  
   \- Detects when acoustic delivery includes contradictory prosodic cues  
   \- Recognizes when utterance contains layered, mixed intentions

3\. \*\*Post-Recording Review\*\* (Annotation Phase):  
   \- Playback analysis identifies subtle competing signals  
   \- Practitioner evaluates whether mixed cues were intentional or artifacts  
   \- Decision made to mark as ambivalent vs. re-record

\*\*Decision Criteria for Ambivalence Marking\*\*:

An utterance receives the \`ambivalex\` marker when:  
\- Two or more competing sub-modifier cues are clearly present  
\- The mixed signals are subtle enough to be realistic (not exaggerated)  
\- The ambivalence serves a communicative purpose (not technical error)  
\- The acoustic profile contains identifiable markers of both/all competing intentions  
\- The practitioner can articulate which specific tonal layers are competing

An utterance is \*\*NOT\*\* marked as ambivalent when:  
\- Mixed signals are due to technical recording issues (mic artifacts, noise)  
\- Competing cues are so subtle they're indistinguishable from baseline  
\- The ambivalence is unintentional and not representative of target tonality  
\- Re-recording can produce clearer, less ambiguous version

\#\#\#\# Ambivalence Annotation Process

\*\*Step-by-Step Workflow\*\*:

1\. \*\*Utterance Design\*\* (for intentional ambivalence):  
   \- Identify target primary intention (e.g., Reciprocity)  
   \- Select primary sub-modifier (e.g., Engaged)  
   \- Add ambivalence layer (e.g., subtle caution/reservation markers)  
   \- Mental preparation: Hold both/all tonal intentions simultaneously during delivery

2\. \*\*Recording Execution\*\*:  
   \- Deliver utterance with intentional tonal layering  
   \- Maintain primary intention while introducing competing cues  
   \- Keep competing signals subtle and realistic (not theatrical)

3\. \*\*Immediate Review\*\*:  
   \- Playback immediately after recording  
   \- Assess: Are both/all intended tonal layers audibly present?  
   \- Assess: Does the ambivalence sound natural or forced?  
   \- Decision: Accept, re-record, or adjust ambivalence marker

4\. \*\*Annotation\*\*:  
   \- Primary\_Intention field: Dominant tonal intent (e.g., "Reciprocity")  
   \- Sub\_Modifier field: Primary sub-modifier (e.g., "enga" for Engaged)  
   \- \*\*Ambivalex field\*\*: Marked as "ambivalex" if competing layers present  
   \- Notes field: Document which specific competing cues are present

5\. \*\*File Naming\*\*:  
   \- Complex utterances with ambivalence receive \`ambivalex\` marker in filename  
   \- Example: \`TPV1\_B1\_UTT1\_S\_Reci\_enga\_ambivalex\_SP-Ronda.wav\`  
   \- This enables easy filtering and analysis of ambivalent samples

\*\*Validation in Quality Control Process\*\*:

During the proprietary heuristic audit (\~18.05% of corpus re-recorded):

\- \*\*Ambivalent samples received special scrutiny\*\*: Audit verified that acoustic features contained identifiable markers of competing tonal cues  
\- \*\*Divergences sometimes indicated successful ambivalence\*\*: When acoustic profile showed "mixed signals," this was often correct annotation of ambivalence rather than error  
\- \*\*Strategic retention\*\*: Some samples flagged as "divergent" were retained specifically because the acoustic-intent mismatch represented genuine ambivalent tonality  
\- \*\*Documentation\*\*: All ambivalent samples have detailed notes explaining which competing cues are present

This means ambivalence survived the QC process when:  
1\. Competing acoustic cues were clearly detectable  
2\. Mixed signals were subtle enough to be realistic  
3\. Ambivalence served communicative/research purpose  
4\. Practitioner could articulate the specific tonal layers

\#\#\#\# Prevalence and Distribution

\*\*Dataset Statistics\*\* (estimated from corpus structure):  
\- Ambivalent samples represent a \*\*minority class\*\* in the dataset  
\- Each batch (18 utterances) includes select ambivalent samples  
\- Not all primary intentions or sub-modifiers include ambivalent versions  
\- Strategic sampling: Ambivalence captured where most relevant/realistic

\*\*File Naming Pattern\*\*:  
\- Single: \`TPV1\_B1\_UTT1\_S\_Att\_SP-Ronda.wav\` (Primary only)  
\- Compound: \`TPV1\_B1\_UTT1\_S\_Reci\_affi\_SP-Ronda.wav\` (Primary \+ Sub-modifier)  
\- \*\*Complex (Ambivalent)\*\*: \`TPV1\_B1\_UTT1\_S\_Reci\_affi\_ambivalex\_SP-Ronda.wav\` (Primary \+ Sub-modifier \+ Ambivalence)

\#\#\#\# Why This Matters Now

\*\*Competitive Advantage\*\*:

2\. \*\*Ecologically Valid\*\*: Reflects real-world communication where pure emotional/tonal states are rare  
3\. \*\*Research Enabler\*\*: Aims to support new research directions in tonal complexity  
4\. \*\*AI Alignment\*\*: Potentially necessary for fine-tuning AI systems to recognize human communication complexity for better trust, attunement and reciprocity.  
5\. \*\*Commercial Value\*\*: Potential for high-stakes applications (e.g., customer service, healthcare, negotiation, autonomous systems) where detecting mixed signals is crucial

\*\*Contrast with Existing Datasets\*\*:

Most emotion/prosody datasets:  
\- Treat ambiguity as annotation disagreement (noise)  
\- Force annotators to choose single dominant emotion  
\- Discard samples with mixed signals  
\- Aim for high inter-rater agreement (which requires ignoring complexity)

TonalityPrint:  
\- Treats ambivalence as signal (feature)  
\- Explicitly marks competing tonal layers  
\- Aims to preserve samples with intentional mixed signals  
\- Single expert annotator can capture nuance that multi-rater consensus would average out

\*\*Research Applications Potentially Enabled by Functional Tonal Intent and Ambivalence Annotation\*\*:

1\. \*\*Ambivalence Detection Models\*\*: precision-tuning classifiers to identify mixed/transitional tonal states  
2\. \*\*Tonal Complexity Analysis\*\*: Study how competing prosodic signals interact acoustically  
3\. \*\*Real-World Tonality Modeling\*\*: Move beyond pure categorical states to realistic mixed intentions  
4\. \*\*Inference-Time Adaptation\*\*: Enable AI systems to recognize and respond appropriately to ambivalent human communication  
5\. \*\*Emotional Granularity\*\*: Investigate fine-grained affective states beyond basic emotion categories  
6\. \*\*Trust & Safety\*\*: Detect uncertainty or hesitation in otherwise confident-sounding speech (e.g., hallucination detection, safety-critical systems,“Soft refusals”)  
7\. \*\*Human-Robot Interaction\*\*: Enable social robots to recognize and navigate complex human tonal states  
8\. \*\*Clinical Applications\*\*: Study ambivalence in therapeutic contexts (e.g., motivational interviewing, trauma recovery)

\*\*Empirical Grounding\*\*:

The ambivalence annotation methodology is grounded in Ronda's observation of \*\*8,873+ real-world customer interactions\*\* where:  
\- Mixed tonal signals frequently occurred in high-stakes conversations  
\- Ambivalent tonality potentially correlated with specific conversational outcomes  
\- Customers may have responded differently to pure vs. ambivalent tonal states  
\- The ability to navigate tonal complexity may have been associated with successful interactions

This real-world foundation motivated annotating ambivalence to possibly reflect \*\*authentic communication patterns\*\*, not artificial laboratory constructs.

\---

\#\#\#\#  Segment-Level Temporal Analysis

Each utterance includes time-aligned segment data with millisecond precision:  
\- \*\*Segment Definition\*\*: Typically whole utterance as single segment (most files)  
\- \*\*Temporal Boundaries\*\*: Start and end times recorded in milliseconds  
\- \*\*Per-Segment Scoring\*\*: All five tonality indices scored for each segment  
\- \*\*Data Structure\*\*: Stored as JSON array with startTime, endTime, and five index scores  
\- \*\*Precision\*\*: Millisecond-level timestamps enable fine-grained temporal analysis  
\- \*\*Purpose\*\*: Supports investigation of tonality dynamics within utterances

\*\*Example Segment Data\*\*:  
\`\`\`json  
\[{  
  "startTime": 0,  
  "endTime": 4284.083333333333,  
  "trust": 75,  
  "reciprocity": 93,  
  "empathy": 76,  
  "cognitive": 96,  
  "attention": 80  
}\]  
\`\`\`

\#\#\#\#  Metadata Recording

For each utterance, the following metadata is captured:  
\- Utterance text (transcription)  
\- Utterance type (Statement/Question)  
\- Primary intention category  
\- Sub-modifier (if applicable)  
\- Ambivalence marker (if applicable)  
\- Temporal data (start, end, duration)  
\- Recording date and processing timestamp  
\- Annotator notes

\---

\#\#\#\# .Validation Procedures

\#\#\#\# 1\. Proprietary Heuristic Audit (Primary QC)

\*\*Blind Acoustic Validation\*\*:  
After initial annotation, all 144 samples underwent blind, proprietary heuristic audit:  
\- Acoustic profiles analyzed without access to practitioner labels  
\- Script evaluated spectral variance (pitch contour, energy dynamics, etc.)  
\- Samples flagged when acoustic features diverged from stated intention labels

\*\*Audit Results\*\*:  
\- \*\*\~80+% alignment rate\*\*: Acoustic profiles matched intended tonal intent categories  
\- \*\*\~18.05% re-recorded\*\*: Samples with acoustic-intent divergence were re-recorded for consistency  
\- \*\*Cross-intent patterns detected\*\*: Cognitive Energy systematically elevated across corpus

\*\*Resolution Process\*\*:  
\- Flagged samples reviewed by practitioner  
\- If acoustic profile didn't support intended tonality → utterance re-recorded  
\- Some divergences retained as genuine ambivalence or tonal complexity  
\- All decisions documented in Notes field

\#\#\#\# 2\. Cross-Batch Consistency Checks  
\- \*\*Similar Intentions\*\*: Compared across batches to ensure temporal stability  
\- \*\*Baseline Stability\*\*: Neutral samples verified for consistent reference point  
\- \*\*Index Relationships\*\*: Internal consistency of tonality indices reviewed  
\- \*\*Pattern Recognition\*\*: Systematic patterns (e.g., CE elevation) identified and documented

\#\#\#\# 3\. Technical Validation

\- \*\*Audio Integrity\*\*: All WAV files checked for corruption or artifacts  
\- \*\*Metadata Completeness\*\*: Verified all 23 variables present and valid  
\- \*\*File Naming\*\*: 100% compliance with systematic convention  
\- \*\*Temporal Alignment\*\*: Segment timestamps validated against audio duration  
\- \*\*JSON Structure\*\*: Segment data verified for correct format and values  
\---  
\#\# Data Processing Pipeline

\#\#\# 1\. Recording Phase  
\`\`\`  
Speaker Preparation → Audio Recording (48kHz WAV) → Quality Check → File Naming → Storage  
\`\`\`

\#\#\# 2\. Annotation Phase  
\`\`\`  
Audio Analysis → Tonality Scoring → Segment Analysis → Metadata Entry → Quality Review  
\`\`\`

\#\#\# 3\. Export Phase  
\`\`\`  
JSON Generation → CSV Conversion → Combined Dataset Creation → Documentation → Packaging  
\`\`\`  
\---

\#\# Potential Reproducibility

\#\#\# Materials Provided  
\- Complete audio recordings (WAV format)  
\- Full annotation data (JSON and CSV formats)  
\- Comprehensive codebook  
\- Detailed methodology documentation  
\- File naming conventions  
\- Version control information

\#\#\# Replication Guidelines

To attempt to replicate this annotation approach:  
1\. Review the full TonalityPrint README on Zenodo  
2\. Fine-tune annotators in tonality perception and measurement  
3\. Use consistent recording equipment and environment  
4\. Follow the acoustic analysis protocols described above  
5\. Implement systematic quality control procedures

\---

## **Ethical Framework**

* **Speaker Consent:** 100% of recordings are of the author (R. Polhill) with explicit informed consent for research use.  
* **Biometric Integrity:** No synthetic voices, clones, or generative AI audio were used. The dataset is 100% human.  
* **Deepfake Restriction:** Researchers are strictly prohibited from using this dataset to create unauthorized voice clones or deepfakes of the speaker.

## **Limitations and Considerations**

* **Single-Speaker:** While purposely controlled and specialized, results may not generalize across genders, accents, or cultures without further validation.  
* **Observational Origin:** The correlation with conversion outcomes is observational and outcome-associated, not a controlled causal experiment.  
* **Subjectivity:** Annotation relies on practitioner judgment and self-correction, which entails inherent subjective bias.

**Measurement Limitations:**  
**Subjective Elements:** Tonality scoring includes perceptual assessment by expert annotator  
**Cognitive Energy Bias**: Systematic elevation documented and retained  
**Ambivalence Complexity**: Mixed-tonality utterances may require specialized analysis

**Quality Control and Systematic Bias Monitoring**  
Known Issue \- Cognitive Energy Index:  
The expert annotator identified systematic elevation in Cognitive Energy scores across the dataset. This pattern was attributed to:  
\- Speaker's natural ecological style  
\- Lexical content choices  
\- Potential annotator perceptual bias  
**\-Decision:** These elevated scores were intentionally retained for transparency rather than artificially adjusted.  
\-**Documentation:** Individual notes field contains explanation for affected utterances.

## **For additional questions about methodology, annotation procedures, or data collection, please :**

\- See CODEBOOK.md for variable definitions  
\- See README.md for dataset overview  
\- Contact researcher for methodological inquiries  
\-See detailed README available  here on Zenodo https://doi.org/10.5281/zenodo.17913895

Version: 1.0  
Last Updated: January 24, 2026

