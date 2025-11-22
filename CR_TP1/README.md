# Template LaTeX ENSA Agadir

Ce template LaTeX est conçu pour les rapports de TP/TD de l'École Nationale des Sciences Appliquées d'Agadir.

## 📋 Contenu du Template

Le template comprend :
- ✅ Page de garde professionnelle avec logos ENSA et UIZ
- ✅ En-tête et pied de page personnalisés
- ✅ Table des matières automatique
- ✅ Sections pré-structurées
- ✅ Exemples de tableaux, figures, listes et équations
- ✅ Configuration des liens hypertextes
- ✅ Mise en page optimisée (marges de 2.5cm)

## 🚀 Utilisation Rapide

### 1. Personnalisation des Informations

Au début du document, modifiez les commandes suivantes selon vos besoins :

```latex
\newcommand{\monTitre}{[Titre du TP/TD]}
\newcommand{\monSousTitre}{[Sous-titre ou thème]}
\newcommand{\maFiliere}{[Filière : ex. DLA2, GI, etc.]}
\newcommand{\monAnnee}{[Année : ex. 2025-2026]}
\newcommand{\monEtudiantUn}{[NOM Prénom 1]}
\newcommand{\monEtudiantDeux}{[NOM Prénom 2]}
\newcommand{\monEtudiantTrois}{[NOM Prénom 3]}
\newcommand{\monProfesseur}{[Prof. NOM]}
```

**Exemple :**
```latex
\newcommand{\monTitre}{TD Qualité Logiciel 6}
\newcommand{\monSousTitre}{Gestion de Projet Agile}
\newcommand{\maFiliere}{Filière : DLA2}
\newcommand{\monAnnee}{2025-2026}
\newcommand{\monEtudiantUn}{Imad DOUIOU}
\newcommand{\monEtudiantDeux}{ABDELKADER KOUAH}
\newcommand{\monEtudiantTrois}{Abderrahman BOUANANI}
\newcommand{\monProfesseur}{Prof. Aimad QAZDAR}
```

### 2. Structure des Dossiers

Créez la structure suivante :
```
votre_projet/
├── rapport.tex (votre fichier basé sur ce template)
└── figures/
    ├── ENSAA.png (logo ENSA Agadir)
    ├── UIZ.png (logo Université Ibn Zohr)
    └── (vos autres images)
```

### 3. Modification du Pied de Page

Dans la configuration du pied de page, modifiez les noms :

```latex
\fancyfoot[L]{\begin{tabular}[t]{@{}l@{}}Nom 1 \\ Nom 2 \\ Nom 3\end{tabular}}
```

## 📝 Éléments Disponibles

### Tableaux

**Tableau simple :**
```latex
\begin{table}[H]
\centering
\begin{tabular}{|l|c|r|}
\hline
\textbf{Colonne 1} & \textbf{Colonne 2} & \textbf{Colonne 3} \\ \hline
Donnée 1 & Donnée 2 & Donnée 3 \\ \hline
\end{tabular}
\caption{Titre du tableau}
\end{table}
```

**Tableau avec colonnes à largeur fixe :**
```latex
\begin{table}[H]
\centering
\begin{tabular}{|p{3cm}|p{5cm}|p{4cm}|}
\hline
\textbf{En-tête 1} & \textbf{En-tête 2} & \textbf{En-tête 3} \\ \hline
Texte long... & Description... & Remarques... \\ \hline
\end{tabular}
\caption{Tableau avec largeurs personnalisées}
\end{table}
```

### Figures

```latex
\begin{figure}[H]
    \centering
    \includegraphics[width=0.6\textwidth]{figures/mon_image.png}
    \caption{Description de l'image}
    \label{fig:monimage}
\end{figure}
```

Pour référencer : `voir Figure~\ref{fig:monimage}`

### Listes

**Liste à puces :**
```latex
\begin{itemize}
    \item Premier élément
    \item Deuxième élément
\end{itemize}
```

**Liste numérotée :**
```latex
\begin{enumerate}
    \item Premier point
    \item Deuxième point
\end{enumerate}
```

### Liens

- Lien simple : `\url{https://www.exemple.com}`
- Lien cliquable : `\href{https://www.exemple.com}{Texte du lien}`

### Mise en Forme du Texte

- **Gras :** `\textbf{texte en gras}`
- *Italique :* `\textit{texte en italique}`
- Souligné : `\underline{texte souligné}`
- Code : `\texttt{code.exemple()}`

### Équations

- Inline : `$E = mc^2$`
- Centrée :
```latex
\begin{equation}
    f(x) = \int_{a}^{b} x^2 dx
\end{equation}
```

## 🔧 Compilation

### Avec LaTeX

```bash
pdflatex template_ensa_agadir.tex
pdflatex template_ensa_agadir.tex  # Deux fois pour la table des matières
```

### Avec Overleaf

1. Créez un nouveau projet
2. Uploadez le fichier .tex
3. Créez le dossier `figures/` et uploadez vos images
4. Compilez

## 📦 Packages Requis

Le template utilise les packages suivants (généralement inclus dans les distributions LaTeX complètes) :

- `inputenc`, `fontenc`, `babel` : Gestion des caractères et langues
- `geometry` : Configuration des marges
- `graphicx` : Insertion d'images
- `float` : Positionnement des figures/tableaux
- `hyperref` : Liens hypertextes
- `fancyhdr` : En-têtes et pieds de page personnalisés
- `lastpage` : Numérotation "Page X/Y"
- `array`, `booktabs` : Tableaux améliorés
- `enumitem` : Listes personnalisables

## 💡 Conseils

1. **Images :** Utilisez des formats PNG ou PDF pour une meilleure qualité
2. **Compilation :** Compilez deux fois pour que la table des matières et les références soient correctes
3. **Sections :** Utilisez `\section`, `\subsection`, `\subsubsection` pour structurer
4. **Labels :** Donnez des noms significatifs à vos labels (`\label{fig:architecture}`)
5. **Espacement :** Le template désactive les alinéas (`\parindent=0cm`) - ajoutez `\vspace{0.5cm}` si besoin

## 🎨 Personnalisation Avancée

### Modifier les couleurs des liens

```latex
\hypersetup{
    colorlinks=true,
    linkcolor=red,        % Liens internes
    filecolor=magenta,    % Fichiers
    urlcolor=blue,        % URLs
}
```

### Changer les marges

```latex
\geometry{a4paper, margin=3cm}  % Marges de 3cm au lieu de 2.5cm
```

### Ajouter un quatrième étudiant

Modifiez le pied de page :
```latex
\fancyfoot[L]{\begin{tabular}[t]{@{}l@{}}Nom 1 \\ Nom 2 \\ Nom 3 \\ Nom 4\end{tabular}}
```

## 📄 Licence

Template libre d'utilisation pour les étudiants de l'ENSA Agadir.

## ❓ Support

Pour toute question ou amélioration, contactez votre professeur ou l'administration de l'ENSA.

---

**Bonne rédaction ! 📚**
