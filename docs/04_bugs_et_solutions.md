# Bugs & solutions

## 1) Titres illisibles en dark mode
**Symptôme :** h2/h3 peu visibles sur fond sombre.  
**Cause :** styles de titres définis en base, surchargés/insuffisants en dark mode.  
**Solution :** règles explicites en `pages.css` dans `prefers-color-scheme: dark` avec sélecteurs plus spécifiques.

## 2) Cartes projets non uniformes
**Symptôme :** hauteurs différentes selon la longueur du texte/bouton.  
**Cause :** hauteur dépend du contenu, pas de structure “pousse le bouton en bas”.  
**Solution :**
- `li` en flex
- `.card` en grid avec zone texte extensible
- image avec hauteur fixe + object-fit

## 3) Boutons inactifs
**Symptôme :** boutons gris et non cliquables.  
**Cause :** attribut `disabled` sur `<button>`.  
**Solution :** remplacer par `<a class="btn ...">` pointant vers GitHub.

## 4) Validation HTML (warnings)
**Symptôme :** trailing slash sur meta + roles ARIA redondants.  
**Solution :** retirer `/` sur `<meta>` et supprimer `role="banner"` / `role="contentinfo"` inutiles.  

