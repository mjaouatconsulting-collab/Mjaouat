# Site Académique — Documentation

Ce dossier contient deux versions d'un site académique minimaliste et premium :

- **`standalone/`** — Version autonome : un seul fichier `index.html` (HTML + CSS + JS intégrés)
- **`clean/`** — Version propre : 3 fichiers séparés (`index.html`, `styles.css`, `script.js`)

---

## Structure des fichiers

```
.
├── standalone/
│   └── index.html          # Version tout-en-un
├── clean/
│   ├── index.html          # Structure HTML
│   ├── styles.css          # Styles CSS
│   └── script.js           # JavaScript
└── README.md               # Ce fichier
```

---

## Personnalisation

### 1. Remplacer les placeholders

Recherchez et remplacez tous les textes `[À compléter : ...]` par vos informations :

| Placeholder | Exemple de remplacement |
|-------------|------------------------|
| `[À compléter : Prénom Nom]` | `Marie Dupont` |
| `[À compléter : Titre académique]` | `Professeure en Sciences Économiques` |
| `[À compléter : Affiliation institutionnelle]` | `Université Paris-Saclay` |
| `[À compléter : email@institution.fr]` | `marie.dupont@universite.fr` |

### 2. Ajouter des publications

Dans la section **Research**, dupliquez le bloc `<article class="publication">` pour ajouter de nouvelles publications.

### 3. Modifier les couleurs (optionnel)

Dans le CSS, modifiez les variables CSS sous `:root` :

```css
:root {
    --color-bg: #fefefe;        /* Couleur de fond */
    --color-text: #1a1a1a;      /* Couleur du texte principal */
    --color-accent: #2c3e50;    /* Couleur d'accentuation (liens) */
}
```

---

## Déploiement sur GitHub Pages

### Étape 1 : Créer un dépôt GitHub

1. Connectez-vous à [GitHub](https://github.com)
2. Cliquez sur **New repository** (bouton vert "+" en haut à droite)
3. Nommez votre dépôt : `votre-nom-academique` (ex: `marie-dupont`)
4. Choisissez **Public**
5. Cliquez sur **Create repository**

### Étape 2 : Uploader les fichiers

#### Méthode A — Interface web (recommandée pour débutants)

1. Sur la page de votre dépôt, cliquez sur **Add file** → **Upload files**
2. Glissez-déposez les fichiers de la version choisie :
   - Pour la version **standalone** : uniquement `index.html`
   - Pour la version **clean** : `index.html`, `styles.css`, `script.js`
3. Cliquez sur **Commit changes**

#### Méthode B — Ligne de commande

```bash
# Cloner le dépôt (remplacez par votre URL)
git clone https://github.com/votre-username/votre-nom-academique.git
cd votre-nom-academique

# Copier les fichiers (exemple avec la version clean)
cp /chemin/vers/clean/* .

# Commit et push
git add .
git commit -m "Initial commit: site académique"
git push origin main
```

### Étape 3 : Activer GitHub Pages

1. Sur votre dépôt GitHub, cliquez sur l'onglet **Settings**
2. Dans le menu de gauche, cliquez sur **Pages**
3. Sous **Source**, sélectionnez :
   - **Deploy from a branch**
   - Branch : `main` (ou `master`)
   - Folder : `/ (root)`
4. Cliquez sur **Save**

### Étape 4 : Vérifier le déploiement

1. Retournez sur l'onglet **Actions** de votre dépôt
2. Attendez que le workflow "pages build and deployment" soit terminé (icône verte ✓)
3. Votre site est accessible à l'adresse :
   ```
   https://votre-username.github.io/votre-nom-academique/
   ```

**Exemple** : `https://mariedupont.github.io/marie-dupont/`

---

## Mise à jour du site

Pour modifier votre site après le déploiement :

1. Modifiez les fichiers localement
2. Committez et pushez les changements :
   ```bash
   git add .
   git commit -m "Mise à jour des publications"
   git push origin main
   ```
3. Les modifications seront automatiquement déployées (délai : 1-2 minutes)

---

## Caractéristiques du design

- **Style** : Académique minimal premium
- **Typographie** : Georgia (titres) + System UI (corps)
- **Palette** : Blanc cassé, gris anthracite, accents sobres
- **Responsive** : Adapté mobile et desktop
- **Accessibilité** : Navigation clavier, contrastes conformes

---

## Dépannage

| Problème | Solution |
|----------|----------|
| Le site ne s'affiche pas | Vérifiez que `index.html` est à la racine du dépôt |
| Les styles ne chargent pas (version clean) | Vérifiez que `styles.css` est bien uploadé et au même niveau que `index.html` |
| La page reste blanche | Ouvrez la console développeur (F12) pour voir les erreurs |
| Les liens ne fonctionnent pas | Assurez-vous que les ancres correspondent aux IDs des sections |

---

## Licence

Ce template est libre d'utilisation. Modifiez-le selon vos besoins.

---

## Contact & Support

Pour toute question sur GitHub Pages : [docs.github.com/pages](https://docs.github.com/fr/pages)
