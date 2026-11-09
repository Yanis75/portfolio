# Portfolio Yanis Allouani

Site statique (HTML + CSS, aucun framework, aucune étape de build).

## Arborescence

```
index.html                                   Page d'accueil
etudes/accessibilite-parcours-credit.html    Étude de cas 01
assets/css/style.css                         Styles (une seule feuille)
assets/img/yanis-allouani.jpg                Photo
assets/cv/*.pdf                              Les deux CV téléchargeables
favicon.svg                                  Icône d'onglet
vercel.json                                  URLs propres (sans .html) + cache des assets
```

## Mettre en ligne sur Vercel

**Option 1 : via GitHub (recommandé, mises à jour automatiques)**
1. Créer un dépôt GitHub (ex. `portfolio`) et y pousser le contenu de ce dossier.
2. Sur vercel.com : *Add New → Project*, importer le dépôt.
3. Framework Preset : **Other**. Build Command : vide. Output Directory : `.` (racine).
4. *Deploy*. Chaque `git push` redéploie le site.

**Option 2 : en ligne de commande**
```bash
npm i -g vercel
cd portfolio
vercel          # premier déploiement (aperçu)
vercel --prod   # mise en production
```

Le site sera servi sur `https://<nom-du-projet>.vercel.app`. Vous pouvez renommer le projet (ex. `yanis-allouani`) dans les réglages Vercel.

## Après la mise en ligne

- Ajouter l'URL dans l'en-tête des deux CV et sur LinkedIn (section « Coordonnées » + « Sélection »).
- Remplacer les PDF de `assets/cv/` à chaque mise à jour des CV (mêmes noms de fichiers).
- Vérifier l'accessibilité : navigation au clavier (Tab), axe DevTools, WAVE.

## Ajouter une étude de cas

Dupliquer `etudes/accessibilite-parcours-credit.html`, garder la même structure
(Contexte, Problème, Démarche, Livrable, Résultats, Ce que j'ai appris), puis remplacer
dans `index.html` la mention « Étude de cas en cours de rédaction » de la carte concernée
par un lien `<a class="case-link" href="etudes/nouveau-fichier.html">`.
