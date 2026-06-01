# NeuByte Technologies — Resume

A modular, data‑driven resume system built with **Jekyll**, **YAML data files**, and **HTML include components**.  
This repository powers the public-facing resume for **Gordon [Last Name]**, designed for clarity, maintainability, and reuse across the NeuByte portfolio.

---

##  Purpose

This repository provides a clean, structured, and easily maintainable resume that:

- Uses **YAML** as the single source of truth for all resume content  
- Uses **HTML include components** for consistent formatting  
- Renders through **Jekyll** for GitHub Pages  
- Ensures theme consistency with the **NeuByte Design System** (Manrope, spacing, layout rules)

The goal is to maintain a professional, version-controlled resume that can be updated quickly without touching layout code.

---

##  Architecture Overview

### **1. YAML Data Layer (`_data/resume/`)**

All resume content is stored in structured YAML files:

- `work.yml` — Work history  
- `education.yml` — Education  
- `skills.yml` — Skill categories + items  
- `certifications.yml` — Certifications  
- `profile.yml` — Header, summary, contact info  
- `projects.yml` — Optional project highlights  

This ensures clean separation between **content** and **presentation**.

---

### **2. HTML Include Components (`_includes/resume/`)**

Reusable components render each section:

- `job-card.html` — Work experience entries  
- `education-card.html` — Education entries  
- `skill-category.html` — Skill groups  
- `certification-card.html` — Certifications  
- `header-card.html` — Resume header block  
- `header.html` — Page header wrapper  
- `footer.html` — Page footer wrapper  

These components receive YAML data and output consistent, theme-aligned HTML.

---

### **3. Layout (`_layouts/default.html`)**

The resume layout:

- Defines the page structure  
- Loads each YAML dataset  
- Iterates through components  
- Applies NeuByte typography and spacing  

This file is the primary layout used to render the resume.

---

##  Local Development

To run the resume locally:

```bash
bundle install
bundle exec jekyll serve

```

## Repository Structure

/
├── _data/
│   └── resume/
│       ├── work.yml
│       ├── education.yml
│       ├── skills.yml
│       ├── certifications.yml
│       ├── profile.yml
│       └── projects.yml
├── _includes/
│   └── resume/
│       ├── job-card.html
│       ├── education-card.html
│       ├── skill-category.html
│       ├── certification-card.html
│       ├── header-card.html
│       ├── header.html
│       └── footer.html
├── _layouts/
│   └── default.html
├── assets/
├── CNAME
└── about.html
🛠 Updating the Resume
To update content:
Edit the YAML files in _data/resume/.

To update layout or styling:
Modify the HTML includes or the main layout.

To add a new section:
Create a new YAML file

Create a matching include component

Add a loop in default.html

## Deployment
This repository is deployed automatically via GitHub Pages using Jekyll.
Any push to main triggers a rebuild.

## Contributions
This repository is maintained internally by NeuByte Technologies.
External contributions are not currently accepted.

## Contact
For professional inquiries:
godon.neuls@gmail.com
