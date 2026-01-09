# Projet Portfolio Ana-Maria (Web)

**Objectif :** créer un site personnel pour présenter mon profil, mes compétences et quelques projets.  
**Outils utilisés :** WebStorm, HTML5, CSS3, Git, GitHub, GitDesktop.

---

## Pages du site (racine du projet)

- `index.html` : accueil (Hero + À propos)
- `cv.html` : CV (profil, compétences, expériences, formations)
- `projets.html` : projets sous forme de cartes
- `contact.html` : formulaire de contact (simulation locale)

---

## Structure du projet (résumé)

- `src/` : contient les ressources du site (CSS, images, polices, icônes)
- `src/assets/css/` : feuilles de style
- `src/assets/img/` : images du site
- `src/assets/fonts/` : polices locales (Inter en woff2)
- `src/assets/icons/` : icônes (SVG)
- `docs/` : documentation de suivi du projet
- `.idea/` : configuration WebStorm (auto)

---

## Points techniques réalisés

- HTML sémantique (`header`, `nav`, `main`, `section`, `footer`, `article`, `figure`)
- Responsive (Grid + media queries)
- Variables CSS (couleurs, polices, espacements)
- Accessibilité:
    - lien d’évitement (`skip-link`)
    - focus clavier visible (`:focus-visible`)
    - texte lecteur d’écran (`.sr-only`)
- Mode sombre sur certaines pages via `prefers-color-scheme: dark` (dans `pages.css`)
- Ressources locales (pas de CDN): polices + images + icônes

---

## Ordre de chargement CSS (dans chaque HTML)

1. `reset.css`
2. `variables.css`
3. `base.css`
4. `layout.css`
5. `pages.css`

Cet ordre garantit que la base est propre, que les variables sont disponibles, puis que la structure et les styles spécifiques s’appliquent correctement.
