# CV de Manoel Da Ponte - Awesome Resume Project

## Présentation du projet

Ce projet contient les fichiers sources d'un CV et d'une lettre de motivation professionnels, créés avec LaTeX en utilisant le template Awesome-CV. Le design est moderne, élégant et hautement personnalisable, permettant de créer différentes versions (complète ou condensée sur une page) du même CV.

## Structure du projet

```
.
├── awesome-cv.cls               # Classe LaTeX principale du template
├── cover_letter.tex             # Template de lettre de motivation
├── cv-sections/                 # Dossiers contenant les sections modulaires du CV
│   ├── education.tex            # Section formation complète
│   ├── education-onepage.tex    # Section formation condensée (une page)
│   ├── experience.tex           # Section expérience professionnelle complète
│   ├── experience-onepage.tex   # Section expérience condensée
│   ├── profile-onepage.tex      # Section profil personnel condensé
│   ├── projects.tex             # Section projets significatifs
│   └── skills.tex               # Section compétences
├── fontawesome.sty              # Style pour les icônes Font Awesome
├── fonts/                       # Dossier pour les polices (non inclus dans le dépôt)
├── resume_cv.tex                # Fichier principal du CV complet
└── resume_cv_onepage.tex        # Fichier principal du CV version une page
```

## Prérequis

Pour compiler ces documents LaTeX, vous aurez besoin de :

1. Une distribution LaTeX complète (comme TeX Live, MiKTeX ou MacTeX)
2. XeLaTeX (pour la gestion des polices)
3. Les polices suivantes dans le dossier `fonts/` :
    - Roboto (pour les en-têtes)
    - Source Sans Pro (pour le corps du texte)
    - FontAwesome (pour les icônes)

## Compilation des documents

Les documents doivent être compilés avec XeLaTeX pour assurer le bon fonctionnement des polices et des caractéristiques spéciales. Commandes recommandées :

```bash
# Pour compiler le CV complet
xelatex resume_cv.tex

# Pour compiler le CV version une page
xelatex resume_cv_onepage.tex

# Pour compiler la lettre de motivation
xelatex cover_letter.tex
```

## Personnalisation

### Informations personnelles

Modifiez les informations personnelles dans les fichiers `resume_cv.tex` et `resume_cv_onepage.tex` :

```latex
\name{Prénom}{Nom}
\address{Votre adresse}
\mobile{Votre numéro de téléphone}
\email{votre.email@exemple.com}
\homepage{votre-site-web.com}
\linkedin{votre-profil-linkedin}
```

### Sections du CV

Chaque section est dans un fichier séparé dans le dossier `cv-sections/`, ce qui permet une édition modulaire :

-   Modifiez `skills.tex` pour mettre à jour vos compétences
-   Modifiez `experience.tex` ou `experience-onepage.tex` pour mettre à jour votre expérience professionnelle
-   Modifiez `education.tex` ou `education-onepage.tex` pour mettre à jour votre formation
-   Modifiez `projects.tex` pour mettre à jour vos projets significatifs

### Couleurs et style

La couleur principale peut être modifiée dans les fichiers `resume_cv.tex` et `resume_cv_onepage.tex` :

```latex
\definecolor{myblue}{HTML}{0066CC} % Changez le code couleur
\colorlet{awesome}{myblue}
```

## Lettre de motivation

Le fichier `cover_letter.tex` sert de modèle pour créer une lettre de motivation assortie au CV. Les sections principales à modifier sont :

```latex
\recipient{Service des Ressources Humaines}{Nom de l'Entreprise\\Adresse de l'Entreprise\\Code Postal, Ville}
\lettertitle{Candidature au poste d'Ingénieur Data Scientist}
\letteropening{Madame, Monsieur,}
\letterclosing{Je vous prie d'agréer, Madame, Monsieur, l'expression de mes salutations distinguées.}
```

Ainsi que le contenu entre les balises `\begin{cvletter}` et `\end{cvletter}`.

## Licence

Ce projet utilise le template Awesome-CV sous licence CC BY-NC-SA 3.0.

---
