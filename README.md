# Projet personnel — Portfolio Ana-Maria (Module 113)

Site personnel réalisé en **HTML5 + CSS3**, versionné avec **Git/GitHub** et publié via **GitHub Pages**.  
Objectif: présenter mon profil, mon CV et quelques projets.

- **Site en ligne**: https://vassagia.github.io/Portfolio_Voisard_Ana_Maria_WEB/
- **Dépôt GitHub**: https://github.com/Vassagia/Portfolio_Voisard_Ana_Maria_WEB

---

## 1) Concept, public cible, objectifs

### Concept
Un portfolio clair, accessible et responsive, orienté “profil + preuves” (CV + projets), avec un style sobre et une identité couleur cohérente (émeraude/orange).

### Public cible
- Recruteurs / entreprises (stage, apprentissage, premier emploi)
- Enseignant (validation des exigences techniques)
- Toute personne voulant consulter mon profil rapidement

### Objectifs
- Mettre en pratique **structure HTML sémantique**, **CSS moderne** (Grid/Flex), **responsive mobile-first**
- Démontrer une organisation propre du projet (assets locaux, CSS structuré, commits)
- Valider la qualité (W3C, accessibilité, performance)

---

## 2) Pages du site (à la racine)

- `index.html` : Accueil (Hero + section “À propos”)
- `cv.html` : CV (profil, compétences, expériences, formations, langues, intérêts)
- `projets.html` : Projets sous forme de cartes (liens vers GitHub)
- `contact.html` : Formulaire de contact (simulation locale)

---

## 3) Structure du projet

Arborescence principale:

- `src/assets/css/`
    - `reset.css` : reset minimal
    - `variables.css` : variables globales + polices locales
    - `base.css` : styles de base (typo, liens, boutons, accessibilité)
    - `layout.css` : structure (topbar, hero, sections, footer, responsive)
    - `pages.css` : styles spécifiques par page (cartes projets, formulaire, dark mode)
- `src/assets/img/` : images (locales, optimisées)
- `src/assets/fonts/` : polices locales (Inter en `.woff2`)
- `src/assets/icons/` : icônes SVG (LinkedIn, GitHub)
- `docs/` : documentation détaillée du projet (intro, arborescence, commits, CSS, bugs/solutions, checklist)

---

## 4) Points techniques réalisés

### HTML
- Balises sémantiques: `header`, `nav`, `main`, `section`, `footer`, `article`, `figure`
- Hiérarchie des titres: **1 seul `h1` par page**, puis `h2`, `h3`, etc.
- Images avec attribut `alt` systématique

### CSS
- Variables CSS (couleurs, polices, espacements) dans `variables.css`
- Layout moderne: **Grid** (cartes) + **Flex** (topbar, actions)
- Interactions: `:hover`, `:focus-visible`, `:visited`
- Responsive: breakpoints utilisés (ex: 600px, 768px, 1024px)
- Mode sombre: `@media (prefers-color-scheme: dark)` (lisibilité + composants)

### Accessibilité (a11y)
- Lien d’évitement: `.skip-link`
- Focus clavier visible: `:focus-visible`
- Texte pour lecteurs d’écran: `.sr-only`

### Ressources locales
- Polices: locales dans `/fonts` (pas de CDN)
- Images: locales dans `/img`, optimisées

---

## 5) Ordre de chargement CSS dans chaque page

1. `reset.css`
2. `variables.css`
3. `base.css`
4. `layout.css`
5. `pages.css`

Cet ordre garantit: base propre → variables disponibles → styles globaux → layout → styles spécifiques.

---

## 6) Outils et méthodologie

- IDE: WebStorm
- Versioning: Git + GitHub + GitHub Desktop
- Déploiement: GitHub Pages
- Méthode: itérations courtes + commits réguliers (corrections, refactor CSS, accessibilité, dark mode, validations)

---

## 7) Tests et validations

### Validation HTML
- Outil: Nu Html Checker (W3C)
- Résultat: **aucune erreur / aucun warning** (après nettoyage)

### Validation CSS
- Outil: W3C CSS Validator
- Résultat: **aucune erreur**

### Performance (PageSpeed / Lighthouse)
- Mobile: Perf **90**, Accessibilité **95**, Bonnes pratiques **100**, SEO **91**
- Desktop: Perf **100**, Accessibilité **95**, Bonnes pratiques **100**, SEO **91**

### Compatibilité navigateurs
- Tests manuels: Firefox, Chrome, Edge (desktop)
- Vérification complémentaire: audit Lighthouse via PageSpeed

---

## 8) Difficultés rencontrées et solutions

- Uniformisation des cartes projets (hauteurs / images) → ajustements Grid + règles image
- Lisibilité du dark mode (titres, textes, boutons) → corrections de contraste + surcharges ciblées
- Validation W3C: suppression d’éléments inutiles/ambiguës (ex: roles redondants, slash sur void elements)

Détails complets: voir `docs/04_bugs_et_solutions.md`.

---

## 9) Améliorations possibles

- Ajouter de vraies pages “Détails” pour chaque projet (TimeHive, Mini-Tricorder)
- Ajouter un formulaire de contact réel (backend) ou un lien mailto sécurisé
- Ajouter plus de projets + captures + explications techniques (stack, difficultés, solutions)

---

## 10) Transparence sur l’usage d’IA

L’IA (ChatGPT et Claude) a été utilisée comme **assistant pédagogique**:
- clarification de concepts (HTML/CSS, accessibilité, responsive)
- aide au debug (cartes, hover, dark mode)
- amélioration de la documentation (structuration, checklist)

Tout le code a été relu, compris et adapté au projet.

---

## Auteur

Ana-Maria Voisard — ESIG (informatique de gestion)
