---
layout: page
title: "FAQ — Questions techniques"
permalink: /faq_fr/
lang: fe
---

<div style="text-align:right; font-size:0.9rem;">
  🌐 <a href="/faq/">FR</a> | <a href="/faq_en/">EN</a>
</div>

# ❓ FAQ Technique — GitHub Pages (ntsama.github.io)

Cette page répond aux questions les plus fréquentes concernant le fonctionnement technique du site, les erreurs possibles et les solutions rapides.

---

## 📘 Documentation Technique — Site GitHub Pages (ntsama.github.io)

Ce document regroupe toutes les règles techniques, solutions, bonnes pratiques et procédures de maintenance pour garantir le bon fonctionnement du site GitHub Pages.

---

🟦 1. Structure d’une page GitHub Pages

Chaque page doit commencer par un front matter :

`yaml
---
layout: default
title: "Titre de la page"
permalink: /nomdepage/
---
`

Règles :
- Le permalink commence et finit par /.
- Le fichier doit être en .md ou .html.
- Le titre doit être unique et cohérent.

---

🟦 2. Règles d’or pour les liens internes

✔️ Toujours utiliser des liens absolus

Correct :
`
About (EN)
`

Incorrect :
`
About
About
`

✔️ Toujours faire correspondre le lien au permalink

Si la page contient :
`
permalink: /research_en/
`

Alors le lien doit être :
`
/research_en/
`

---

🟦 3. Navigation EN/FR

Dans chaque page :

`html
<div style="text-align:right; font-size:0.9rem;">
  🌐 <a href="/abouten/">EN</a> | <a href="/aboutfr/">FR</a>
</div>
`

Règles :
- EN pointe vers la version anglaise.
- FR pointe vers la version française.
- Les permalinks doivent exister.

---

🟦 4. Gestion des erreurs 404

Symptômes :
- Page introuvable
- Lien cassé
- Redirection incorrecte

Causes :
- Mauvais permalink
- Mauvais lien
- Mauvaise casse du nom de fichier
- Fichier déplacé

Solution rapide :
1. Vérifier le front matter.
2. Vérifier le lien dans le menu.
3. Tester l’URL directe :
   `
   https://ntsama.github.io/nomdepage/
   `

---

🟦 5. Boutons qui ne redirigent pas

Causes :
- Liens Copilot (ca://…)
- Liens relatifs
- Permalink manquant

Solution :
Remplacer par des liens absolus :

`
IA4ZEP (EN)
`

---

🟦 6. Problèmes d’images ou PDF

Causes :
- Mauvais chemin
- Fichier non placé dans assets/
- Mauvaise casse

Solution :
`html
<img src="/assets/photo.jpg" alt="Jean Marie Ntsama">
`

Pour un PDF :
`markdown
Download CV
`

---

🟦 7. Délai de mise à jour GitHub Pages

GitHub Pages peut prendre 10 à 60 secondes pour se rafraîchir.

Solutions :
- Attendre quelques secondes
- Rafraîchir la page
- Vider le cache si nécessaire

---

🛠️ 8. Guide de résolution — Étape par étape

🟩 Étape 1 — Identifier le problème
Note :
- L’URL exacte
- Le bouton cliqué
- Le message affiché

---

🟩 Étape 2 — Vérifier le fichier
Ouvrir le fichier correspondant et vérifier :

`yaml
---
layout: default
title: "Titre"
permalink: /nomdepage/
---
`

---

🟩 Étape 3 — Vérifier le lien
Le lien doit être :

`
/nomdepage/
`

---

🟩 Étape 4 — Tester l’URL directe
Dans le navigateur :

`
https://ntsama.github.io/nomdepage/
`

---

🟩 Étape 5 — Vérifier la casse
- abouten.md ≠ Abouten.md
- Researchen.md ≠ researchen.md

---

🟩 Étape 6 — Attendre la propagation
GitHub Pages peut mettre un petit délai.

---

🟩 Étape 7 — Créer une page de test si nécessaire

`markdown
---
layout: default
title: "Test Page"
permalink: /test_page/
---

Test Page
`

Tester :
`
https://ntsama.github.io/test_page/
`

---

🟦 9. Modèles prêts à l’emploi

Modèle EN
`markdown
---
layout: default
title: "About (EN)"
permalink: /about_en/
---

<div style="text-align:right; font-size:0.9rem;">
  🌐 <a href="/abouten/">EN</a> | <a href="/aboutfr/">FR</a>
</div>

About (EN)
`

Modèle FR
`markdown
---
layout: default
title: "À propos (FR)"
permalink: /about_fr/
---

<div style="text-align:right; font-size:0.9rem;">
  🌐 <a href="/abouten/">EN</a> | <a href="/aboutfr/">FR</a>
</div>

À propos (FR)
`

---

🟦 10. Checklist de maintenance

✔️ Avant d’ajouter une page
- Nom du fichier correct
- Front matter complet
- Permalink défini

✔️ Avant d’ajouter un lien
- Lien absolu
- Correspondance exacte avec le permalink

✔️ Après modification
- Tester l’URL directe
- Tester depuis /home
- Tester depuis le menu
- Tester depuis le footer

---

📬 Besoin d’aide ?

En cas de dysfonctionnement, note :
- la page concernée  
- le bouton cliqué  
- le comportement observé  



layout: default
title: "Titre"
permalink: /nom_de_page/
---
