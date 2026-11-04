---
name: project-init
description: "Initialise un nouveau projet logiciel selon les standards modernes : interview cadrage Q&A native, état de l'art GitHub (Phase 0.5), scaffolding Git propre, kit de marque complet (4 types de logos x 4 variantes couleur de 16 à 512 px, tokens CSS/JSON, zéro CDN), hygiène/lint et cartographie initiale du code."
---

# /project-init

Protocole complet d'initialisation de projet assisté par IA.

---

## Phase 0 — Cadrage & Interview Q&A (Bloquant)

Poser impérativement les questions de cadrage via l'outil natif de questions à choix multiples de l'environnement (`ask_question` sous Antigravity, ou questions structurées à options A/B/C/D sous Claude Code/Cursor). Ne jamais déverser un bloc de texte brut sans options.

Questions à poser :
1. **Pitch & Problème** : Définition du problème résolu en 1 phrase.
2. **Cible & Contexte** : Profil utilisateur (Usage perso, Recruteur, Interne, Grand public).
3. **Stack & Contraintes** : Technologies imposées et contraintes (100% offline, zéro CDN, SQLite, etc.).
4. **Hébergement & Déploiement** : Local seul, Docker, VPS, ou reverse-proxy avec auth.
5. **Dossier cible** : Nom du projet et chemin exact du répertoire local.

Attendre impérativement les réponses avant d'engager la suite.

---

## Phase 0.5 — État de l'Art GitHub & Écosystème Existant

Une fois les réponses obtenues, avant d'écrire le moindre code :

1. **Recherche sur GitHub** :
   - Chercher les dépôts open-source résolvant un problème proche (`gh search repos`, web search ou API).
   - Identifier : bibliothèques légères réutilisables, architectures de référence, pièges évités.
2. **Synthèse comparative (3 à 5 puces)** :
   - Projets existants les plus proches (stars, activité récente, licence).
   - Ce qu'on réutilise ou dont on s'inspire (patterns, schémas).
   - Ce qui justifie le développement sur-mesure (valeur ajoutée, spécificité, offline).
3. **Validation utilisateur** :
   - Présenter brièvement la synthèse pour validation (principe YAGNI : ne pas réinventer la roue).

---

## Phase 1 — Scaffolding Git & Rangement Propre

1. Créer le dossier cible validé.
2. Initialiser Git : `git init -b main`.
3. Écrire le `.gitignore` adapté à la stack (exclure `.venv`, `node_modules`, `*.log`, `.env`, secrets, `.DS_Store`).
4. Créer le `README.md` minimal :
   - Titre, pitch en 1 phrase issu du cadrage.
   - Stack technique.
   - Commandes rapides (démarrage, tests).
5. Créer `AGENTS.md` local (instructions de session pour les agents IA, architecture, commandes récurrentes).

---

## Phase 2 — Identité Visuelle & Co-conception de Marque

Inclusion obligatoire de l'utilisateur dans la boucle décisionnelle. Zéro décision graphique unilatérale.
Respect strict de la règle **Zéro CDN / 100% Hors-ligne** (polices système ou locales WOFF2, zéro requête réseau externe).

1. **Consultation interactive sur le style** (via outil de questions / choix multiples) :
   - Palette & Ambiance : Dark Tech minimaliste, Studio néon/cyberpunk, Monochromatique sobre, ou Couleurs vives.
   - Type de marque : Monogramme géométrique, Pictogramme métier, Symbole abstrait pur, ou Wordmark typographique.
2. **Génération de 3 concepts de logos SVG distincts** :
   - Créer 3 variantes SVG pures dans `docs/marque/kit/concepts/` (`concept-a.svg`, `concept-b.svg`, `concept-c.svg`).
   - Tester chaque concept à 16 px (favicon), en monochrome et sur fond sombre.
   - Présenter les 3 concepts à l'utilisateur et lui demander de choisir.
3. **Validation & Exports du kit de marque complet (multi-types & multi-tailles)** :
   - **4 types vectoriels (SVG purs)** :
     - **Isotype / Favicon seul** : symbole épuré compact (app icon, favicon, avatar).
     - **Wordmark seul** : logotype typographique (titres, footer).
     - **Lockup horizontal** : symbole + texte alignés en ligne (header web, barres de navigation).
     - **Lockup vertical** : symbole centré au-dessus du texte (cartes, splash screens).
   - **Variantes chromatiques pour chaque type** :
     - Dark (accent + blanc sur fond sombre).
     - Light (accent + noir sur fond clair).
     - Monochrome 100% blanc.
     - Monochrome 100% noir.
   - **Découpage multi-résolutions (PNG & SVG)** :
     - Favicons & Web : 16, 32, 48 px.
     - App Icons & Mobile : 64, 96, 128, 192, 256, 512 px.
     - Social & Bannières : 1200x630 (OpenGraph).
   - **Design Tokens** :
     - Produire `docs/marque/tokens.json` et `docs/marque/tokens.css` (variables `--bg-main`, `--text-main`, `--accent`, `--radius`).
     - Rédiger `docs/marque/charte-graphique.md`.

---

## Phase 3 — Qualité, Hygiène & Vérification

1. Poser les outils de lint/format selon la stack :
   - Python : Ruff (`pyproject.toml` ou `ruff.toml`).
   - JS/TS : Biome ou ESLint + Prettier.
2. Créer un script de smoke test / vérification de baseline :
   - Python : `verify_goal.py` ou `pytest`.
   - Node : script `npm test` fonctionnel.
   - Shell : script `test.sh` avec `set -euo pipefail`.
3. Si conteneurisation : créer un `docker-compose.yml` minimaliste.

---

## Phase 4 — Cartographie Initiale & Documentation

1. Lancer la cartographie du code (si `graphify` est installé) :
   ```bash
   command -v graphify >/dev/null 2>&1 && graphify . || true
   ```
2. Effectuer le premier commit Git :
   ```bash
   git add .
   git commit -m "feat(init): squelette initial, identite visuelle et charte"
   ```

---

## Directives Locales de Session

- **Réponses concises et denses** : style direct et télégraphique. Zéro blabla d'introduction ou de conclusion.
- **Diffs ciblés** : le code parle de lui-même.
