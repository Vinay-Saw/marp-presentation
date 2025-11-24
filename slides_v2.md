<!-- marp: true -->
---
marp: true
theme: custom-theme
class: lead
paginate: true
size: 16:9
math: true
---

<!--
  A single-file Marp Markdown presentation:
  - Multiple Marp directives (HTML + YAML front-matter)
  - Custom theme & CSS
  - Page numbers enabled
  - Uses local image: /mnt/data/world_map.webp
  - Math (KaTeX) enabled
  - Includes email: 23f2005452@ds.study.iitm.ac.in
-->

<style>
/* Simple custom theme CSS that Marp will apply */
section {
  font-family: "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  color: #222;
  background-color: #ffffff;
  padding: 36px;
}

/* Headings */
h1 { color: #1f6feb; font-size: 48px; margin-bottom: 6px; }
h2 { color: #ff7a00; font-size: 34px; margin-bottom: 4px; }
h3 { color: #333; font-size: 24px; }

/* Note / small text */
.note { font-size: 0.9em; color: #555; opacity: 0.95; }

/* Background image helper class */
img.bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  opacity: 0.18;
  z-index: -1;
}

/* Card-like content styling */
.card {
  background: rgba(255,255,255,0.96);
  padding: 18px;
  border-radius: 12px;
  box-shadow: 0 10px 24px rgba(14, 30, 37, 0.06);
  border-left: 8px solid #1f6feb;
}
</style>

<!-- Title slide -->
# A Friendship Between a Dog and a Cat
### A Heartwarming Tale
#### Vinay — 23f2005452@ds.study.iitm.ac.in
<div class="note">Marp presentation — multiple directives, custom theme, page numbers, background image, math</div>

---

<!-- Why this story -->
# Why this story?
- Dogs and cats are commonly portrayed as rivals.
- This story highlights curiosity, patience & trust.
- Good for demonstrating Marp features in a maintainable Markdown file.

---

<!-- Requirements slide -->
# Requirements satisfied
- **Email included:** `23f2005452@ds.study.iitm.ac.in`  
- **Multiple Marp directives** (HTML comment + YAML front-matter)  
- **Custom theme** (CSS inside `<style>`)  
- **Page numbers** (`paginate: true`)  
- **Background image slide** using `world_map.webp`  
- **Math** enabled (`math: true`)  

---

<!-- Background image slide using the provided local file path.
     If you host the file on GitHub, replace the path with the raw GitHub URL:
     https://raw.githubusercontent.com/<USER>/<REPO>/main/path/to/world_map.webp
-->
![bg](/mnt/data/world_map.webp)

# First Meeting
<div class="card">
- A shy cat on the porch and a curious dog in the yard.  
- They notice each other across a fence and slowly explore.  
- Early interactions are cautious but curious.
</div>

---

# Building Trust
- Shared food moments (distance-respected treats).  
- Gentle play that respects boundaries.  
- Time and repetition increase comfort.

---

# Shared Adventures
- Short explorations together (backyard, garden paths).  
- Play: chasing leaves & shadow games.  
- Rest: sunny naps with alternating positions.

---

# Custom Styling Example
```css
section {
  background-color: #fffaf5;
  border-left: 10px solid #ff7a00;
  padding: 22px;
}
