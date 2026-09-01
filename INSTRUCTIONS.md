# Déploiement du carnet en PWA (mode artiste)

## 1. Mettre les 4 fichiers sur GitHub Pages

Sur github.com, dans ton dépôt (ou un nouveau dépôt) :
1. **Add file → Upload files**, glisse les 4 fichiers :
   `carnet-artiste.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`
2. Commit.
3. **Settings → Pages** → Source : `Deploy from a branch` → branche `main`, dossier `/ (root)` → Save.
4. Après ~1 minute, ton carnet est en ligne à une adresse du type :
   `https://TON-PSEUDO.github.io/TON-DEPOT/carnet-artiste.html`

## 2. Choisir ton secret et corriger le manifest

Choisis une longue chaîne aléatoire (ex. `a8f3d9e2b1c7f0e5`) — c'est ton mot de passe artiste, qui sera aussi ton lien magique.

Édite `manifest.json` sur GitHub (crayon ✏️) et remplace :
```
"start_url": "./carnet-artiste.html#artist=REMPLACE_PAR_TON_SECRET",
```
par ton propre secret, ex. :
```
"start_url": "./carnet-artiste.html#artist=a8f3d9e2b1c7f0e5",
```
Commit.

## 3. Activer ton mode artiste une première fois

Ouvre dans un navigateur :
```
https://TON-PSEUDO.github.io/TON-DEPOT/carnet-artiste.html#artist=a8f3d9e2b1c7f0e5
```
La première fois, ce secret devient automatiquement ton mot de passe artiste (rien à taper). Tu es directement en mode édition.

## 4. Installer comme application sur chaque appareil

- **Ordinateur (Chrome/Edge)** : ouvre ce même lien → icône d'installation dans la barre d'adresse (ou menu ⋮ → « Installer l'application »).
- **Android (Chrome)** : menu ⋮ → « Ajouter à l'écran d'accueil » / « Installer l'application ».
- **iPhone/iPad (Safari)** : bouton Partager → « Sur l'écran d'accueil ».

L'icône installée ouvre directement le carnet en mode artiste, en plein écran, sans barre d'adresse.

## Important

- Ne partage **jamais** ce lien avec `#artist=...` — c'est ton accès privé.
- Le lien public à partager reste simplement :
  `https://TON-PSEUDO.github.io/TON-DEPOT/carnet-artiste.html` (sans le `#artist=...`).
- Si tu perds/soupçonnes une fuite de ce secret, ouvre le panneau **Carnet → Sécurité** en mode artiste et change le mot de passe : ça invalide l'ancien lien.
