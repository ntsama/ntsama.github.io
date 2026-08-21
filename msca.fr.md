---
layout: page
title: "Projet MSCA — Trapèze Cognitif"
permalink: /fr/msca/
lang: fr
description: "Projet MSCA — Trapèze Cognitif : modélisation computationnelle de la dynamique langage-pensée dans l'apprentissage augmenté par l'IA."
---

<div style="text-align:right; font-size:0.9rem; margin-bottom:15px;">
  🌐 <a href="/msca/" style="font-weight:bold;">EN</a>
</div>

# Projet MSCA  
## Trapèze Cognitif : Modélisation computationnelle de la dynamique langage–pensée dans l'apprentissage augmenté par l'IA  
*Une approche computationnelle de l’acquisition de la littératie chez les apprenants typiques et neurodivers*

---

# Résumé Exécutif  
Le projet **Trapèze Cognitif** étudie comment le **langage et la pensée se développent conjointement** dans des environnements d'apprentissage augmentés par l'IA.  
Le projet intègre l'analyse conceptuelle, l'expérimentation cognitive, les données multilingues et la modélisation computationnelle pour comprendre comment les apprenants naviguent entre les structures linguistiques, les représentations cognitives et la médiation technologique.

---

## Preuve de concept technique – Résultats ASR sur plus de 60 élèves en ZEP

Pour valider le choix de notre moteur de reconnaissance vocale (ASR), nous avons mené une campagne d'évaluation comparative en conditions réelles de classe dans les ZEP de l'Adamaoua. Plus de **60 apprenants** ont été testés sur **18 textes du corpus**, en comparant les modèles Whisper (Tiny, Medium, Large).

Les résultats sont sans équivoque :

| Texte | Niveau | Whisper Tiny | Whisper Medium | Whisper Large |
| :--- | :--- | :--- | :--- | :--- |
| **Texte 1** | 6ème | 50,6 % | 23,4 % | **1,3 %** |
| **Texte 2** | CE1 | 75,5 % | 29,6 % | **24,5 %** |
| **Texte 3** | CE2/CM1 | 97,4 % | 32,9 % | **23,1 %** |
| **Texte 4** | CE2 | 83,8 % | 31,5 % | **25,7 %** |
| **Texte 5** | CM1/CM2 | 78,0 % | 24,4 % | **14,9 %** |
| **Texte 7** | CM2/6ème | 75,5 % | 12,9 % | **14,8 %** |

*(Les WER affichés sont des moyennes pour les modèles Whisper. Large est le plus fiable, avec une précision remarquable dans les conditions les plus difficiles).*

<div style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: center;">
  <img src="/assets/images/synthese_texte1.png" alt="Résultats ASR Texte 1" style="max-width: 100%; height: auto; width: 400px; border: 1px solid #ddd; border-radius: 8px;">
  <img src="/assets/images/synthese_texte2.png" alt="Résultats ASR Texte 2" style="max-width: 100%; height: auto; width: 400px; border: 1px solid #ddd; border-radius: 8px;">
  <img src="/assets/images/synthese_texte3.png" alt="Résultats ASR Texte 3" style="max-width: 100%; height: auto; width: 400px; border: 1px solid #ddd; border-radius: 8px;">
  <img src="/assets/images/synthese_texte4.png" alt="Résultats ASR Texte 4" style="max-width: 100%; height: auto; width: 400px; border: 1px solid #ddd; border-radius: 8px;">
  <img src="/assets/images/synthese_texte5.png" alt="Résultats ASR Texte 5" style="max-width: 100%; height: auto; width: 400px; border: 1px solid #ddd; border-radius: 8px;">
  <img src="/assets/images/synthese_texte7.png" alt="Résultats ASR Texte 7" style="max-width: 100%; height: auto; width: 400px; border: 1px solid #ddd; border-radius: 8px;">
</div>

### 🔴 Le défi critique : les hallucinations sémantiques

Malgré l'excellente performance de **Whisper Large**, l'analyse qualitative révèle un problème fondamental pour un usage pédagogique : **les hallucinations sémantiques**. Le modèle transcrit correctement les sons, mais inverse le sens de la phrase ou change le temps verbal.

**Exemples réels observés sur nos élèves :**
- *"La maman prépare le repas"* → **"La maman ne fait pas le repas"** *(Négation intruse)*
- *"Je regarde par la fenêtre"* → **"Je ne regarde pas la fenêtre"** *(Inversion de sens)*
- *"Papa a acheté"* → **"Papa achetait"** *(Dérive temporelle)*

### ✅ La solution architecturale : une double couche ASR + LLM

Ces erreurs sémantiques sont invisibles pour un simple correcteur phonétique. Elles ne peuvent être détectées que par un **modèle de langage (LLM)** capable de comprendre le contexte.

C'est pourquoi le **TDR v2** de l'application Cognitive Trapeze intègre une **double couche obligatoire** :
1. **Moteur ASR (Whisper Large quantifié)** : pour le décodage phonétique.
2. **Moteur LLM (Qwen 0.5B ou Phi-3-mini)** : pour la vérification sémantique, la détection des inversions de sens et la correction des dérives temporelles avant transmission du feedback à l'élève.

**Cette architecture n'est pas une option : elle est la garantie d'un feedback pédagogique fiable.**

---

**Objectif pédagogique central :** Le projet cible spécifiquement la **lecture suivie** dans les zones d'éducation prioritaire (ZEP) du Cameroun. Il vise à démontrer comment les outils multimodaux assistés par l'IA aident les apprenants à combler le fossé entre le **décodage linguistique** et la **compréhension sémantique profonde**.

**Terrain empirique :** 4 écoles pilotes représentant les 4 types d'établissements du système éducatif camerounais (CES, CETIC, Lycée Général, Lycée Technique), soit environ **160 apprenants**. L'ensemble des activités de terrain est officiellement supervisé par la **Délégation Régionale du MINESEC (Adamaoua)** et ses Inspecteurs Régionaux (ICR) en Informatique et en Langues.

---

# État d'avancement du projet (Août 2026)

**✅ Institution hôte et superviseur principal confirmés :** Le projet est hébergé par l'**Université de Copenhague (UCPH), Danemark**, sous la supervision du **Professeur Daniel Spikol**. La **lettre officielle de soutien et de supervision** a été reçue et signée par le Professeur Spikol le 21 août 2026, confirmant son engagement total envers le projet et les missions de terrain prévues au Cameroun.

**✅ Co‑supervision et secondement confirmés :** Le Professeur **Marcelo Worsley** (Université Northwestern, États‑Unis) a officiellement accepté d'être co‑superviseur pour la partie computationnelle et le prototypage de l'IA, avec un **secondement de 6 mois (M10–M16)** au sein du *tiilt lab*.

**✅ Supervision terrain :** La **Délégation Régionale du MINESEC (Adamaoua)** et ses Inspecteurs Régionaux (ICR) superviseront officiellement toutes les activités de terrain. Le **Professeur Pius Ondoua** (Université de Yaoundé I) agit en tant que conseiller académique pour la cohérence philosophique du modèle.

**✅ Dossier final validé :** La proposition complète (Partie A, Partie B-1, Partie B-2) a été examinée et validée par le bureau de soutien à la recherche de l'UCPH et l'équipe de supervision. La soumission finale sur le portail EU Funding & Tenders est prévue avant la date limite du **9 septembre 2026**.

---

# PARTIE B1 — EXCELLENCE  

## 1. Titre du projet  
**Trapèze Cognitif :** Modélisation de la co‑évolution langage–pensée dans l’apprentissage augmenté par l’IA  
*Sous‑titre : Une approche computationnelle de l’acquisition de la littératie chez les apprenants typiques et neurodivers*

## 2. Résumé  
Ce projet explore comment le **langage et la pensée co-évoluent** au sein d'environnements d'apprentissage augmentés par l'IA.  
S'appuyant sur le *Modèle du Trapèze Cognitif* et sur l'expérience de terrain du programme **IA4ZEP** (supervisé par les ICR du MINESEC), il propose un cadre computationnel dynamique pour modéliser la manière dont les apprenants se déplacent entre les structures linguistiques, les représentations cognitives et la médiation technologique.

## 3. Objectifs  

### Objectifs scientifiques  
- Modéliser l'interaction dynamique entre le **langage, la pensée et la technologie** via des réseaux bayésiens et une simulation multi‑agents.  
- Analyser comment les outils d'IA influencent le développement conceptuel en lecture.  
- Étudier les schémas d'apprentissage interlinguistiques et neurodivers (dyslexie, troubles du langage).  

### Objectifs méthodologiques  
- **Terrain 1 (M8–M10) :** Évaluation initiale (N=160 élèves) et collecte des données de base.  
- **Secondement (M10–M16) :** Développement de l'APK MVP au *tiilt lab* (Northwestern) avec le Prof. Worsley.  
- **Terrain 2 (M16–M20) :** Déploiement du prototype et pilot‑test (N=30 élèves, 15 dyslexiques, 15 typiques).  
- **Produire un jeu de données multilingue** d'interactions de lecture médiatisées par l'IA.  

### Objectifs de développement de carrière  
- Renforcer l'expertise en modélisation cognitive computationnelle grâce au secondement à Northwestern.  
- Construire un réseau de recherche international durable (Europe–Afrique–USA) via la collaboration avec le Prof. Worsley, le MINESEC et l'UCPH.  
- Publier **4 articles de rang A** (M8, M16, M22).  

---

# PARTIE B2 — IMPACT  

## Impact sur le chercheur  
- Expertise avancée en modélisation cognitive et en pédagogie de l'IA.  
- Profil interdisciplinaire solide (philosophie, linguistique, IA).  
- Visibilité internationale renforcée par le réseau transatlantique et africain.  

## Impact sur l'établissement d'accueil  
- Nouvelles collaborations en sciences cognitives et en éducation numérique.  
- Méthodologies innovantes pour l'alphabétisation assistée par l'IA.  
- Cadre de recherche transcontinental et institutionnel (MINESEC).  

## Impact sur l'Europe  
- Contribution à l'éducation numérique et aux cadres éthiques de l'IA.  
- Innovation en sciences cognitives pour l'apprentissage multilingue.  

## Impact sur l'Afrique  
- **Impact sur le terrain :** Amélioration concrète de la compréhension en lecture dans les ZEP du Cameroun (4 écoles pilotes).  
- Renforcement des littératies numériques multilingues (français/fulfulde).  
- Modèles d'apprentissage inclusifs et extensibles pour la neurodiversité.  

---

# PARTIE B3 — MISE EN ŒUVRE  

## Lots de travail (Work Packages)  

### WP1 — Fondements théoriques (M1–M8)  
Formalisation du modèle du Trapèze Cognitif en un **réseau bayésien** et une **simulation multi‑agents (ABM)** prédictive.  
*Livrable :* Rapport technique + **Article 1 (Théorie)** soumis en M8.  

### WP2 — Validation empirique (M6–M22)  
- **M8–M10 :** Évaluation initiale (N=160).  
- **M10–M16 :** Le chercheur est en secondement à Northwestern. Aucune activité terrain.  
- **M16–M20 :** Déploiement du prototype MVP et collecte de données dans les 4 écoles. Supervisé par les ICR du MINESEC.  
- **M20–M22 :** Analyse statistique finale (régression bayésienne, modèles multiniveaux).  
*Livrables :* **Article 2 (Descriptif)** soumis M16 + **Article 3 (Confirmatoire)** soumis M22.  

### WP3 — Prototypage IA et modélisation computationnelle (M10–M22)  
- **M10–M16 :** Secondement intensif à Northwestern (*tiilt lab*). Développement de l'APK Android (Whisper Large quantifié + Qwen 0.5B LLM).  
- **M16–M20 :** Pilot‑test du prototype dans les 4 écoles (N=30).  
- **M20–M22 :** Analyse des données et rédaction de l'article technique.  
*Livrables :* APK alpha fonctionnelle + **Article 4 (Technique)** soumis M22 (co‑auteur Marcelo Worsley).  

### WP4 — Consortium et pérennité (M15–M24)  
Construction d'un partenariat durable Afrique–Europe (accords institutionnels) et pré‑proposition ERC Synergy.  
*Livrables :* Consortium agreement + pré‑proposition ERC (M23) + atelier de dissémination (M24).

---

## Diagramme de Gantt (Aperçu textuel)  
- **Mois 1–8 :** WP1 (Théorie – Europe)  
- **Mois 8–10 :** WP2 (Terrain 1 – Cameroun)  
- **Mois 10–16 :** WP3 (Secondement – Northwestern, USA)  
- **Mois 16–20 :** WP2/WP3 (Terrain 2 – Cameroun)  
- **Mois 20–22 :** WP2/WP3 (Analyse finale – Europe)  
- **Mois 22–24 :** WP4 (Consortium & ERC – Europe + Cameroun)  

**Jalons de publication :** Article 1 (M8) | Article 2 (M16) | Articles 3 & 4 (M22)  

---

## Risques et mesures d'atténuation  
- **Faible disponibilité des participants :** Élargir le recrutement via le réseau IA_4_ZEP et les ICR du MINESEC.  
- **Complexité de la modélisation :** Prototypage itératif avec collaboration des étudiants de Northwestern.  
- **Variabilité des données :** Triangulation par méthodes mixtes.  

---

# Éthique et Science Ouverte  
- Conformité au RGPD pour les données des apprenants ; jeux de données anonymisés.  
- Code et prototypes publiés en open‑source (GitHub, Zenodo) sous licence MIT/GPL.  
- Preprint sur arXiv co‑signé avec Marcelo Worsley (avant M1).  
- Traitement éthique des participants neurodivers.  

---

# Budget indicatif (24 mois)  
- **Contribution européenne demandée :** **283 502 €** (taux de financement 100 %)  
  - Bourse de vie (incl. CCC Danemark 115,5 %) : 176 022 €  
  - Allocation de mobilité : 17 040 €  
  - Allocation familiale (si applicable) : 15 840 €  
  - Recherche, Formation & Réseautage (RTN) : 24 000 €  
  - Frais de gestion & coûts indirects : 15 600 €  
  - Équipement & logiciels : 6 000 €  
  - Voyages & logistique : 16 000 €  
  - Publications Open Access : 8 000 €  
  - Contingence : 5 000 €  

---

# Adéquation avec l'établissement d'accueil et plan de formation  
L'établissement hôte (Université de Copenhague, UCPH) fournira :  
- une expertise en sciences cognitives et en IA ;  
- un accès aux installations de modélisation computationnelle ;  
- un encadrement interdisciplinaire sous la direction du Professeur Daniel Spikol ;  
- une intégration dans les réseaux de recherche européens.  

Le plan de formation comprend :  
- des cours avancés en modélisation cognitive (réseaux bayésiens, ABM) ;  
- des ateliers sur l'apprentissage médiatisé par l'IA ;  
- un **secondement de 6 mois (M10–M16) à Northwestern** sous la supervision du Professeur Marcelo Worsley pour le prototypage technique.  

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
