
---

## Fichier : `docs/04_bugs_et_solutions.md`



````markdown
#  Bugs rencontrés et solutions appliquées

Ce document répertorie tous les **problèmes rencontrés pendant le développement**  
et les **solutions apportées**.  
Chaque section décrit :
1. le **symptôme** ou le message d’erreur  
2. la **cause probable**  
3. la **solution appliquée**  
4. éventuellement **ce que j’ai appris**

---

## Format d’entrée 

> Date : JJ.MM.AAAA  
> **Problème :** phrase courte décrivant l’erreur  
> **Détails :** description ou message d’erreur complet  
> **Cause :** pourquoi cela s’est produit  
> **Solution :** comment j’ai corrigé  
> **Appris :** leçon retenue pour ne plus refaire la même erreur

---

## Exemple 1 — Chemin d’image incorrect

**Date :** 21.10.2025  
**Problème :** L’image d’accueil ne s’affichait pas sur la page index.  
**Détails :** L’élément `<img>` apparaissait vide dans le navigateur.  
**Cause :** Le chemin relatif était faux (`../img/landing.jpg` au lieu de `../assets/img/landing.jpg`).  
**Solution :** Correction du chemin dans `index.html` :  
```html
<img src="../assets/img/landing.jpg" alt="Photo de Ana-Maria">
````

**Appris :** toujours vérifier le dossier exact dans l’arborescence (`assets/img`).

---

## Exemple 2 — Fichier CSS non appliqué

**Date :** 22.10.2025
**Problème :** Le style ne s’appliquait pas sur la page.
**Détails :** Les couleurs et marges n’étaient pas visibles.
**Cause :** Mauvais ordre de chargement des fichiers CSS dans `<head>`.
**Solution :** Réorganiser l’ordre :

```html
<link rel="stylesheet" href="../assets/css/_reset.css">
<link rel="stylesheet" href="../assets/css/_variables.css">
<link rel="stylesheet" href="../assets/css/base.css">
<link rel="stylesheet" href="../assets/css/layout.css">
```

**Appris :** toujours charger `_reset.css` et `_variables.css` en premier.

---

## Exemple 3 — Git ne détecte pas les changements

**Date :** 23.10.2025
**Problème :** Les fichiers modifiés dans `docs/` n’apparaissaient pas dans la liste des commits.
**Cause :** Le dossier `docs` n’avait pas été ajouté au suivi Git.
**Solution :**

```bash
git add docs/
git commit -m "docs: mise à jour documentation"
```

**Appris :** bien vérifier la liste des fichiers “staged” avant de committer.

---

## Exemple 4 — Mauvais rendu sur mobile

**Date :** 24.10.2025
**Problème :** Le texte dépassait de l’écran sur téléphone.
**Cause :** Oubli de la balise viewport dans `<head>`.
**Solution :**

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**Appris :** toujours inclure cette balise dans chaque page HTML.

---

## Conseils de gestion des bugs

1.  Reproduire le problème avant d’essayer de le corriger.
2.  Lire attentivement les messages d’erreur (ils contiennent souvent la solution).
3.  Noter immédiatement la solution ici dès que le bug est réglé.
4.  Faire un **commit clair** :

   ```
   fix: corriger lien image accueil
   ```
5.  À la fin du projet, ce fichier devient ta **bibliothèque de solutions** !

---

## Exemple de commit de correction

| Type    | Message                                  | Description                |
| :------ | :--------------------------------------- | :------------------------- |
| `fix:`  | `fix: corriger chemin image d’accueil`   | Correction d’un bug simple |
| `fix:`  | `fix: rétablir affichage CSS sur mobile` | Ajustement responsive      |
| `docs:` | `docs: ajouter bug Git + solution`       | Mise à jour de ce fichier  |

---
