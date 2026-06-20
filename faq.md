---
layout: default
title: "FAQ Technique"
permalink: /faq/
---

<div style="text-align:right; font-size:0.9rem;">
  🌐 <a href="/faq/">FR</a> | <a href="/faq_en/">EN</a>
</div>

# ❓ FAQ Technique — GitHub Pages (ntsama.github.io)

Cette page répond aux questions les plus fréquentes concernant le fonctionnement technique du site, les erreurs possibles et les solutions rapides.

---

## 🔵 1. Pourquoi j’obtiens une erreur **404 – File not found** ?

**Causes possibles :**
- Le `permalink` de la page ne correspond pas à l’URL.
- Le fichier n’est pas à la racine du dépôt.
- Le nom du fichier ne correspond pas (la casse compte).
- Le lien dans le menu n’est pas correct.

**Solution :**
1. Ouvrir le fichier concerné (ex : `about_en.md`).
2. Vérifier qu’il commence par :

```yaml
---
layout: default
title: "Titre"
permalink: /nom_de_page/
---
