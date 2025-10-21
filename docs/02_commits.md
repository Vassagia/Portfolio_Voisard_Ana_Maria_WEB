
---

## Exemple complet — `docs/02_commits.md`


# Historique des commits

Ce fichier me sert à **suivre l’évolution du projet** étape par étape,  
avec des messages clairs, structurés et professionnels.  
Chaque commit représente une **petite étape terminée et fonctionnelle**.

---

##  Règle à suivre

>  **1 commit = 1 idée complète**  
> Je commit uniquement quand :
> - Mon code fonctionne sans erreur
> - L’étape est terminée
> - Je peux décrire clairement ce que j’ai fait en une phrase

---

##  Format des messages de commit

Je commence toujours par un **préfixe clair** selon le type de modification :

| Préfixe | Signification | Exemple |
|:--|:--|:--|
| `feat:` | nouvelle fonctionnalité | `feat(home): ajouter section hero` |
| `style:` | mise en forme / apparence | `style: ajuster couleurs et marges` |
| `fix:` | correction d’un bug | `fix: lien vers contact.html` |
| `docs:` | documentation uniquement | `docs: mise à jour arborescence.md` |
| `chore:` | maintenance ou configuration | `chore: initialiser Git + structure` |
| `assets:` | ajout d’images, polices, etc. | `assets: ajouter landing.jpg` |

---

##  Historique des commits

###  Étape 1 — Initialisation du projet


chore: initialiser Git + structure du projet


Création du dépôt, activation de Git dans WebStorm, mise en place des premiers dossiers.


### Étape 2 — Mise en place de la documentation


docs: créer dossier /docs et fichiers de base (.md)


Création des fichiers `00_intro.md` à `04_bugs_et_solutions.md`.



###  Étape 3 — Arborescence du projet


feat(structure): ajouter src/pages + assets + partials

Mise en place de la structure HTML/CSS/JS propre et logique.



### Étape 4 — Palette de couleurs


style: ajouter _variables.css avec palette émeraude/orange


Définition des variables CSS pour une charte visuelle cohérente.


###  Étape 5 — Première page HTML


feat(home): créer index.html avec base structure


Création de la page d’accueil avec titre et conteneurs.



### Étape 6 — Ajout du style de base


style: ajouter reset.css + base.css

Application du reset CSS et styles globaux.



### Étape 7 — Ajout de la photo d’accueil


assets: ajouter landing.jpg dans assets/img


Image visible sur la page d’accueil.

---

### Étape 8 — Première documentation de suivi


docs: mise à jour du suivi des commits


Ajout de l’historique logique dans `02_commits.md`.

---

##  Bonnes pratiques Git

- 🔸 Faire un commit **toutes les 15 à 30 minutes** maximum quand une étape est terminée  
- 🔸 Garder les messages **courts, clairs, en français ou anglais cohérent**  
- 🔸 Ne pas faire de commits “test” inutiles (tout doit être significatif)  
- 🔸 Vérifier que tout fonctionne avant de committer  
- 🔸 Committer aussi la **documentation** quand elle est mise à jour

---

##  Exemple de séquence typique d’une journée

| Heure | Action | Message de commit |
|:--|:--|:--|
| 08:30 | Création du projet et activation Git | `chore: init projet portfolio` |
| 09:00 | Ajout des variables CSS | `style: ajouter variables couleurs` |
| 09:45 | Création de index.html | `feat(home): structure page d’accueil` |
| 10:10 | Correction du lien CSS | `fix: chemin feuille de style` |
| 10:30 | Note dans la documentation | `docs: mise à jour suivi commits` |

---

 **Conseil personnel :**
Avant de fermer WebStorm, je regarde mes modifications (en vert dans le Commit Panel)  
et je me demande :
> “Si je reprends demain, est-ce que je saurai ce que j’ai fait aujourd’hui ?”

Si oui → je commit 
Si non → j’écris une phrase claire dans `02_commits.md`.

---




