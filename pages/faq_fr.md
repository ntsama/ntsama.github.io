---

✅ VERSION FINALE — FAQ_FR (mise à jour + enrichie)
(à remplacer intégralement dans ton fichier)

`markdown
---
layout: page
title: "FAQ — Questions techniques"
permalink: /faq_fr/
lang: fr
description: "FAQ technique pour ntsama.github.io — GitHub Pages, liens, permalinks, navigation bilingue, images, PDF et erreurs courantes."
---

<div style="text-align:right; font-size:0.9rem; margin-bottom:15px;">
  🌐 <a href="/faq/" style="font-weight:bold;">EN</a>
</div>

❓ FAQ Technique — GitHub Pages (ntsama.github.io)

Cette page répond aux questions les plus fréquentes concernant le fonctionnement technique du site, les erreurs possibles, la navigation bilingue et les bonnes pratiques de maintenance.

---

🔧 1. Pourquoi ai‑je une erreur 404 – Page introuvable ?

Causes fréquentes :  
- Le permalink ne correspond pas à l’URL.  
- Le nom du fichier ne correspond pas (sensible à la casse).  
- Le fichier n’est pas à la racine du dépôt.  
- Le lien du menu pointe vers un mauvais chemin.

Front matter correct :

`yaml
---
layout: page
title: "Titre"
permalink: /nomdepage/
lang: fr
---
`

Tester l’URL :  
https://ntsama.github.io/nomdepage/

---

🔧 2. Pourquoi un bouton ne redirige pas ?

Cause principale :  
Le lien utilise un chemin relatif ou un lien interne Copilot.

❌ Incorrect  
`
À propos
`

❌ Incorrect (Copilot)  
`
À propos
`

✅ Correct  
`
À propos
`

👉 Toujours utiliser des liens absolus commençant par /.

---

🔧 3. Pourquoi certains liens cassent quand j’utilise /home ?

Parce que les liens relatifs deviennent :

`
/home/about_fr
`

au lieu de :

`
/about_fr/
`

👉 Solution :  
Utiliser uniquement des liens absolus.

---

🔧 4. Pourquoi les boutons EN/FR redirigent mal ?

Chaque page doit avoir un seul bouton de langue, pointant vers sa version opposée.

Exemple correct pour une page FR :

`html
🌐 <a href="/about/">EN</a>
`

Exemple correct pour une page EN :

`html
🌐 <a href="/about_fr/">FR</a>
`

👉 Ne jamais mélanger EN et FR dans le footer ou le header.

---

🔧 5. Pourquoi les images ou PDF ne s’affichent pas ?

Causes possibles :  
- Mauvais chemin  
- Fichier non placé dans /assets/  
- Mauvaise casse du nom

Image correcte :

`html
<img src="/assets/photo.jpg" alt="Jean Marie Ntsama">
`

PDF correct :

`markdown
Télécharger le CV
`

---

🔧 6. Pourquoi GitHub Pages ne met pas à jour immédiatement ?

GitHub Pages peut prendre 10 à 60 secondes pour reconstruire le site.

Solutions :  
- Attendre quelques secondes  
- Rafraîchir la page  
- Forcer le rafraîchissement (Ctrl+Shift+R)  
- Vider le cache du navigateur  

---

🔧 7. Pourquoi mon menu ne s’affiche pas correctement ?

Causes fréquentes :  
- Présence de deux blocs navigation: dans _config.yml  
- Mauvaise indentation YAML  
- Tirets manquants  
- Caractères invisibles (copiés depuis Word/PDF)

Exemple correct :

`yaml
navigation:
  - title: "À propos"
    url: /about_fr/
  - title: "Recherche"
    url: /research_fr/
`

---

🔧 8. Pourquoi ma page n’apparaît pas dans le menu ?

Parce que al‑folio n’ajoute pas automatiquement les pages.  
Il faut les ajouter manuellement dans _config.yml.

---

🔧 9. Pourquoi ma mise en page est cassée ?

Causes :  
- Balises HTML non fermées (</div>)  
- Absence de ligne vide après le front matter  
- Markdown placé dans un bloc HTML sans espace

Solution :  
Toujours laisser une ligne vide après le front matter.

---

🔧 10. Comment structurer correctement le bilingue ?

Chaque page doit avoir son paire EN/FR :

| Page EN | Page FR |
|---------|---------|
| /about/ | /about_fr/ |
| /research/ | /research_fr/ |
| /teaching/ | /teaching_fr/ |
| /projects/ | /projects_fr/ |
| /msca/ | /msca_fr/ |
| /faq/ | /faq_fr/ |

👉 Le footer doit correspondre à la langue de la page.

---

🧠 FAQ Académique — Recherche & Pédagogie

---

📘 11. Qu’est‑ce que le Modèle du Trapèze Cognitif ?

Un cadre dynamique décrivant comment les apprenants se déplacent entre :  
- structures linguistiques  
- représentations cognitives  
- points d’appui conceptuels  
- médiation technologique  

Il explique comment l’IA influence le raisonnement et la métacognition.

---

📘 12. Qu’est‑ce que la Balançoire Pédagogique ?

Une extension éducative du Trapèze Cognitif.  
Elle modélise le rythme de l’apprentissage :  
- stabilité → compréhension  
- exploration → découverte  

---

📘 13. Comment votre recherche influence‑t‑elle votre enseignement ?

Mon enseignement intègre :  
- dynamiques langage–pensée  
- apprentissage augmenté par IA  
- littératies numériques  
- cognition multilingue  
- modélisation cognitive  

---

📘 14. Qu’est‑ce que le programme IA4ZEP ?

Un programme dédié à :  
- l’autonomisation numérique  
- la pédagogie assistée par IA  
- l’inclusion en zones prioritaires  
- les pratiques multilingues  
- la formation des enseignants  

---

🛠️ Guide de résolution — Étapes

---

🟩 Étape 1 — Identifier le problème
Noter :  
- l’URL  
- le bouton cliqué  
- le message affiché  

🟩 Étape 2 — Vérifier le fichier
`yaml
---
layout: page
title: "Titre"
permalink: /nomdepage/
lang: fr
---
`

🟩 Étape 3 — Vérifier le lien
`
/nomdepage/
`

🟩 Étape 4 — Tester l’URL directe
`
https://ntsama.github.io/nomdepage/
`

🟩 Étape 5 — Vérifier la casse
aboutfr.md ≠ AboutFr.md

🟩 Étape 6 — Attendre la propagation

🟩 Étape 7 — Créer une page de test
`markdown
---
layout: page
title: "Test Page"
permalink: /test_page/
---

Page de test
`

---

<hr style="margin-top:40px;">

<div style="text-align:center; font-size:0.85rem; opacity:0.85;">
  <a href="/about_fr/">À propos</a> •
  <a href="/theory_fr/">Théorie</a> •
  <a href="/research_fr/">Recherche</a> •
  <a href="/msca_fr/">MSCA</a> •
  <a href="/ia4zepfr/">IA4_ZEP</a> •
  <a href="/faq_fr/">FAQ</a>
</div>
`

---
