---
layout: page
title: "Expérimentation ASR et analyse WER — Texte 1"
permalink: /fr/asr-pilot/
lang: fr
description: "Résultats de l'étude pilote ASR pour Cognitive Trapeze, comparant Whisper Tiny, Medium et Large en classe ZEP au Cameroun."
---

<div style="text-align:right; font-size:0.9rem; margin-bottom:15px;">
  🌐 <a href="/asr-pilot/" style="font-weight:bold;">EN</a>
</div>

# Expérimentation ASR et analyse WER — Texte 1  
## Quel moteur ASR peut équiper Cognitive Trapeze ?

---

### 1. L'expérimentation
Dans le cadre du projet Cognitive Trapeze, une collecte de données vocales pilote a été menée dans une classe réelle en Zone d'Éducation Prioritaire (ZEP) au Cameroun. Quatre apprenants anonymisés ont été enregistrés en train de lire le **Texte 1** (82 mots) dans des conditions de bruit ambiant naturel.

L'objectif était d'évaluer la robustesse de trois variantes du modèle Whisper (**Tiny**, **Medium**, **Large**) pour sélectionner le moteur ASR embarqué de notre application mobile offline (contrainte par 3 Go de RAM).

### 2. Résultats du taux d'erreur de mots (WER) – Texte 1
Le graphique ci-dessous présente le taux d'erreur (WER) pour chaque élève et chaque modèle. La ligne rouge en pointillés indique un seuil critique de 40 % d'erreurs.

![Graphique WER pour le Texte 1](/assets/img/wer_chart_text1.png)

**Enseignements clés des données :**
- **Whisper Large** surpasse tous les modèles en conditions de lecture normales — jusqu'à **17 fois plus précis** que Tiny (Élève 1 : 1,3 % contre 50,6 %).
- **Whisper Tiny** est inutilisable en classe réelle : les hallucinations sémantiques poussent le WER au-delà de 50–140 %, même pour des lecteurs calmes.
- Lorsqu'un apprenant lit trop vite ou hache les mots (Élèves 3 et 4), **tous les modèles se dégradent** — le goulot d'étranglement est la **qualité du signal**, et non le choix du modèle.

### 3. Recommandations pour l'application
Sur la base de ce pilote, nous avons adopté les décisions techniques suivantes :
- **✅ Utiliser une version quantifiée de Whisper Large** (int8 / float16) — compatible avec la contrainte 3 Go RAM et le mode offline.
- **✅ Ajouter un pré‑traitement audio :** filtrage du bruit et normalisation du volume avant l'ASR.
- **✅ Entraîner les élèves à une lecture posée et calme** pendant les séances.
- **✅ Envisager un microphone externe directionnel** si le budget le permet.

---

### 4. Wireframes UX de l'application (Flux en classe)
Les maquettes ci-dessous illustrent le flux utilisateur en 4 étapes conçu pour le MVP : **Sélection de l'élève → Interface de lecture → Feedback multimodal (visuel, auditif, haptique) → Tableau de bord enseignant.**

![Wireframes UX pour Cognitive Trapeze](/assets/img/ux_wireframe_fr.png)

**Fonctionnalités UX clés :**
- **Texte en grands caractères** (>80 % de l'écran) pour guider la focalisation de l'apprenant.
- **Surlignage en temps réel** (jaune) pour visualiser le rythme de lecture.
- **Feedback instantané** sur les erreurs (surlignage rouge + vibration haptique pour le rythme).
- **Tableau de bord enseignant** avec vue agrégée des 5 derniers élèves pour repérer rapidement les erreurs récurrentes.

---

### 5. Prochaines étapes
Ce pilote valide nos choix d'architecture. Nous préparons actuellement la collecte de données pour le **Texte 2** et l'affinement de la chaîne de pré‑traitement audio. Un rapport consolidé et un article scientifique, co‑signé avec le Professeur Marcelo Worsley, suivront l'analyse de l'ensemble du corpus.

---

<hr style="margin-top:40px;">

<div style="text-align:center; font-size:0.85rem; opacity:0.85;">
  <a href="/fr/about/">À propos</a> •
  <a href="/fr/theory/">Théorie</a> •
  <a href="/fr/research/">Recherche</a> •
  <a href="/fr/msca/">MSCA</a> •
  <a href="/fr/ia4zep/">IA_4_ZEP</a> •
  <a href="/fr/faq/">FAQ</a>
</div>
