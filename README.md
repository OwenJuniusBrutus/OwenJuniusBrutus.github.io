# Site Eutopia

Source Jekyll du site public : <https://owenjuniusbrutus.github.io/>.

## Publication actuelle

GitHub Pages publie la branche `main`, dossier racine `/`. Il n'est pas nécessaire de sélectionner GitHub Actions : GitHub construit automatiquement les fichiers Jekyll présents sur cette branche.

Dans **Settings → Pages**, la source doit rester configurée ainsi :

- **Deploy from a branch**
- branche **main**
- dossier **/(root)**

## Installation locale

Ruby 3.3 avec Devkit est installé dans `C:\Ruby33-x64`.

Depuis ce dossier :

```powershell
$env:Path = "C:\Ruby33-x64\bin;$env:Path"
bundle install
bundle exec jekyll build
```

Pour lancer un aperçu local :

```powershell
$env:Path = "C:\Ruby33-x64\bin;$env:Path"
bundle exec jekyll serve --baseurl ""
```

Ouvrir ensuite <http://127.0.0.1:4000/>.

## Mise à jour du site

Après avoir modifié les fichiers :

```powershell
$env:Path = "C:\Ruby33-x64\bin;$env:Path"
bundle exec jekyll build
git add .
git commit -m "Update Eutopia website"
git push origin main
```

GitHub Pages reconstruit ensuite le site depuis `main`. L'état de la publication est visible dans **Settings → Pages** ou à l'adresse <https://github.com/OwenJuniusBrutus/OwenJuniusBrutus.github.io/deployments>.

## Structure

- `_layouts/` : structure HTML commune.
- `_includes/` : menu partagé par toutes les pages.
- `assets/` : feuille de style et images.
- `guides/` : une page par guide.
- `index.html` : page d'accueil.
- `mod-list.html` : liste des mods.
