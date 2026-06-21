---
layout: page
title: "FAQ — Technical & Academic Questions"
permalink: /faq_en/
lang: en
---
<div style="text-align:right; font-size:0.9rem;">
  🌐 <a href="/faq/">FR</a> | <a href="/faq_en/">EN</a>
</div>

# ❓ Technical FAQ — GitHub Pages (ntsama.github.io)

This page answers the most common questions about the technical functioning of the site, errors, and quick solutions.


🔵 1. Why do I get a 404 – File not found error?

Possible causes:
- The page permalink does not match the URL.
- The file is not in the repository root.
- The filename does not match (case sensitive).
- The menu link is incorrect.

Solution:
1. Open the file (e.g., about_en.md).
2. Ensure it begins with:

`yaml
---
layout: default
title: "Title"
permalink: /page_name/
---
`

3. Test the URL:  
   https://ntsama.github.io/page_name/

---

🔵 2. Why does a button not redirect?

Most common cause:  
The link uses a Copilot internal format or a relative path.

Incorrect:
`markdown
About
About
`

Correct:
`markdown
About
`

👉 Always use absolute links.

---

🔵 3. Why does /home work but some links fail?

Relative links become:

`
/home/about_en
`

instead of:

`
/about_en/
`

👉 Always start links with /.

---

🔵 4. Why do EN/FR buttons redirect to About / À propos?

Because the language selector points to:

`html
<a href="/about_en/">EN</a>
<a href="/about_fr/">FR</a>
`

If you want EN/FR to redirect to a bilingual home page, create:

- /home_en/
- /home_fr/

---

🔵 5. Why do images or PDFs not display?

Possible causes:
- Wrong path.
- File not in assets/.
- Wrong filename case.

Correct image:
`html
<img src="/assets/photo.jpg" alt="Jean Marie Ntsama">
`

Correct PDF:
`markdown
Download CV
`

---

🔵 6. Why does GitHub Pages not update immediately?

GitHub Pages may take 10–60 seconds to refresh.

Solution:
- Wait a few seconds.
- Refresh the page.
- Clear cache if needed.

---

🛠️ Troubleshooting Guide — Step by Step

---

🟩 Step 1 — Identify the problem

Note:
- Exact URL
- Button clicked
- Error message

---

🟩 Step 2 — Check the file

Verify the front matter:

`yaml
---
layout: default
title: "Title"
permalink: /page_name/
---
`

---

🟩 Step 3 — Check the link

Correct link:

`
/page_name/
`

---

🟩 Step 4 — Test the URL directly

`
https://ntsama.github.io/page_name/
`

---

🟩 Step 5 — Check filename case

abouten.md ≠ Abouten.md

---

🟩 Step 6 — Wait for GitHub Pages propagation

---

🟩 Step 7 — Create a test page if needed

`markdown
---
layout: default
title: "Test Page"
permalink: /test_page/
---

Test Page
.
---
layout: default
title: "Title"
permalink: /page_name/
---
