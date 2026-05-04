# 03 — Execution (Step-by-Step)

## Step 1 — Setup Repository

```bash
# Di GitHub.com:
# 1. New repository → Name: alif-portfolio
# 2. ✅ Add README
# 3. Create repository

# Di terminal:
git clone https://github.com/alif7laksono/alif-portfolio.git
cd alif-portfolio
mkdir plan assets
```

## Step 2 — Build index.html

### Struktur Semantic HTML yang Digunakan

```html
<nav>          → Fixed navigation bar dengan hamburger menu
<header>       → Hero section dengan headline + stats
<main>
  <section id="about">      → About me + tech stack tags
  <section id="skills">     → 4 skill cards (Frontend, Backend, Tools, Practices)
  <section id="projects">   → 4 project cards dari real projects
  <section id="experience"> → Timeline work history
</main>
<footer id="contact"> → Contact links + email + GitHub
```

### Kenapa Semantic HTML?
- `<nav>` → browser dan screen reader tahu ini navigasi
- `<header>` → area utama/intro halaman
- `<main>` → konten utama, hanya boleh satu per halaman
- `<section>` → grup konten bertema, dengan heading
- `<footer>` → info penutup, kontak, copyright

## Step 3 — Build style.css

### CSS Variables (Design Tokens)
```css
:root {
  --bg:    #0a0c0f;     /* Background utama */
  --teal:  #2cd9c5;     /* Accent color (dari passes.com) */
  --white: #f0f4f8;     /* Teks heading */
  --muted: #7a8a99;     /* Teks body/secondary */
  --card:  #111620;     /* Background card */
}
```
Kenapa CSS variables? → Satu tempat ubah warna, berlaku di seluruh halaman.

### Mobile-First Responsive
```css
/* Default → Mobile styles */
.about-grid { grid-template-columns: 1fr; }

/* Tablet ke atas */
@media (min-width: 768px) {
  .about-grid { grid-template-columns: 1fr 1fr; }
}
```

### Scroll Reveal Animation
```javascript
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) e.target.classList.add('visible');
  });
}, { threshold: 0.1 });
```
Artinya: ketika elemen masuk viewport 10%, tambah class `visible` yang trigger CSS transition opacity + translateY.

## Step 4 — Commit & Push

```bash
git add .
git commit -m "Initial commit: portfolio website"
git push origin main
```

## Step 5 — Enable GitHub Pages

```
Repository → Settings → Pages
Source: Deploy from branch
Branch: main / (root)
Save
```

Live URL: `https://alif7laksono.github.io/alif-portfolio/`

## Challenges & Solutions

| Challenge | Solution |
|---|---|
| Featured project card span 2 columns | `grid-column: span 2` + media query reset ke 1 di mobile |
| Nav hamburger di mobile | Toggle class `.open` dengan JS event listener |
| Glow background tanpa performance hit | `filter: blur()` pada absolute div, `pointer-events: none` |
| Font loading cepat | Google Fonts dengan hanya weight yang dipakai |
