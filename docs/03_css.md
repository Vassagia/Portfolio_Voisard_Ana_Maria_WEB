
---

##  Fichier : `docs/03_css.md`


# Documentation CSS 

Ce document explique **l’organisation des fichiers CSS**,  
leurs rôles respectifs, la **palette de couleurs**,  
et les **bonnes pratiques** à suivre pour garder le code propre et cohérent.

---

## Structure des fichiers CSS

```

src/assets/css/
│
├─ _variables.css    → variables globales (couleurs, polices, tailles)
├─ _reset.css        → réinitialisation du style par défaut des navigateurs
├─ base.css          → styles généraux (texte, boutons, liens)
└─ layout.css        → disposition des sections, grilles, topbar, hero, etc.

````

Les fichiers qui commencent par un **underscore `_`** sont dits *“partiels”* :  
ils servent de **fichiers utilitaires** qu’on peut réutiliser ou importer ailleurs.

---

##  1. `_variables.css`

> Ce fichier contient **toutes les variables globales** du site :  
> couleurs, tailles, bordures, espacements, etc.  
> Cela permet de modifier rapidement tout le design sans toucher 20 fichiers.

### Exemple :
```css

:root {
  --emerald: #006d5b;      /* Couleur principale (vert émeraude) */
  --orange: #ff4500;       /* Accent (orange feu) */
  --beige: #f5f5f0;        /* Fond clair */
  --dark: #2e2e2e;         /* Fond sombre */
  --gray: #9e9e9e;         /* Texte secondaire */

  --radius: 10px;          /* Rayon standard des bords */
  --spacing: 16px;         /* Espacement de base */
  --transition: 0.3s ease; /* Transition fluide */
}
````

 Pour utiliser une variable :

```css
background-color: var(--emerald);
```

---

##  2. `_reset.css`

> Sert à **supprimer les styles par défaut du navigateur**
> (ex. marges des `<body>`, tailles des `<h1>`, etc.)

### Exemple :

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: "Segoe UI", Arial, sans-serif;
  background-color: var(--beige);
  color: var(--dark);
}
```

Ce fichier est **toujours chargé en premier**,
pour que tous les navigateurs partent d’une base identique.

---

## 3. `base.css`

> Contient les styles **généraux et récurrents** :
> titres, paragraphes, liens, boutons, listes, etc.

### Exemple :

```css
h1, h2, h3 {
  font-weight: 700;
  color: var(--dark);
}

a {
  color: var(--emerald);
  text-decoration: none;
  transition: color var(--transition);
}

a:hover {
  color: var(--orange);
}

button {
  border-radius: var(--radius);
  padding: 10px 16px;
  cursor: pointer;
}
```

Tous les fichiers CSS spécialisés (`layout.css`, `hero.css`, etc.) héritent de ces bases.

---

## 4. `layout.css`

> Sert à gérer la **mise en page générale** :
> position des sections, header, footer, grilles, flexbox, etc.

### Exemple :

```css
.container {
  width: min(1200px, 90%);
  margin: 0 auto;
}

.section {
  padding: 40px var(--spacing);
}

.grid {
  display: grid;
  gap: var(--spacing);
}
```

---

## Palette de couleurs

| Nom           | Variable    | Couleur    | Usage principal                    |
| :------------ | :---------- | :--------- | :--------------------------------- |
| Vert émeraude | `--emerald` | 🟩 #006d5b | Couleur principale                 |
| Orange feu    | `--orange`  | 🟧 #ff4500 | Accent / boutons                   |
| Beige doux    | `--beige`   | 🟨 #f5f5f0 | Fond clair                         |
| Gris foncé    | `--dark`    | ⚫ #2e2e2e  | Texte ou fond sombre               |
| Gris neutre   | `--gray`    | ⚪ #9e9e9e  | Sous-titres / éléments secondaires |

 Cette palette peut être ajustée selon ton goût, mais **reste cohérente sur tout le site**.

---

## Bonnes pratiques CSS

1. **Toujours utiliser les variables** (`var(--nom)`) au lieu des codes directs.
   → plus facile à modifier plus tard.
2. **Nommer les classes logiquement**

    * Exemple : `.hero__image`, `.hero__content`, `.topbar__nav`
3. **Séparer la logique du style** :

    * HTML = contenu
    * CSS = apparence
4. **Tester le responsive** après chaque grande modification (sur mobile et desktop).
5. **Commenter** ton CSS pour t’y retrouver :

   ```css
   /* ===== Section Hero ===== */
   ```
6. **Toujours enregistrer (Ctrl + S)** avant de tester dans le navigateur.
7. **Committer** quand ton style est stable :

   ```
   style: mise à jour layout et couleurs
   ```

---

## Rappel de l’ordre d’importation CSS

Dans le fichier HTML (`index.html`), l’ordre recommandé est :

```html
<link rel="stylesheet" href="../assets/css/_reset.css">
<link rel="stylesheet" href="../assets/css/_variables.css">
<link rel="stylesheet" href="../assets/css/base.css">
<link rel="stylesheet" href="../assets/css/layout.css">
```

Cet ordre garantit que :

* `_reset.css` nettoie la base
* `_variables.css` définit les couleurs
* `base.css` applique les styles généraux
* `layout.css` gère la structure finale

---

## Exemple de commit liés au CSS

| Type     | Message de commit                            | Description                              |
| :------- | :------------------------------------------- | :--------------------------------------- |
| `style:` | `style: ajouter _variables.css avec palette` | Création du fichier de variables         |
| `style:` | `style: mise en page du hero`                | Ajout du design principal                |
| `style:` | `style: améliorer la lisibilité du texte`    | Ajustement de la typo                    |
| `fix:`   | `fix: corriger marge du footer`              | Correction d’un problème de mise en page |

---

 **Conseil personnel :**
Quand je modifies mon CSS, je note toujours ce que je fais dans la doc.
Exemple :

> “Le 21/10, j’ai ajusté la couleur de fond du hero (plus foncé).”
> Ça t’évitera d’oublier les petits changements visuels.

---


 
