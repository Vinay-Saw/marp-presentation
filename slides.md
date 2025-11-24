---
marp: true
theme: custom-theme
class: lead
paginate: true
---

<!-- Custom Theme Specification -->
<style>
section {
  font-family: 'Segoe UI', sans-serif;
}

h1, h2, h3 {
  color: #1a73e8;
}

img.bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0.15;
  z-index: -1;
}
</style>

# Product Documentation Presentation
### Using **Marp** for Maintainable Slides
#### Vinay — 23f2005452@ds.study.iitm.ac.in

---

# Why Marp?
- Markdown-based slides
- Easy version control (Git)
- Export to PDF/HTML/PPTX
- Developer-friendly

---

# Custom Theme Info
This presentation uses:
- Custom fonts
- Custom heading colors
- Custom background styling

---

# Background Image Slide
![bg](https://picsum.photos/1200/800)

## Example Slide with Background Image
- This slide demonstrates background usage
- Image applied with low opacity

---

# Page Numbers Enabled
Marp automatically numbers slides when `paginate: true` is set.

---

# Custom Styling Example

```css
section {
  background-color: #f5f9ff;
  border-left: 10px solid #1a73e8;
  padding: 20px;
}
```

This adds a soft layout aesthetic.

---

# Mathematical Equations
### Algorithmic Complexity Example

Using inline LaTeX:

$$ T(n) = O(n \log n) $$

Example for merge sort.

Or recurrence:

$$ T(n) = 2T\left(\frac{n}{2}\right) + O(n) $$

---

# Thank You!
### Questions?

