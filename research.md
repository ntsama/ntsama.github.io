---
layout: page
title: "Research — Language, Thought & AI"
permalink: /research/
lang: en
description: "Research program of Jean Marie Ntsama — language–thought dynamics, AI-augmented learning, digital literacies, and computational modeling."
---

<div style="text-align:right; font-size:0.9rem; margin-bottom:15px;">
  🌐 <a href="/fr/research/" style="font-weight:bold;">FR</a>
</div>

# Research  
## Scientific Program & Research Vision  

My research investigates how **language and thought co‑evolve** in technologically mediated environments.  
I work at the intersection of philosophy of language, cognitive science, linguistics, AI‑augmented learning, and digital literacies.

My long‑term goal is to develop a **unified cognitive framework** for understanding human learning in the age of AI.

---

# 1. Research Vision  
My work is guided by a central question:  
**How do language and thought co‑develop when learners interact with AI‑mediated environments?**

To answer this, I combine:  
- conceptual analysis  
- cognitive and linguistic experiments  
- computational modeling  
- AI‑supported learning environments  
- multilingual and intercultural perspectives  

---

# 2. Main Research Axes  

### Axis 1 — Language–Thought Dynamics  
Exploring the cognitive mechanisms linking linguistic structures and conceptual representations.  
This includes:  
- semantic and conceptual modeling  
- cross‑linguistic cognition  
- neurodiversity and cognitive variability  

### Axis 2 — AI‑Augmented Learning  
Studying how AI tools reshape learning processes.  
Focus areas:  
- multimodal explanations  
- adaptive feedback  
- cognitive scaffolding  
- AI as a cognitive partner  

#### AI-Powered Reading Companion for ZEP
In collaboration with the **IA4ZEP** program, I am designing a mobile application that uses **Automatic Speech Recognition (ASR)** and **Large Language Models (LLM)** to support guided reading sessions in priority education zones.

The application strictly follows the **official 5-step guided reading methodology** (situation, reading, grid, confrontation, synthesis) prescribed by the Cameroonian curriculum for 6th grade French classes. It provides:
- Real-time pronunciation feedback (phonetic accuracy, fluency, prosody).
- Semantic comprehension checks (literal and inferential questions).
- A performance dashboard with a **90% mastery threshold**, ensuring learners achieve proficiency before progressing.

This tool bridges the gap between **linguistic decoding** and **deep semantic comprehension**, directly validating the **Cognitive Trapeze Model** and aligning with national educational priorities.
#### ASR Classification: A Window into Neurodiversity
A comprehensive ASR evaluation across 13+ texts and 26 learners in a ZEP classroom revealed a striking pattern: 4 learners (15.4% of the sample) exhibited acoustic and attentional signatures consistent with neurodivergent profiles (dyspraxia, dysarthria, ADHD spectrum). Using Whisper Tiny, Medium, and Large as diagnostic proxies, we applied four evidence‑based criteria:

- **Criterion 1 – Persistent Tiny Hallucination:** Mean WER > 90% across multiple texts, indicating systematic failure of the small model to encode phonetic information.
- **Criterion 2 – Multiple Hallucination Cascades:** WER > 100% on Tiny for at least two texts, reflecting uncontrolled generative drift.
- **Criterion 3 – Extreme Large‑Model Volatility:** Large WER exceeding 100%, revealing signal pathology beyond normal variance.
- **Criterion 4 – High Standard Deviation of Large WER:** σ > 40 percentage points across texts, indicating state‑dependent processing (fatigue, attention fluctuations).

These patterns are not errors—they are acoustic signatures of neurodevelopmental differences. The remaining 22 learners (84.6%) showed typical progression curves aligned with grade level and reading confidence.

**Pedagogical implications for Cognitive Trapeze:**
- **Individualized audio preprocessing:** Spectral smoothing and timing regularization for flagged learners.
- **Dynamic model selection:** Confidence‑gated fallback to Medium when Large is unstable.
- **Semantic verification as a safety layer:** Essential to correct hallucination‑corrupted output.
- **State‑dependent mastery thresholds:** Reduced target accuracy (70%) and shorter session limits (5‑10 min) for learners showing attentional fragmentation.

These findings validate the dual‑layer ASR+LLM architecture and confirm that Cognitive Trapeze’s adaptive design is not an optimization—it is a necessity for inclusive, neurodiversity‑aware pedagogy.

### Axis 3 — Digital Literacies in African Contexts  
Investigating how learners in African contexts engage with digital tools.  
Includes:  
- multilingual digital practices  
- inclusive learning environments  
- educational innovation in priority zones  

### Axis 4 — Computational Modeling of Cognition  
Developing computational simulations to model:  
- language–thought co‑development  
- learning trajectories  
- agent‑based cognitive dynamics  

---

# 3. Research Methods  
My work combines:  
- conceptual analysis  
- cognitive and linguistic experiments  
- computational modeling  
- AI‑mediated learning environments  
- mixed‑methods approaches  

This methodological diversity bridges **theory, empirical data, and computational simulation**.

---

# 4. Europe–Africa Research Strategy  
Based in Ngaoundéré (Cameroon) and collaborating across Europe and Africa, my research builds bridges between:  
- cognitive science  
- digital education  
- multilingual learning  
- AI‑supported pedagogy  

This strategy strengthens both scientific and societal impact.

---

# 5. Alignment with My MSCA Project  
My MSCA project **Cognitive Trapeze** integrates all four research axes.  
It provides a coherent framework for:  
- theoretical modeling  
- empirical studies  
- computational simulation  
- educational innovation  

---

## Research Hypotheses

The project is built on four core hypotheses aligned with the work packages and empirical predictions:

- **H1 (Predictive validity):** The three feedback loops of the Cognitive Trapeze model can be formalized as conditional probability distributions within a Bayesian network, and the resulting model will predict reading comprehension scores with **≥ 70% accuracy**.
- **H2 (Clinical sensitivity):** Learners using the AI tutor will show significantly greater improvement in semantic comprehension (**effect size d ≥ 0.5**) compared to the control group, moderated by neurodiversity status (dyslexia, language disorders).
- **H3 (Technical robustness):** The quantized **Whisper Large** combined with the **Qwen 0.5B** semantic LLM will achieve a Word Error Rate (WER) **below 15%** on low-end Android devices (3GB RAM) in 100% offline conditions.
- **H4 (Scalability):** The prototype functions with **> 80% fidelity** in low-bandwidth settings (< 2 Mbps) and offline mode, and can be successfully deployed in real school environments across diverse contexts.

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
