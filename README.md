# Astaghfirullah

Un jardin contemplatif qui évolue avec les répétitions d’« Astaghfirullah ». Site statique en français, adapté au mobile, sans installation de dépendances.

## Utilisation

Servir le dossier avec `python3 -m http.server 8080`, puis ouvrir http://localhost:8080. Le microphone fonctionne sur localhost ou en HTTPS, selon la prise en charge du navigateur. Le bouton manuel reste disponible. La transcription n’est pas infaillible ; seules les expressions reconnues dans les résultats définitifs sont comptées. Le navigateur peut envoyer l’audio à son fournisseur de reconnaissance vocale. L’application ne conserve pas l’audio.

La progression est conservée dans localStorage sur l’appareil. Export/import JSON permettent de la sauvegarder et de la transférer. Pas de compte ni de synchronisation serveur. Éviter de réciter dans plusieurs onglets simultanément : la dernière sauvegarde l’emporte.

## Progression

- Départ : terre aride ; une goutte animée à chaque répétition.
- 10 000 : premier arbre ; 25 000 : jardin fleuri.
- 100 000 : bosquet ; 500 000 : forêt ; 1 000 000 : forêt de géants.
- Un arbre supplémentaire par tranche de 10 000 gouttes (affichage plafonné à 80 arbres). Les arbres grandissent jusqu’au palier d’un million.
- Bouton admin : +1 000 000 sans animation. Bouton de remise à zéro : efface les compteurs, le jardin et les succès après confirmation, en conservant l’objectif quotidien.
- Objectif quotidien : 10 000 par défaut, réglable de 100 à 1 000 000. La récompense illumine le jardin pour la journée. Les jours suivent la date locale de l’appareil.
- Six succès permanents, dont 1 000 répétitions par jour pendant sept jours consécutifs.

Ces objectifs sont des mécanismes de motivation personnels, sans promesse religieuse associée.

## GitHub Pages

Créer un dépôt GitHub nommé `astaghfirullah`, puis y pousser ces fichiers sur la branche `main`. Dans **Settings → Pages → Build and deployment → Source**, choisir **GitHub Actions**. Le workflow `.github/workflows/pages.yml` publie automatiquement le site. L’adresse sera `https://mounirdark.github.io/Astaghfirullah/`.

```sh
git init -b main
git add .
git commit -m "Create Astaghfirullah garden"
git remote add origin https://github.com/mounirdark/Astaghfirullah.git
git push -u origin main
```

Le site utilise Google Fonts avec des polices système de secours. Aucun outil d’analyse n’est installé.
