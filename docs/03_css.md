# Organisation CSS

## Ordre de chargement (toutes les pages)

1. `reset.css`
2. `variables.css`
3. `base.css`
4. `layout.css`
5. `pages.css`

## Rôle des fichiers

- `reset.css` : base propre (marges/paddings/box-sizing)
- `variables.css` : variables globales + polices locales (Inter)
- `base.css` : typographie, boutons, liens, focus clavier, utilitaires
- `layout.css` : topbar, hero, sections, footer + responsive principal
- `pages.css` : styles spécifiques pages + dark mode + cartes projets

## Dark mode
- Implémenté via `@media (prefers-color-scheme: dark)`
- Ajustement des couleurs de fond, textes, titres, cartes, topbar/footer
