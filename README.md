# NeuByte Technologies — Resume

A modular, data‑driven resume system built with **Jekyll**, **YAML data files**, and **HTML include components**.  
This repository powers the public-facing resume for **Gordon [Last Name]**, designed for clarity, maintainability, and reuse across the NeuByte portfolio.

---

## 📌 Purpose

This repository provides a clean, structured, and easily maintainable resume that:

- Uses **YAML** as the single source of truth for all resume content  
- Uses **HTML include components** for consistent formatting  
- Renders through **Jekyll** for GitHub Pages  
- Ensures theme consistency with the **NeuByte Design System** (Manrope, spacing, layout rules)

The goal is to maintain a professional, version-controlled resume that can be updated quickly without touching layout code.

---

## 🧱 Architecture Overview

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

## 🚀 Local Development

To run the resume locally:

```bash
bundle install
bundle exec jekyll serve

