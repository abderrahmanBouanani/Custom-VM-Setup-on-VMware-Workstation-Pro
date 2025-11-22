# 🚀 Guide de Démarrage Rapide

## En 5 Minutes

### Étape 1 : Préparer les Images (2 min)
1. Placez les logos **ENSAA.png** et **UIZ.png** dans le dossier `figures/`
2. Ajoutez vos propres images si nécessaire

### Étape 2 : Choisir Votre Point de Départ (1 min)

**Option A : Commencer avec l'exemple**
- Ouvrez `exemple_utilisation.tex`
- C'est un document pré-rempli avec vos informations

**Option B : Template vierge**
- Ouvrez `template_ensa_agadir.tex`
- C'est un template avec tous les exemples

### Étape 3 : Personnaliser les Informations (2 min)

Modifiez ces lignes dans votre fichier .tex :

```latex
\newcommand{\monTitre}{TD Qualité Logiciel 6}
\newcommand{\monSousTitre}{Gestion de Projet Agile}
\newcommand{\maFiliere}{Filière : DLA2}
\newcommand{\monAnnee}{2025-2026}
\newcommand{\monEtudiantUn}{Votre Nom}
\newcommand{\monEtudiantDeux}{Nom 2}
\newcommand{\monEtudiantTrois}{Nom 3}
\newcommand{\monProfesseur}{Prof. Nom}
```

### Étape 4 : Compiler

**Méthode 1 - Visual Studio Code :**
1. Installez l'extension "LaTeX Workshop"
2. Ouvrez votre fichier .tex
3. Cliquez sur l'icône de compilation ou utilisez `Ctrl+Alt+B`

**Méthode 2 - Ligne de commande :**
```bash
pdflatex votre_fichier.tex
pdflatex votre_fichier.tex  # Deux fois pour les références
```

**Méthode 3 - Overleaf :**
1. Créez un compte sur [overleaf.com](https://www.overleaf.com)
2. Créez un nouveau projet et uploadez les fichiers
3. La compilation est automatique

---

## ✅ Checklist Avant de Commencer

- [ ] J'ai les logos ENSAA.png et UIZ.png
- [ ] J'ai installé LaTeX (MiKTeX, TeX Live, ou j'utilise Overleaf)
- [ ] J'ai un éditeur (VS Code, TeXstudio, ou Overleaf)
- [ ] J'ai choisi entre `template_ensa_agadir.tex` ou `exemple_utilisation.tex`

---

## 📚 Structure du Template

```
Template ENSA Agadir/
├── 📄 template_ensa_agadir.tex     (Template complet avec exemples)
├── 📄 exemple_utilisation.tex       (Exemple minimaliste)
├── 📖 README.md                     (Documentation complète)
├── 🚀 GUIDE_DEMARRAGE.md           (Ce fichier)
└── 📁 figures/                      (Dossier pour les images)
    ├── ENSAA.png                    (À ajouter)
    ├── UIZ.png                      (À ajouter)
    └── README.md                    (Instructions)
```

---

## 🎯 Workflow Recommandé

1. **Copier** le template dans un nouveau dossier pour votre projet
2. **Renommer** le fichier selon votre besoin (ex: `TP6_Qualite_Logiciel.tex`)
3. **Personnaliser** les informations en haut du document
4. **Écrire** votre contenu section par section
5. **Compiler** régulièrement pour vérifier le rendu
6. **Sauvegarder** votre travail fréquemment

---

## 💾 Installation de LaTeX

### Windows
- [MiKTeX](https://miktex.org/download) (Recommandé)
- [TeX Live](https://www.tug.org/texlive/)

### Mac
- [MacTeX](https://www.tug.org/mactex/)

### Linux
```bash
# Ubuntu/Debian
sudo apt-get install texlive-full

# Fedora
sudo dnf install texlive-scheme-full
```

### Sans Installation
- [Overleaf](https://www.overleaf.com) (Gratuit, en ligne)

---

## 🔧 Éditeurs Recommandés

1. **Overleaf** - Idéal pour débuter (en ligne, gratuit)
2. **VS Code** + Extension "LaTeX Workshop" - Puissant et moderne
3. **TeXstudio** - Spécialisé pour LaTeX
4. **TeXmaker** - Simple et efficace

---

## ❓ Problèmes Fréquents

### Les images ne s'affichent pas
✅ **Solution :** Vérifiez que les fichiers PNG sont bien dans `figures/` avec les bons noms

### Erreur "File not found"
✅ **Solution :** Vérifiez les chemins des images dans le code

### La table des matières est vide
✅ **Solution :** Compilez **deux fois** le document

### Caractères accentués bizarres
✅ **Solution :** Vérifiez que l'encodage du fichier est UTF-8

### Package manquant
✅ **Solution :** 
- MiKTeX : Installation automatique au premier lancement
- TeX Live : Installez le package avec `tlmgr install <package>`

---

## 🎨 Personnalisation Rapide

### Changer la couleur des liens
```latex
\hypersetup{
    colorlinks=true,
    linkcolor=red,      % Changez 'blue' en 'red'
    urlcolor=purple,    % Changez 'cyan' en 'purple'
}
```

### Modifier les marges
```latex
\geometry{a4paper, margin=3cm}  % Au lieu de 2.5cm
```

### Ajouter un logo supplémentaire
```latex
\includegraphics[width=0.3\textwidth]{figures/logo_supplementaire.png}
```

---

## 📞 Besoin d'Aide ?

1. Consultez le **README.md** pour la documentation complète
2. Regardez les exemples dans **template_ensa_agadir.tex**
3. Testez avec **exemple_utilisation.tex** pour débuter simplement
4. Contactez votre professeur ou l'administration

---

**Bon courage pour votre rédaction ! 📝✨**
