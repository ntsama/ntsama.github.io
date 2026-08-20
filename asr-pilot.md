---
layout: page
title: "ASR Pilot & WER Analysis — Text 1"
permalink: /asr-pilot/
lang: en
description: "Preliminary ASR pilot study results for Cognitive Trapeze, comparing Whisper Tiny, Medium, and Large in a ZEP classroom in Cameroon."
---

<div style="text-align:right; font-size:0.9rem; margin-bottom:15px;">
  🌐 <a href="/fr/asr-pilot/" style="font-weight:bold;">FR</a>
</div>

# ASR Pilot & WER Analysis — Text 1  
## Which ASR Engine Can Cognitive Trapeze Rely On?

---

### 1. The Experiment
As part of the Cognitive Trapeze project, a pilot voice data collection was conducted in a real ZEP (Priority Education Zone) classroom in Cameroon. Four anonymized learners were recorded reading **Text 1** (82 words) under natural classroom noise conditions.

The objective was to evaluate the robustness of three Whisper model variants (**Tiny**, **Medium**, **Large**) to select the embedded ASR engine for our offline mobile application (constrained by 3 GB RAM).

### 2. Word Error Rate (WER) Results – Text 1
The graph below shows the Word Error Rate (WER) for each learner and each model. The red dashed line indicates a critical threshold of 40% errors.

![WER Chart for Text 1](/assets/img/wer_chart_text1.png)

**Key Takeaways from the data:**
- **Whisper Large** beats every model under normal reading conditions — up to **17x more accurate** than Tiny (Learner 1: 1.3% vs 50.6%).
- **Whisper Tiny** is unusable in a real classroom: hallucinations push the WER above 50–140% even for calm readers.
- When a learner reads too fast or chops words (Learners 3–4), **every model degrades** — the bottleneck is **signal quality**, not the model choice.

### 3. Recommendations for the App
Based on this pilot, we have adopted the following technical decisions:
- **✅ Adopt a quantized Whisper Large** (int8 / float16) — it fits the 3 GB RAM and offline constraint.
- **✅ Add audio pre‑processing:** noise filtering + volume normalization before ASR.
- **✅ Coach learners toward calm, paced reading** during sessions.
- **✅ Consider a directional external mic** if budget allows.

---

### 4. Application UX Wireframes (Classroom Flow)
The wireframes below illustrate the 4‑step user flow designed for the MVP: **Student Selection → Guided Reading Interface → Multimodal Feedback (visual, auditory, haptic) → Teacher Dashboard.**

![UX Wireframes for Cognitive Trapeze](/assets/img/ux_wireframe_en.png)

**Core UX features:**
- **Large‑print text** (>80% of screen) to guide the learner's focus.
- **Live word highlighting** (yellow) to monitor reading pace.
- **Real‑time feedback** on misread words (red highlight + haptic vibration for rhythm).
- **Aggregated teacher dashboard** displaying the performance of the last 5 students to quickly spot recurrent errors.

---

### 5. Classification Insights: Neurodiversity Signatures from ASR Performance

Beyond evaluating ASR engines, the collected data allowed us to develop an evidence‑based classification framework to detect potential neurodivergent profiles using WER patterns. Across 13+ texts and 26 learners, we identified **4 learners (15.4%)** exhibiting hallmark characteristics of neurodevelopmental differences (dyspraxia, dysarthria, ADHD spectrum). The classification criteria are:

- **Persistent Tiny Hallucination (Mean WER > 90%):** Systematic failure of the smallest model to encode phonetic information.
- **Multiple Hallucination Cascades (WER > 100% on Tiny for ≥2 texts):** Uncontrolled generative drift triggered by acoustic ambiguities.
- **Extreme Large‑Model Volatility (Max Large WER > 100%):** Breakdown of Large’s mitigation capacity, indicating signal pathology.
- **High Standard Deviation of Large WER (σ > 40 pp):** State‑dependent processing instability.

These 4 learners show acoustic and attentional patterns that standard reading assessments miss, but that ASR systems reveal with precision. This finding validates the dual‑layer ASR+LLM architecture (TDR v2) as essential for neurodiverse learners, because it can adapt audio preprocessing, dynamically switch models, and apply state‑dependent mastery thresholds.

---

### 6. Next Steps
This pilot validates our architectural choices and provides a concrete neurodiversity‑sensitive methodology. We are now:
- Preparing the data collection for **Text 2** with refined audio preprocessing.
- Designing individualized acoustic profiles for the 4 flagged learners.
- Finalizing the preprint with Prof. Worsley (co‑signed).
- A consolidated report and a scientific article will follow the analysis of the full corpus.
---

<hr style="margin-top:40px;">

<div style="text-align:center; font-size:0.85rem; opacity:0.85;">
  <a href="/about/">About</a> •
  <a href="/theory/">Theory</a> •
  <a href="/research/">Research</a> •
  <a href="/msca/">MSCA</a> •
  <a href="/ia4zep/">IA_4_ZEP</a> •
  <a href="/faq/">FAQ</a>
</div>
