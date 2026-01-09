# Documentation CSS — Portfolio Ana-Maria

Ce document explique l’organisation des fichiers CSS, leur rôle et les bonnes pratiques du projet.

---

## Structure des fichiers CSS

src/assets/css/
├─ reset.css → neutralise les styles par défaut
├─ variables.css → polices locales + variables globales
├─ base.css → styles généraux (typo, boutons, liens, accessibilité)
├─ layout.css → structure (topbar, hero, sections, footer) + responsive
└─ pages.css → styles spécifiques (projets, contact, CV) + dark mode


---

## 1) `variables.css`
Contient:
- `@font-face` pour charger **Inter** en local (woff2)
- Variables globales `:root` :
    - couleurs (émeraude, orange, gris, beige, dark)
    - polices (`--font-body`, `--font-heading`)
    - espacements (`--space-sm`, `--space`, `--space-lg`)
    - arrondis (`--radius`)

But: éviter les valeurs “en dur” partout, garder une charte cohérente.

---

## 2) `reset.css`
Base minimale pour partir propre:
- `* { margin:0; padding:0; box-sizing:border-box; }`
- images responsive
- listes sans puces
- liens neutres

Important: `base.css` redéfinit ensuite les liens (couleur émeraude), car `reset.css` les met volontairement neutres.

---

## 3) `base.css`
Styles communs à toutes les pages:
- typographie générale (`body`, titres)
- `.container` (largeur + centrage)
- boutons `.btn` + variantes
- liens `a:hover`, `a:visited`
- accessibilité :
    - `:focus-visible` (clavier)
    - `.skip-link` (aller au contenu)
    - `.sr-only` (lecteurs d’écran)

---

## 4) `layout.css`
Mise en page globale:
- `.topbar` (flex)
- `.main-nav ul` (flex)
- `.hero` (grid)
- `.section`, `.site-footer`

Responsive:
- ≥600px : topbar/sections plus aérées
- ≥768px : hero en 2 colonnes
- ≥1024px : layout plus large
- ≥1440px : confort grand écran

---

## 5) `pages.css`
Spécifique selon la page:
- projets: `.cards`, `.card`, images, hover + grille responsive
- contact: formulaire (focus, inputs)
- cv: listes et titres
- dark mode: `@media (prefers-color-scheme: dark)` (ajuste texte + cartes)

---

## Ordre d’importation CSS (dans les HTML)
```html
<link rel="stylesheet" href="src/assets/css/reset.css">
<link rel="stylesheet" href="src/assets/css/variables.css">
<link rel="stylesheet" href="src/assets/css/base.css">
<link rel="stylesheet" href="src/assets/css/layout.css">
<link rel="stylesheet" href="src/assets/css/pages.css">
