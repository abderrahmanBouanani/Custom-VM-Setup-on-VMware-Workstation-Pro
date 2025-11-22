# Installer et Configurer une Machine Virtuelle Personnalisée sur VMware Workstation Pro

## Description

Ce guide complet vous accompagne dans l'installation et la configuration d'une machine virtuelle sur VMware Workstation Pro. Vous apprendrez à créer un environnement virtualisé Windows 10 avec une configuration personnalisée avancée.

## Objectifs

- Étudier et comparer des outils de virtualisation (VMware Player, VMware Workstation Pro, VirtualBox)
- Créer et configurer une machine virtuelle personnalisée avec VMware Workstation Pro
- Installer Windows 10 64-bit dans un environnement virtualisé
- Comprendre les différents paramètres de configuration d'une VM

## Structure du Projet

```
CR_TP1/
├── template_ensa_agadir.tex    # Document LaTeX principal
├── template_ensa_agadir.pdf    # Guide compilé (à générer)
├── figures/                     # Dossier contenant les captures d'écran
│   ├── 1.png à 34.png          # Screenshots du tutoriel
│   ├── ENSAA.png               # Logo ENSA Agadir
│   └── UIZ.png                 # Logo UIZ
├── .gitignore                  # Fichiers LaTeX à ignorer
└── README.md                   # Ce fichier
```

## Contenu du Guide

### Partie 1 : Étude Comparative
- Comparaison détaillée de VMware Player Free Edition, VMware Workstation Pro et VirtualBox
- Tableau comparatif selon les critères : type de virtualisation, prérequis, OS supportés, fonctionnalités, sécurité, part de marché

### Partie 2 : Installation et Configuration Pratique
- Installation de VMware Workstation Pro 17.6
- Configuration personnalisée (Custom) d'une machine virtuelle :
  - Choix de la compatibilité matérielle
  - Configuration processeur (2 cœurs)
  - Allocation mémoire (2 GB RAM)
  - Configuration réseau (Host-only)
  - Disque virtuel NVMe (60 GB, pré-alloué)
- Installation de Windows 10 x64
- Réponses aux 10 questions du guide

## Prérequis pour Compilation

Pour compiler le document LaTeX, vous aurez besoin de :

- Distribution LaTeX (TeX Live, MiKTeX, ou MacTeX)
- Packages LaTeX requis :
  - `babel` (français)
  - `graphicx`
  - `hyperref`
  - `fancyhdr`
  - `geometry`
  - `float`
  - `booktabs`

## Compilation du Document

### Avec pdflatex
```bash
cd CR_TP1
pdflatex template_ensa_agadir.tex
pdflatex template_ensa_agadir.tex  # Seconde compilation pour la table des matières
```

### Avec latexmk (recommandé)
```bash
cd CR_TP1
latexmk -pdf template_ensa_agadir.tex
```

## Points Clés Abordés

1. Installation complète de VMware Workstation Pro (captures d'écran détaillées)
2. Différence entre VM Typical et Custom
3. Méthodes d'installation (disque physique vs ISO)
4. Sélection et optimisation du système d'exploitation
5. Choix entre BIOS et EFI
6. Configuration des types de réseau virtuels (Bridged, NAT, Host-only)
7. Contrôleurs SCSI et leurs différences (BusLogic, LSI Logic, LSI Logic SAS)
8. Types de disques virtuels (IDE, SCSI, SATA, NVMe)
9. Options de disque virtuel (nouveau, existant, physique)
10. Stratégies d'allocation de l'espace disque (pré-allocation vs dynamique)

## Technologies Utilisées

- **VMware Workstation Pro 17.6** : Hyperviseur de type 2
- **Windows 10 x64** : Système d'exploitation invité
- **LaTeX** : Rédaction du compte rendu
- **Git** : Gestion de version

## Auteur

- **Youssefi**

## Contributions

Les contributions, suggestions et améliorations sont les bienvenues ! N'hésitez pas à ouvrir une issue ou proposer une pull request.

## License

Ce guide est partagé à des fins éducatives et pédagogiques.
