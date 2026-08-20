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

### 5. Résultats de classification : signatures de la neurodiversité à partir des performances ASR

Au‑delà de l’évaluation des moteurs ASR, les données collectées nous ont permis de développer un cadre de classification fondé sur des preuves pour détecter d’éventuels profils neurodivergents à partir des schémas de WER. Sur plus de 13 textes et 26 apprenants, nous avons identifié **4 apprenants (15,4 %)** présentant des caractéristiques de différences neurodéveloppementales (dyspraxie, dysarthrie, spectre TDAH). Les critères de classification sont :

- **Hallucination persistante de Tiny (WER moyen > 90 %) :** défaillance systématique du petit modèle à encoder l’information phonétique.
- **Cascades d’hallucinations multiples (WER > 100 % sur Tiny pour ≥2 textes) :** dérive générative incontrôlée déclenchée par des ambiguïtés acoustiques.
- **Volatilité extrême du modèle Large (WER maximal > 100 %) :** effondrement de la capacité d’atténuation de Large, indiquant une pathologie du signal.
- **Écart‑type élevé du WER de Large (σ > 40 pp) :** instabilité du traitement dépendant de l’état.

Ces 4 apprenants présentent des schémas acoustiques et attentionnels que les évaluations de lecture standard ne détectent pas, mais que les systèmes ASR révèlent avec précision. Cette découverte valide l’architecture à double couche ASR+LLM (TDR v2) comme essentielle pour les apprenants neurodivers, car elle peut adapter le prétraitement audio, changer dynamiquement de modèle et appliquer des seuils de maîtrise dépendants de l’état.

### Analyse visuelle : les quatre cas neurodivers

Le cadre de classification a identifié quatre apprenants dont les schémas de performance ASR sont fortement corrélés à des profils neurodivergents. Le graphique ci-dessous visualise leur taux d'erreur de mots (WER) sur les trois modèles Whisper (Tiny, Medium et Large).

![Graphique de classification neurodivers](/assets/img/neurodiverse_classification_graph.png)

**Récapitulatif des quatre apprenants identifiés :**

- **Élève 03 – Soupçon de dysarthrie ou trouble moteur de la parole :** Caractérisé par un Tiny WER persistant > 90 % (5/7 textes), un effondrement catastrophique du Large WER (141,5 %) et une forte volatilité (\(\sigma\) = 51,3 pp). Le signal acoustique peine à être encodé, y compris par le modèle Large.
- **Élève 06 – Soupçon de TDAH ou dérégulation :** Montre un ratio Medium/Large erratique et un effondrement extrême du Large (94,4 %). La performance varie fortement, indiquant un traitement dépendant de l'état plutôt qu'une limite de capacité fixe.
- **Élève 22 – Soupçon de dyspraxie ou trouble du contrôle moteur :** Présente une performance Tiny extrême (WER > 100 % sur 3/3 textes) dominée par des hallucinations. Bien que le Large WER soit modéré (79,6 %), la pathologie acoustique est constamment présente sur tous les modèles.
- **Élève 23 – Soupçon de dyspraxie ou dysarthrie :** Démontre un Tiny WER persistant > 100 % (sur 4 textes) avec des déclenchements d'hallucinations stables. Large WER modéré (50 %) mais forte volatilité (\(\sigma\) = 24,6 pp) suggérant une fragmentation attentionnelle et des effets de fatigue.

**Enseignement pédagogique :** Ces quatre apprenants ne sont pas en « échec » face à l'ASR ; leur diversité acoustique et attentionnelle nécessite précisément l'architecture adaptative du Trapèze Cognitif (double couche ASR+LLM, prétraitement adaptatif, seuils dépendants de l'état) pour fournir un feedback pédagogique fiable et inclusif.
---

### 6. Prochaines étapes
Ce pilote valide nos choix d’architecture et fournit une méthodologie concrète sensible à la neurodiversité. Nous préparons actuellement :
- La collecte de données pour le **Texte 2** avec un prétraitement audio affiné.
- La conception de profils acoustiques individualisés pour les 4 apprenants identifiés.
- La finalisation du preprint avec le Prof. Worsley (co‑signé).
- Un rapport consolidé et un article scientifique suivront l’analyse de l’ensemble du corpus.
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
