# Németh Dávid — Personal Academic Website

This repository hosts the source code of my personal academic website, built using **Jekyll** and the **Academic Pages** template, deployed via **GitHub Pages**.

🔗 **Live site:** [https://ho92ms.github.io](https://ho92ms.github.io)

---

## Overview

The site serves as a professional profile with emphasis on:
- **Software engineering** — system design, DevOps, backend development
- **Applied machine learning** — neural networks, LLMs, interpretable AI
- **Academic rigor** — mathematically grounded, empirically verifiable solutions

---

## Structure

The website is organized into the following sections:

- **[Home](https://ho92ms.github.io/)** — introduction and professional summary
- **[About](https://ho92ms.github.io/about/)** — detailed background and philosophy
- **[Research](https://ho92ms.github.io/research/)** — research interests and methodologies
- **[Experience](https://ho92ms.github.io/experience/)** — professional domains and technical skills
- **[CV](https://ho92ms.github.io/cv/)** — curriculum vitae
- **[Contact](https://ho92ms.github.io/contact/)** — professional contact information

---

## Philosophy

> *"Conceptually simple. Mathematically grounded. Empirically verifiable."*

I prefer solutions that balance theoretical elegance with practical constraints, emphasizing:
1. **Structure** over ad-hoc optimization
2. **Reproducibility** and transparency
3. **Interpretability** in complex systems

---

## Technology Stack

- **Jekyll** — static site generator (GitHub Pages compatible)
- **Markdown** — content authoring
- **Academic Pages** — base template with customizations
- **Custom CSS** — BME/ELTE IK academic styling
- **MathJax** — mathematical notation support

---

## Local Development

To run the site locally:

```bash
# Install dependencies
bundle install

# Serve the site
bundle exec jekyll serve

# View at http://localhost:4000
```

---

## Customization

### Site Configuration
Edit `_config.yml` for site-wide settings (title, author info, plugins).

### Navigation
Modify `_data/navigation.yml` to change menu items.

### Content
- **Pages:** Edit files in `_pages/`
- **Home:** Edit `index.md`
- **Styling:** Customize `assets/css/main.scss`

---

## Deployment

The site is automatically deployed to GitHub Pages when changes are pushed to the `main` branch.

```bash
git add .
git commit -m "Update content"
git push origin main
```

---

## License

The content of this repository is intended for personal and academic use. The underlying Academic Pages template retains its original license.

---

## Contact

📧 **Email:** [neduabi@pm.me](mailto:neduabi@pm.me)  
🔗 **GitHub:** [github.com/ho92ms](https://github.com/ho92ms)

---

*Last updated: December 2025*
