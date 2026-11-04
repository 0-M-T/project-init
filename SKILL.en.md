---
name: project-init
description: "Initializes a new software project according to modern production standards: mandatory discovery Q&A interview, GitHub state-of-the-art prior-art scan, clean Git scaffolding, complete brand identity kit (4 logo layout types x 4 colorways from 16 to 512 px, zero-CDN CSS/JSON design tokens), baseline lint/testing, and initial code knowledge graph mapping."
---

# /project-init

Comprehensive AI-assisted project initialization protocol.

---

## Phase 0 — Discovery & Interactive Q&A (Blocking)

Ask discovery questions using the environment's native multiple-choice question tool (`ask_question` in Google Antigravity, or structured A/B/C/D choices in Claude Code / Cursor). Never dump a raw wall of text without selectable options.

Questions to cover:
1. **Pitch & Problem** : 1-sentence definition of what the project does and what problem it solves.
2. **Target Audience & Context** : User profile (Personal use, Recruiters/portfolio, Internal homelab, Public SaaS/product).
3. **Tech Stack & Constraints** : Required language/framework and hard constraints (100% offline, zero-CDN, air-gapped, SQLite, etc.).
4. **Hosting & Deployment** : Local CLI only, Docker container, VPS, or reverse-proxy with authentication.
5. **Target Directory** : Project name and exact local folder path.

Do not proceed to code creation until the user confirms their choices.

---

## Phase 0.5 — GitHub Prior Art & State of the Art

Once answers are collected, before writing code:

1. **GitHub Ecosystem Search** :
   - Search public open-source repos tackling a similar problem (`gh search repos`, web search, or API).
   - Identify: lightweight reusable libraries, architecture references, pitfalls already solved by others.
2. **Comparative Summary (3-5 bullet points)** :
   - Nearest existing projects (stars, recent maintenance, license).
   - What to reuse or take inspiration from (data models, patterns, algorithms).
   - What justifies custom implementation (unique value, offline constraints, project specifics).
3. **User Validation** :
   - Present a concise summary for validation (YAGNI principle: do not reinvent existing wheels).

---

## Phase 1 — Clean Git & Scaffolding

1. Create target directory.
2. Initialize Git: `git init -b main`.
3. Generate strict `.gitignore` tailored to the stack (exclude `.venv`, `node_modules`, `*.log`, `.env`, secrets, `.DS_Store`).
4. Create minimal `README.md`:
   - Title and 1-sentence pitch from Phase 0.
   - Tech stack overview.
   - Quickstart commands (setup, dev, test).
5. Create local `AGENTS.md` (session rules, architecture notes, recurring agent commands).

---

## Phase 2 — Visual Identity & Brand Co-Design

Mandatory user inclusion. No unilateral design decisions.
Strict adherence to **Zero-CDN / 100% Offline** rules (system fonts or local WOFF2, zero third-party network calls).

1. **Interactive Style Consultation** (via question tool / multiple choice) :
   - Palette & Mood: Dark Tech minimalist, Neon studio / cyberpunk, Clean monochrome, or High-contrast vibrant.
   - Mark Type: Geometric monogram, Domain pictogram, Pure abstract symbol, or Typographic wordmark.
2. **Generate 3 Distinct SVG Logo Concepts** :
   - Save 3 standalone SVGs in `docs/marque/kit/concepts/` (`concept-a.svg`, `concept-b.svg`, `concept-c.svg`).
   - Validate each concept at 16 px (favicon), in one-color monochrome, and on dark backgrounds.
   - Present the 3 concepts to the user and wait for their choice.
3. **Complete Brand Kit Exports (Multi-Type & Multi-Size)** :
   - **4 Vector Layout Types (Pure SVG)** :
     - **Isotype / Favicon**: Standalone compact symbol (app icon, favicon, avatar).
     - **Wordmark**: Typographic logotype (headers, footers).
     - **Horizontal Lockup**: Symbol + text side-by-side (web navbars, headers).
     - **Vertical Lockup**: Symbol centered above text (splash screens, cards, posters).
   - **4 Colorways per Layout** :
     - Dark (accent + white on dark background).
     - Light (accent + dark on light background).
     - Monochrome 100% white.
     - Monochrome 100% black.
   - **Multi-Resolution Asset Grid (PNG & SVG)** :
     - Favicons & Web: 16, 32, 48 px.
     - App Icons & Mobile: 64, 96, 128, 192, 256, 512 px.
     - Social & Banners: 1200x630 (OpenGraph).
   - **Design Tokens** :
     - Generate `docs/marque/tokens.json` and `docs/marque/tokens.css` (variables `--bg-main`, `--text-main`, `--accent`, `--radius`).
     - Write `docs/marque/charte-graphique.md`.

---

## Phase 3 — Baseline Quality & Testing Harness

1. Configure linting and formatting:
   - Python: Ruff (`pyproject.toml` or `ruff.toml`).
   - JS/TS: Biome or ESLint + Prettier.
2. Create smoke test / baseline verification script:
   - Python: `verify_goal.py` or `pytest`.
   - Node: `npm test` script.
   - Shell: `test.sh` with `set -euo pipefail`.
3. If containerized: generate minimal `docker-compose.yml`.

---

## Phase 4 — Initial Code Graph & Verification

1. Run initial code knowledge graph mapping (if `graphify` is installed):
   ```bash
   command -v graphify >/dev/null 2>&1 && graphify . || true
   ```
2. Make the initial Git commit:
   ```bash
   git add .
   git commit -m "feat(init): initial scaffold, visual identity, and brand tokens"
   ```

---

## Session Communication Directives

- **Concise & Telegraphic** : Zero pleasantries or conversational filler.
- **Diff-Oriented** : Code and short bullet points speak for themselves.
