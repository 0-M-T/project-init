# project-init 🚀

![project-init banner](banner.jpg)

> **Autonomous AI-agent workflow skill** for initializing production-ready software projects with interactive discovery interviews, GitHub prior-art search, automated design systems, and code graph mapping.

Available languages: **[English](SKILL.en.md)** | **[Français](SKILL.fr.md)**  
Compatible with **Claude Code**, **Google Antigravity**, **Cursor**, **Codex**, and **OpenCode**.

---

## What It Does / Fonctionnalités

When triggered, your AI agent automatically executes a battle-tested 5-phase onboarding protocol:

1. **Phase 0 — Discovery Interview (Interactive Q&A)**  
   Asks targeted multiple-choice questions (purpose, target users, tech stack constraints, deployment/hosting, local directory structure) before touching the codebase.
2. **Phase 0.5 — GitHub State-of-the-Art Scan**  
   Searches public GitHub repositories for proven open-source packages, architectures, and solved patterns. Follows YAGNI principles to determine what to reuse versus build from scratch.
3. **Phase 1 — Git & Documentation Scaffolding**  
   Initializes `git`, writes strict `.gitignore` rules, generates a structured `README.md`, and deposits a session-level `AGENTS.md` context file.
4. **Phase 2 — Co-Designed Brand Identity & Assets**  
   Offers 3 geometric SVG logo concepts tested at 16 px and monochrome. Upon selection, exports:
   - **4 structural layouts**: Isotype / Favicon, Wordmark, Horizontal Lockup, Vertical Lockup.
   - **4 colorways**: Dark mode, Light mode, Monochrome White, Monochrome Black.
   - **Full size grid**: 16, 32, 48, 64, 96, 128, 192, 256, 512 px + OpenGraph social preview.
   - **Offline design tokens**: `tokens.json` & `tokens.css` with zero CDN dependencies.
5. **Phase 3 & 4 — Baseline Quality & Code Graph**  
   Configures linting tools, test harnesses, and runs an initial AST graph extraction (`graphify`) for instant structural awareness.

---

## ⚡ 1-Prompt Setup for Your AI Agent (English)

Paste this prompt into your AI assistant session (**Claude Code**, **Antigravity**, or **Cursor**):

```text
Install the 'project-init' skill into my dev environment by following these steps:

1. Detect where my agent skills/rules are stored (e.g., ~/.claude/skills/, ~/.gemini/antigravity/skills/, or .cursor/rules/).
2. Create a folder named 'project-init/' in that directory.
3. Fetch or copy the SKILL.en.md (renamed to SKILL.md) from https://github.com/0-M-T/project-init into that folder.
4. Add a rule to my global instructions (CLAUDE.md or AGENTS.md):
   "Whenever creating or scaffolding a new project, strictly follow the 'project-init' skill starting with Phase 0 (multiple-choice discovery questions)."
5. Confirm completion in 2 concise lines.
```

---

## ⚡ Prompt d'installation en 1 clic (Français)

Copiez et collez ce prompt dans la session de votre agent IA :

```text
Installe le skill 'project-init' dans mon environnement de développement en suivant ces instructions :

1. Détecte où sont stockés mes skills IA (ex: ~/.claude/skills/, ~/.gemini/antigravity/skills/ ou .cursor/rules/).
2. Crée le dossier 'project-init/' à cet endroit.
3. Télécharge ou copie le fichier SKILL.fr.md (renommé en SKILL.md) depuis https://github.com/0-M-T/project-init dans ce dossier.
4. Ajoute une règle globale dans mes instructions d'agent (CLAUDE.md ou AGENTS.md) :
   "À chaque création d'un nouveau projet, applique obligatoirement le skill 'project-init' en commençant par la Phase 0 (questions à choix multiples pour cadrer le projet)."
5. Confirme-moi l'installation en 2 lignes.
```

---

## 🛠️ Manual Installation / Installation manuelle

### Option A — English
```bash
git clone https://github.com/0-M-T/project-init.git ~/.claude/skills/project-init
cp ~/.claude/skills/project-init/SKILL.en.md ~/.claude/skills/project-init/SKILL.md
```

### Option B — Français
```bash
git clone https://github.com/0-M-T/project-init.git ~/.claude/skills/project-init
cp ~/.claude/skills/project-init/SKILL.fr.md ~/.claude/skills/project-init/SKILL.md
```

---

## Usage

Simply run:
```text
/project-init
```
Or tell your agent:
> *"Create a new project for my CLI backup utility..."* / *"Crée un nouveau projet pour mon outil de..."*

---

## License

MIT © [0-M-T](https://github.com/0-M-T)
