## Installation (app non signée)

Ces builds ne sont ni signés ni notarisés par Apple. Au premier lancement, macOS peut dire que l'app « est endommagée » ou « ne peut pas être ouverte ». Après l'avoir copiée dans Applications :

```bash
xattr -cr "/Applications/Nebula News.app"
```

ou bien clic droit → Ouvrir. Fichiers : `-arm64` pour les Mac Apple Silicon (M1 et suivants), `-x64` pour les Mac Intel.

La mise à jour automatique intégrée ne fonctionne pas sur macOS pour une app non signée : installez simplement la release Mac suivante.

## Limites connues sur macOS
- Apple Silicon uniquement (le moteur Prisma embarqué est natif arm64).
- Icône Electron par défaut (le dépôt d'origine ne fournit qu'une icône `.ico`).
- Au tout premier lancement, l'accueil reste vide jusqu'à la première collecte d'articles (environ 20 s) : changez de page ou relancez.
