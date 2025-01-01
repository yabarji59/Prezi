
# Marp CLI Guide

Marp CLI est un outil puissant pour convertir des fichiers Markdown en diapositives ou documents (PDF, HTML, etc.). Voici une documentation détaillée pour l'utiliser efficacement.

## Installation

Pour utiliser Marp CLI, installez-le globalement via npm :

```bash
npm install -g @marp-team/marp-cli
```

## Commandes principales

### Prévisualisation des diapositives (`--preview`)

Pour lancer une prévisualisation de vos diapositives dans le navigateur :

```bash
marp --preview your-presentation.md
```

Cela ouvre automatiquement votre présentation dans un navigateur et met à jour les changements en direct.

---

### Génération en PDF (`--pdf`)

Pour exporter une présentation en PDF :

```bash
marp --pdf your-presentation.md
```

Vous pouvez aussi indiquer un chemin de sortie spécifique :

```bash
marp --pdf your-presentation.md -o output-file.pdf
```

---

### Génération en HTML (`--html`)

Pour exporter votre présentation en HTML autonome :

```bash
marp --html your-presentation.md
```

Pour inclure un fichier CSS personnalisé :

```bash
marp --html --theme custom-theme.css your-presentation.md
```

---

### Prise en charge des thèmes personnalisés

Pour utiliser un thème CSS personnalisé, ajoutez l'option `--theme` :

1. Créez un fichier CSS pour votre thème, par exemple `custom-theme.css`.
2. Appliquez le thème à votre présentation :

```bash
marp --theme custom-theme.css your-presentation.md
```

Vous pouvez également utiliser des thèmes intégrés comme `default` ou `gaia`.

---

### Autres options utiles

#### Génération en lot

Pour convertir tous les fichiers Markdown d'un répertoire :

```bash
marp --pdf *.md
```

#### Spécifier la taille des diapositives

Utilisez `--width` et `--height` pour définir la taille des diapositives :

```bash
marp --width 1280 --height 720 your-presentation.md
```

#### Forcer un arrière-plan sombre ou clair

Ajoutez `--theme-set` pour un thème spécifique ou forcez le mode sombre :

```bash
marp --theme dark your-presentation.md
```

#### Ajouter des notes du présentateur

Pour inclure des notes au format HTML, utilisez `--notes` :

```bash
marp --notes your-presentation.md
```

---

### Commandes avancées

#### Définir des options globales

Vous pouvez définir des options globales pour éviter de les répéter à chaque commande :

1. Créez un fichier de configuration `.marprc.yml` :

```yaml
theme: custom-theme.css
pdfNotes: true
html: true
```

2. Lancez simplement Marp CLI :

```bash
marp your-presentation.md
```

---

### Ressources

- [Documentation officielle de Marp](https://marp.app)
- [Dépôt GitHub](https://github.com/marp-team/marp-cli)
- [Créer des thèmes personnalisés](https://marpit.marp.app/theme-css)

---

Avec ces commandes et options, vous pouvez exploiter toute la puissance de Marp CLI pour vos présentations Markdown !
