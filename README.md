# Digital Garden (System Root)

![Build Status](https://img.shields.io/github/actions/workflow/status/cjalanano-dev/zeta-space/deploy.yml?label=Build&style=flat-square)
![Quartz](https://img.shields.io/badge/Built%20With-Quartz%20v4-FF2E88?style=flat-square)
![Status](https://img.shields.io/badge/Status-Online-success?style=flat-square)

> "The faint ink is better than the best memory."

This repository hosts the source code for my personal **Digital Archive**, a public-facing knowledge base and engineering portfolio. Unlike a traditional linear blog, this site utilizes bi-directional linking to create a network of interconnected thoughts and documentation.

**[Live Deployment](https://cjalanano-dev.github.io/zeta-space/)**

---

## Architecture

This project implements a **GitOps** workflow to publish local Obsidian notes to the web.

1.  **Input:** Content is written locally in **Obsidian** (Markdown) within a strictly typed schema.
2.  **Processing:** **Quartz v4** (a static site generator based on Node.js/TypeScript) parses the Markdown, resolves the Wiki-style links `[[ ]]`, and generates a dependency graph.
3.  **Output:** Static HTML is built and optimized for performance (Lighthouse score: 100).
4.  **Deployment:** **Netlify** automatically detects pushes to `main`, triggers the build command (`npx quartz build`), and distributes the assets via their global Edge Network.

## 🛠 Tech Stack

* **Core Engine:** [Quartz v4](https://quartz.jzhao.xyz/)
* **Language:** TypeScript / TSX
* **Content Management:** Obsidian (Local Filesystem)
* **Styling:** SCSS / Custom Components
* **Hosting:** GitHub Pages

## Content Structure

The vault is organized into specific sectors to maintain separation of concerns:

* `Projects/` - Documentation for active coding work.
* `TIL/` - "Today I Learned". Atomic notes on C#, Python, and Algorithms.
* `Journal/` - Reflections and academic life.

## License
Content is © 2026 Carlos James. Source code is licensed under the MIT License.