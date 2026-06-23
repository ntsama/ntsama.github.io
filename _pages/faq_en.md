---

✅ VERSION FINALE — FAQ (EN)
(mise à jour + corrections + enrichissement)

`markdown
---
layout: page
title: "FAQ — Technical & Academic Questions"
permalink: /faq/
lang: en
description: "Technical FAQ for ntsama.github.io — GitHub Pages, links, permalinks, bilingual navigation, images, PDFs, and common errors."
---

<div style="text-align:right; font-size:0.9rem; margin-bottom:15px;">
  🌐 <a href="/faq_fr/" style="font-weight:bold;">FR</a>
</div>

❓ FAQ — Technical & Academic Questions
This page answers the most common questions about the technical functioning of the site, GitHub Pages errors, bilingual navigation, and academic content structure.

---

🔧 1. Why do I get a 404 – File not found error?

Most frequent causes:  
- The permalink does not match the URL.  
- The filename does not match the permalink (case‑sensitive).  
- The file is not in the root folder of the repository.  
- The menu link points to the wrong path.

Correct front matter:

`yaml
---
layout: page
title: "Page Title"
permalink: /page_name/
lang: en
---
`

Test the URL:  
https://ntsama.github.io/page_name/

---

🔧 2. Why does a button not redirect?

Most common cause:  
The link uses a relative path or a Copilot internal link.

❌ Incorrect  
`
About
`

❌ Incorrect (Copilot internal link)  
`
About
`

✅ Correct  
`
About
`

👉 Always use absolute links starting with /.

---

🔧 3. Why do some links break when using /home?

If you use /home as a prefix, relative links become:

`
/home/about_en
`

instead of:

`
/about_en/
`

👉 Solution:  
Use absolute links everywhere.

---

🔧 4. Why do EN/FR buttons redirect to the wrong page?

Because the language selector must point to the correct bilingual pair.

Correct example for a French page:

`html
🌐 <a href="/about/">EN</a>
`

Correct example for an English page:

`html
🌐 <a href="/about_fr/">FR</a>
`

👉 Each page must have one and only one language switch button.

---

🔧 5. Why do images or PDFs not display?

Possible causes:  
- Wrong path  
- Wrong filename (case‑sensitive)  
- File not stored in /assets/

Correct image:

`html
<img src="/assets/photo.jpg" alt="Jean Marie Ntsama">
`

Correct PDF:

`markdown
Download CV
`

---

🔧 6. Why does GitHub Pages not update immediately?

GitHub Pages may take 10–60 seconds to rebuild.

Solutions:  
- Wait a few seconds  
- Refresh the page  
- Force refresh (Ctrl+Shift+R)  
- Clear browser cache  

---

🔧 7. Why does my menu not display correctly?

Common causes:  
- Duplicate navigation: or nav: keys in _config.yml  
- Wrong indentation  
- Missing hyphens in YAML lists  
- Invisible characters copied from Word or PDF

Correct example:

`yaml
navigation:
  - title: "About"
    url: /about/
  - title: "Research"
    url: /research/
`

---

🔧 8. Why does my page not appear in the menu?

Because al‑folio does not automatically add pages to the navigation.  
You must manually add them in _config.yml.

---

🔧 9. Why does my page show raw HTML or broken layout?

Causes:  
- Missing closing tags (</div>)  
- Missing blank line after front matter  
- Markdown inside HTML blocks without proper spacing

Solution:  
Always leave one blank line after the front matter.

---

🔧 10. Why does my bilingual structure break?

Each page must follow this rule:

| English page | French page |
|--------------|-------------|
| /about/ | /about_fr/ |
| /research/ | /research_fr/ |
| /teaching/ | /teaching_fr/ |
| /msca/ | /msca_fr/ |
| /projects/ | /projects_fr/ |
| /faq/ | /faq_fr/ |

👉 Never mix EN and FR links in the footer or header.

---

🧠 Academic FAQ — Research & Teaching

---

📘 11. What is the Cognitive Trapeze Model?

A dynamic framework describing how learners move between:  
- linguistic structures  
- cognitive representations  
- conceptual anchors  
- technological mediation  

It explains how AI tools influence reasoning, conceptual development, and metacognition.

---

📘 12. What is the Pedagogical Swing?

An educational extension of the Cognitive Trapeze describing the rhythm of learning:  
- stability → understanding  
- exploration → discovery  

It models how teachers and learners co‑construct meaning.

---

📘 13. How does your research connect to teaching?

My teaching integrates:  
- language–thought dynamics  
- AI‑augmented learning  
- digital literacies  
- multilingual cognition  
- cognitive modeling  

---

📘 14. What is IA4ZEP?

A program dedicated to:  
- digital empowerment  
- AI‑supported pedagogy  
- inclusive learning  
- multilingual practices  
- teacher training in priority education zones  

---

🛠️ Troubleshooting Guide — Step by Step

---

🟩 Step 1 — Identify the problem
Note:  
- exact URL  
- button clicked  
- error message  

🟩 Step 2 — Check the file
Verify the front matter:

`yaml
---
layout: page
title: "Title"
permalink: /page_name/
lang: en
---
`

🟩 Step 3 — Check the link
Correct link:

`
/page_name/
`

🟩 Step 4 — Test the URL directly
`
https://ntsama.github.io/page_name/
`

🟩 Step 5 — Check filename case
abouten.md ≠ AboutEn.md

🟩 Step 6 — Wait for GitHub Pages propagation

🟩 Step 7 — Create a test page if needed

`markdown
---
layout: page
title: "Test Page"
permalink: /test_page/
---

Test Page
`

---

<hr style="margin-top:40px;">

<div style="text-align:center; font-size:0.85rem; opacity:0.85;">
  <a href="/about/">About</a> •
  <a href="/theory/">Theory</a> •
  <a href="/research/">Research</a> •
  <a href="/msca/">MSCA</a> •
  <a href="/ia4zep/">IA4ZEP</a> •
  <a href="/faq/">FAQ</a>
</div>
`

---

