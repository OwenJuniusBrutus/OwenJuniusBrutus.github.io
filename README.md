# Site Eutopia

Site Jekyll destiné à GitHub Pages.

## Publication

1. Créer un dépôt GitHub et placer **le contenu de ce dossier** à la racine du dépôt.
2. Utiliser `main` comme branche par défaut, ou adapter la branche dans `.github/workflows/jekyll.yml`.
3. Dans **Settings → Pages → Build and deployment**, sélectionner **GitHub Actions** comme source.
4. Envoyer les fichiers sur GitHub. Le workflow construit puis publie le site automatiquement.

Les liens utilisent le filtre Jekyll `relative_url`. Le site fonctionne donc aussi bien sur un domaine utilisateur (`nom.github.io`) que dans un sous-chemin de dépôt (`nom.github.io/depot`). GitHub renseigne ce sous-chemin pendant la construction.

## Aperçu local avec Jekyll

Ruby et Bundler doivent être installés :

```powershell
bundle install
bundle exec jekyll serve
```

Ouvrir ensuite `http://localhost:4000`.

## Structure

- `_layouts/` : structure HTML commune.
- `_includes/` : menu partagé par toutes les pages.
- `assets/` : feuille de style et images.
- `guides/` : une page par guide.
- `index.html` : page d'accueil.
- `mod-list.html` : liste des mods.

