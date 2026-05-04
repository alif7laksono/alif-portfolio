# 02 — Project Details (RTCC-O)

## Project Name
Alif Wiji Laksono — Frontend Developer Portfolio

## RTCC-O Framework

### Role
You are a senior frontend developer and UI/UX designer helping me build a personal portfolio website that I will fully understand and be able to explain to any recruiter.

### Task
Build a complete, responsive, single-page portfolio website using only HTML5, CSS3, and vanilla JavaScript. The site must include: navigation, hero section, about, skills, projects, experience timeline, and contact footer.

### Context
- **Developer:** Alif Wiji Laksono — Frontend Developer, Semarang, Indonesia
- **Real tech stack:** Next.js, TypeScript, Tailwind CSS, MongoDB, AWS S3, Node.js
- **Real projects:** veslavia.com, Balkesmas Ambarawa government site, Nestforma, Aurora & Verdant photography sites
- **Design reference:** passes.com — dark theme, bold typography (Syne font), teal/cyan accent (#2cd9c5)
- **Constraint:** This is a bootcamp homework — must use plain HTML/CSS/JS only (no React, no Next.js)

### Constraints (Yang TIDAK boleh / WAJIB)
- ✅ WAJIB: Semantic HTML5 (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`)
- ✅ WAJIB: Responsive CSS (mobile-first)
- ✅ WAJIB: All code must be explainable to a recruiter
- ❌ TIDAK boleh: Use frameworks (React, Vue, Next.js) for this homework file
- ❌ TIDAK boleh: Submit raw AI output without understanding it
- ❌ TIDAK boleh: Use placeholder/fake project data

### Output
- `index.html` — single-page portfolio with all sections
- `style.css` — complete responsive stylesheet with CSS variables
- Hosted on GitHub Pages at: `https://alif7laksono.github.io/alif-portfolio/`

## File Structure
```
alif-portfolio/
├── README.md
├── index.html
├── style.css
├── assets/
│   ├── desktop-view.png
│   └── mobile-view.png
└── plan/
    ├── 01-brainstorm.md
    ├── 02-details.md
    ├── 03-execution.md
    └── 04-results.md
```

## Design Decisions
| Decision | Choice | Reason |
|---|---|---|
| Color scheme | Dark (#0a0c0f) + Teal (#2cd9c5) | Inspired by passes.com, modern dev aesthetic |
| Font | Syne (headings) + DM Sans (body) | Bold, distinctive — not generic Inter/Roboto |
| Layout | Single page, scroll sections | Simple, fast, no routing needed |
| Animation | CSS IntersectionObserver scroll reveal | Pure JS, no library dependency |
| Responsive | Mobile-first CSS with breakpoints | Required by homework spec |
