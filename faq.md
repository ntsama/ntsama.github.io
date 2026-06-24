---
layout: page
title: "FAQ — Technical & Academic Questions"
lang: en
description: "FAQ for ntsama.github.io — GitHub Pages troubleshooting, research content, and MSCA project."
---

<div style="text-align:right; font-size:0.9rem; margin-bottom:15px;">
  🌐 <a href="/faq_fr/" style="font-weight:bold;">FR</a>
</div>

# FAQ — Frequently Asked Questions

Welcome to the FAQ of my academic website. This page is divided into two sections: **technical troubleshooting** for the site, and **academic questions** about my research and projects.

---

## 🔧 Technical Troubleshooting (GitHub Pages)

**1. Why do I get a 404 – File not found error?**  
Ensure the file's permalink (e.g., `/pagename/`) exactly matches the URL typed in your browser, and that the filename respects case sensitivity.

**2. Why does the EN/FR language button redirect incorrectly?**  
Each page must have exactly one language button pointing to its opposite version:
- On a FR page: `<a href="/about/">EN</a>`
- On an EN page: `<a href="/about_fr/">FR</a>`

**3. Why do my images or PDFs not display?**  
Files must be placed inside the `/assets/` folder at the root of the repository. Example: `<img src="/assets/photo.jpg">`.

**4. Why does my menu not display correctly?**  
The navigation is managed manually in the `_config.yml` file. Check for indentation errors or missing hyphens.

**5. How do I force GitHub Pages to update the site?**  
Wait 10 to 60 seconds after a `git push`. You can also force refresh your browser using `Ctrl+Shift+R`.

---

## 🧠 Academic FAQ (Research & Projects)

**6. What is the Cognitive Trapeze Model?**  
A theoretical framework describing how learners navigate between linguistic structures, cognitive representations, and technological tools (AI). It models the co-evolution of language and thought.

**7. How can I collaborate with you on a research project?**  
I am open to interdisciplinary collaborations on topics like AI in education, neurodiversity, and digital literacies in Africa. You can reach out directly via the **[Contact](/contact/)** page.

**8. Where can I find your pedagogical resources or research data?**  
My publications are listed on the **[Publications](/publications/)** page. Pedagogical tools and datasets related to the IA_4_ZEP or MSCA projects are mentioned on their dedicated pages and are available upon request.

**9. What is the status of your MSCA project (Cognitive Trapeze)?**  
The project is currently in the theoretical development and experimental preparation phase. The goal is to formalize the computational model and launch multilingual data collection in Europe and Africa. More details on the **[MSCA](/msca/)** page.

---

<hr style="margin-top:40px;">

<div style="text-align:center; font-size:0.85rem; opacity:0.85;">
  <a href="/about/">About</a> • <a href="/theory/">Theory</a> • <a href="/research/">Research</a> • <a href="/msca/">MSCA</a> • <a href="/ia4zep/">IA_4_ZEP</a> • <a href="/faq/">FAQ</a>
</div>
