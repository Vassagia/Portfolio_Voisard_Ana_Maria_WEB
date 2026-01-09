# Arborescence du projet — Portfolio Ana-Maria WEB

Ce document décrit la structure complète du projet.  
Il sert de **référence** pour retrouver les fichiers et comprendre le rôle de chaque dossier.

---

## Structure générale

Portfolio_Voisard_Ana_Maria_WEB/
├─ .idea/
│ ├─ inspectionProfiles/
│ ├─ vcs.xml
│ └─ workspace.xml
├─ docs/
│ ├─ M_00_intro.md
│ ├─ M_01_arborescence.md
│ ├─ M_02_commits.md
│ ├─ M_03_css.md
│ ├─ M_04_bugs_et_solutions.md
│ └─ M_05_checklist_projet.md
├─ src/
│ └─ assets/
│ ├─ css/
│ │ ├─ base.css
│ │ ├─ layout.css
│ │ ├─ pages.css
│ │ ├─ reset.css
│ │ └─ variables.css
│ ├─ fonts/
│ │ ├─ inter-v20-latin-700.woff2
│ │ └─ inter-v20-latin-regular.woff2
│ ├─ icons/
│ │ ├─ github.svg
│ │ └─ linkedin.svg
│ └─ img/
│ ├─ cover.jpg
│ ├─ landing.jpg
│ ├─ timehive.jpg
│ └─ tricorder.jpg
├─ .gitignore
├─ contact.html
├─ cv.html
├─ index.html
├─ projets.html
└─ README.md


---

## Détail dossier par dossier

### `.idea/`
Dossier automatique créé par WebStorm.  
Contient la configuration de l’IDE (projet, VCS, préférences).  
**À ne pas modifier manuellement**.

### `docs/`
Documentation du projet:
- `M_00_intro.md` : présentation du projet
- `M_01_arborescence.md` : structure complète (ce fichier)
- `M_02_commits.md` : suivi de l’historique Git
- `M_03_css.md` : organisation CSS + bonnes pratiques
- `M_04_bugs_et_solutions.md` : problèmes rencontrés + correctifs
- `M_05_checklist_projet.md` : checklist d’auto-évaluation

### `src/assets/css/`
Feuilles de style du site :
- `reset.css` : base neutre navigateur
- `variables.css` : polices locales + variables (couleurs, espaces, radius)
- `base.css` : typographie, boutons, liens, accessibilité
- `layout.css` : structure générale + responsive
- `pages.css` : styles spécifiques (projets/contact/CV) + dark mode

### `src/assets/fonts/`
Polices locales (Inter):
- regular 400
- bold 700

### `src/assets/icons/`
Icônes SVG (LinkedIn / GitHub).

### `src/assets/img/`
Images utilisées (hero + projets).

### Pages HTML (racine)
Les pages visibles par l’utilisateur sont à la racine du projet:
- `index.html`
- `cv.html`
- `projets.html`
- `contact.html`
