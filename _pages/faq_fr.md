---
layout: page
title: "FAQ — Questions techniques & Académiques"
permalink: /faq_fr/
lang: fr
description: "FAQ du site ntsama.github.io — erreurs GitHub Pages, contenu académique et projet MSCA."
---

<div style="text-align:right; font-size:0.9rem; margin-bottom:15px;">
  🌐 <a href="/faq/" style="font-weight:bold;">EN</a>
</div>

# FAQ — Questions Fréquentes

Bienvenue sur la FAQ de mon site académique. Cette page est divisée en deux sections : **le dépannage technique** du site, et **les questions académiques** sur mes recherches et mes projets.

---

## 🔧 Dépannage Technique (GitHub Pages)

**1. Pourquoi ai‑je une erreur 404 – Page introuvable ?**  
Vérifiez que le permalink du fichier (ex: `/nomdepage/`) correspond exactement à l'URL tapée dans le navigateur, et que le nom du fichier respecte la casse.

**2. Pourquoi un bouton de langue (EN/FR) ne redirige pas correctement ?**  
Chaque page doit avoir un seul bouton de langue pointant vers sa version opposée :
- Sur une page FR : `<a href="/about/">EN</a>`
- Sur une page EN : `<a href="/about_fr/">FR</a>`

**3. Pourquoi mes images ou PDF ne s'affichent pas ?**  
Les fichiers doivent impérativement se trouver dans le dossier `/assets/` à la racine du dépôt. Exemple : `<img src="/assets/photo.jpg">`.

**4. Pourquoi mon menu ne s'affiche pas correctement ?**  
La navigation est gérée manuellement dans le fichier `_config.yml`. Vérifiez qu'il n'y a pas d'erreur d'indentation ou de tirets manquants.

**5. Comment faire pour que GitHub Pages mette à jour le site ?**  
Il faut attendre 10 à 60 secondes après un `git push`. Vous pouvez forcer le rafraîchissement du navigateur avec `Ctrl+Shift+R`.

---

## 🧠 FAQ Académique (Recherche & Projets)

**6. Qu’est‑ce que le Modèle du Trapèze Cognitif ?**  
C'est un cadre théorique qui décrit comment les apprenants se déplacent entre les structures linguistiques, les représentations cognitives et les outils technologiques (IA). Il modélise la co-évolution du langage et de la pensée.

**7. Comment puis-je collaborer avec vous sur un projet de recherche ?**  
Je suis ouvert aux collaborations interdisciplinaires, notamment sur les thématiques de l'IA en éducation, la neurodiversité, et les littératies numériques en Afrique. Vous pouvez me contacter directement via la page **[Contact](/fr/contact/)**.

**8. Où puis-je trouver vos ressources pédagogiques ou vos données de recherche ?**  
Mes publications sont listées sur la page **[Publications](/fr/publications/)**. Pour les outils pédagogiques et les jeux de données liés au projet IA_4_ZEP ou MSCA, ils sont mentionnés dans les pages dédiées et disponibles sur demande.

**9. Où en est votre projet MSCA (Cognitive Trapeze) ?**  
Le projet est actuellement en phase de développement théorique et de préparation expérimentale. L'objectif est de formaliser le modèle computationnel et de lancer des collectes de données multilingues en Europe et en Afrique. Plus de détails sur la page **[MSCA](/fr/msca/)**.

---

<hr style="margin-top:40px;">

<div style="text-align:center; font-size:0.85rem; opacity:0.85;">
  <a href="/fr/about/">À propos</a> • <a href="/fr/theory/">Théorie</a> • <a href="/fr/research/">Recherche</a> • <a href="/fr/msca/">MSCA</a> • <a href="/fr/ia4zep/">IA_4_ZEP</a> • <a href="/fr/faq/">FAQ</a>
</div>
