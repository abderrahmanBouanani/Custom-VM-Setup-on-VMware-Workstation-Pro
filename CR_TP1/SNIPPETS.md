# 📚 Bibliothèque de Snippets LaTeX

Collection de snippets utiles pour vos rapports ENSA Agadir.

## 📊 Tableaux Avancés

### Tableau avec Couleurs

```latex
\usepackage{xcolor}
\usepackage{colortbl}

\begin{table}[H]
\centering
\begin{tabular}{|l|c|c|}
\hline
\rowcolor{lightgray}
\textbf{Critère} & \textbf{Valeur} & \textbf{Statut} \\ \hline
Performance & 95\% & \textcolor{green}{OK} \\ \hline
Sécurité & 88\% & \textcolor{orange}{Moyen} \\ \hline
\end{tabular}
\caption{Tableau avec couleurs}
\end{table}
```

### Tableau Multi-lignes et Multi-colonnes

```latex
\begin{table}[H]
\centering
\begin{tabular}{|l|c|c|c|}
\hline
\multirow{2}{*}{\textbf{Catégorie}} & \multicolumn{3}{c|}{\textbf{Métriques}} \\ \cline{2-4}
 & Sprint 1 & Sprint 2 & Sprint 3 \\ \hline
Vélocité & 10 & 12 & 15 \\ \hline
Bugs & 5 & 3 & 2 \\ \hline
\end{tabular}
\caption{Tableau avec fusion de cellules}
\end{table}
```

**Note :** Ajoutez `\usepackage{multirow}` dans le préambule.

---

## 📈 Diagrammes et Graphiques

### Diagramme Simple avec TikZ

```latex
\usepackage{tikz}

\begin{figure}[H]
\centering
\begin{tikzpicture}
    % Nœuds
    \node[rectangle, draw, fill=blue!20] (a) at (0,0) {Étape 1};
    \node[rectangle, draw, fill=green!20] (b) at (3,0) {Étape 2};
    \node[rectangle, draw, fill=red!20] (c) at (6,0) {Étape 3};
    
    % Flèches
    \draw[->, thick] (a) -- (b);
    \draw[->, thick] (b) -- (c);
\end{tikzpicture}
\caption{Diagramme de processus}
\end{figure}
```

### Arbre Hiérarchique

```latex
\usepackage{tikz}
\usetikzlibrary{trees}

\begin{figure}[H]
\centering
\begin{tikzpicture}[
  level 1/.style={sibling distance=3cm},
  level 2/.style={sibling distance=1.5cm}
]
\node {Racine}
    child {node {Branche 1}
        child {node {Feuille 1.1}}
        child {node {Feuille 1.2}}
    }
    child {node {Branche 2}
        child {node {Feuille 2.1}}
        child {node {Feuille 2.2}}
    };
\end{tikzpicture}
\caption{Arbre hiérarchique}
\end{figure}
```

---

## 💻 Code Source

### Bloc de Code avec Coloration Syntaxique

```latex
\usepackage{listings}
\usepackage{xcolor}

\lstdefinestyle{mystyle}{
    backgroundcolor=\color{gray!10},
    commentstyle=\color{green!60!black},
    keywordstyle=\color{blue},
    numberstyle=\tiny\color{gray},
    stringstyle=\color{orange},
    basicstyle=\ttfamily\footnotesize,
    breakatwhitespace=false,
    breaklines=true,
    captionpos=b,
    keepspaces=true,
    numbers=left,
    numbersep=5pt,
    showspaces=false,
    showstringspaces=false,
    showtabs=false,
    tabsize=2
}

\lstset{style=mystyle}

\begin{lstlisting}[language=Python, caption=Exemple de code Python]
def hello_world():
    print("Hello, ENSA Agadir!")
    return True

if __name__ == "__main__":
    hello_world()
\end{lstlisting}
```

### Code depuis un Fichier Externe

```latex
\lstinputlisting[language=Java, caption=Code Java]{src/Main.java}
```

---

## 📝 Listes Personnalisées

### Liste avec Symboles Personnalisés

```latex
\begin{itemize}
    \item[$\checkmark$] Tâche complétée
    \item[$\times$] Tâche échouée
    \item[$\rightarrow$] Tâche en cours
    \item[$\star$] Tâche prioritaire
\end{itemize}
```

### Liste Numérotée Personnalisée

```latex
\usepackage{enumitem}

\begin{enumerate}[label=\Alph*.]  % A. B. C.
    \item Premier élément
    \item Deuxième élément
\end{enumerate}

\begin{enumerate}[label=(\roman*)]  % (i) (ii) (iii)
    \item Premier élément
    \item Deuxième élément
\end{enumerate}
```

---

## 🎨 Boîtes et Encadrés

### Boîte d'Information

```latex
\usepackage{tcolorbox}

\begin{tcolorbox}[colback=blue!5!white, colframe=blue!75!black, title=Information]
Ceci est une information importante à retenir.
\end{tcolorbox}
```

### Boîte d'Avertissement

```latex
\begin{tcolorbox}[colback=yellow!5!white, colframe=orange!75!black, title=Attention]
Faites attention à ce point particulier !
\end{tcolorbox}
```

### Boîte Simple

```latex
\fbox{
\parbox{0.9\textwidth}{
Texte encadré dans une boîte simple.
}
}
```

---

## 📐 Équations et Mathématiques

### Système d'Équations

```latex
\begin{equation}
\begin{cases}
x + y = 5 \\
2x - y = 1
\end{cases}
\end{equation}
```

### Matrice

```latex
\begin{equation}
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix}
\end{equation}
```

### Équations Alignées

```latex
\begin{align}
f(x) &= x^2 + 2x + 1 \\
     &= (x + 1)^2
\end{align}
```

---

## 📋 Glossaire et Acronymes

```latex
\usepackage[acronym]{glossaries}

\makeglossaries

% Définitions
\newacronym{api}{API}{Application Programming Interface}
\newacronym{mvc}{MVC}{Model-View-Controller}

% Dans le texte
La \gls{api} utilise le pattern \gls{mvc}.

% À la fin du document
\printglossary[type=\acronymtype]
```

---

## 📅 Diagramme de Gantt

```latex
\usepackage{pgfgantt}

\begin{figure}[H]
\centering
\begin{ganttchart}[
    vgrid,
    hgrid,
    x unit=1cm,
    y unit title=0.5cm,
    y unit chart=0.7cm
]{1}{10}
\gantttitle{Sprint 1}{10} \\
\gantttitlelist{1,...,10}{1} \\
\ganttbar{US1}{1}{3} \\
\ganttbar{US2}{3}{5} \\
\ganttbar{US3}{5}{7} \\
\ganttbar{US4}{7}{10}
\end{ganttchart}
\caption{Planning du Sprint}
\end{figure}
```

---

## 🔗 Références Croisées

### Référencer des Éléments

```latex
% Définir un label
\section{Introduction}\label{sec:intro}
\begin{figure}[H]
    % ... figure ...
    \label{fig:architecture}
\end{figure}

% Référencer
Comme mentionné dans la section~\ref{sec:intro}...
La Figure~\ref{fig:architecture} montre...
```

---

## 📊 Graphiques avec pgfplots

```latex
\usepackage{pgfplots}
\pgfplotsset{compat=1.17}

\begin{figure}[H]
\centering
\begin{tikzpicture}
\begin{axis}[
    xlabel={Sprint},
    ylabel={Vélocité},
    xmin=0, xmax=5,
    ymin=0, ymax=20,
    legend pos=north west,
]
\addplot coordinates {
    (1,10) (2,12) (3,15) (4,14) (5,18)
};
\legend{Vélocité}
\end{axis}
\end{tikzpicture}
\caption{Évolution de la vélocité}
\end{figure}
```

---

## 📖 Bibliographie

### Bibliographie Simple

```latex
\begin{thebibliography}{9}
\bibitem{scrum}
Schwaber, K., \& Sutherland, J. (2020).
\textit{The Scrum Guide}.
Scrum.org.

\bibitem{agile}
Beck, K., et al. (2001).
\textit{Manifesto for Agile Software Development}.
AgileManifesto.org.
\end{thebibliography}
```

### Avec BibTeX

```latex
% Dans le préambule
\usepackage{natbib}

% Dans le texte
Selon \cite{scrum}, la méthodologie Scrum...

% À la fin du document
\bibliographystyle{plain}
\bibliography{references}  % fichier references.bib
```

---

## 🎯 Mise en Page Spéciale

### Colonnes Multiples

```latex
\usepackage{multicol}

\begin{multicols}{2}
Texte sur deux colonnes...
\end{multicols}
```

### Paysage

```latex
\usepackage{pdflscape}

\begin{landscape}
% Contenu en mode paysage (ex: grand tableau)
\end{landscape}
```

---

## ✨ Astuces de Mise en Forme

### Espacement

```latex
\vspace{1cm}        % Espace vertical
\hspace{2cm}        % Espace horizontal
\vfill              % Remplit l'espace vertical
\newpage            % Nouvelle page
\clearpage          % Nouvelle page + flush des figures
```

### Texte Spécial

```latex
\textbf{Gras}
\textit{Italique}
\underline{Souligné}
\texttt{Code}
\textsc{Petites Capitales}
\emph{Emphase}
```

### Citations

```latex
\begin{quote}
Citation courte
\end{quote}

\begin{quotation}
Citation longue avec plusieurs paragraphes...
\end{quotation}
```

---

## 🛠️ Packages Utiles

```latex
\usepackage{amsmath}        % Équations avancées
\usepackage{amssymb}        % Symboles mathématiques
\usepackage{graphicx}       % Images
\usepackage{subcaption}     % Sous-figures
\usepackage{hyperref}       % Liens hypertextes
\usepackage{xcolor}         % Couleurs
\usepackage{listings}       % Code source
\usepackage{tikz}           % Diagrammes
\usepackage{pgfplots}       % Graphiques
\usepackage{tcolorbox}      % Boîtes colorées
\usepackage{enumitem}       % Listes personnalisées
\usepackage{multirow}       % Tableaux multi-lignes
\usepackage{longtable}      % Tableaux longs
\usepackage{algorithm}      % Algorithmes
\usepackage{algpseudocode}  % Pseudo-code
```

---

**Copiez-collez ces snippets dans votre document pour gagner du temps ! ⚡**
