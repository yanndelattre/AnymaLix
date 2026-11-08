# Publier et installer AnymaLix

AnymaLix est préparée comme une application web installable (PWA). Le dossier de publication est ce dossier `anymalix` : il contient la page, le manifeste, le service worker et les icônes. Il faut publier son contenu chez un hébergeur web qui fournit une adresse HTTPS. L’adresse doit rester la même pour que les installations existantes reçoivent les versions suivantes.

## Publication automatique avec GitHub Pages

Le dossier comprend un workflow GitHub Actions qui publie automatiquement AnymaLix lorsque des changements sont envoyés sur la branche `main`.

1. Créer un compte GitHub si nécessaire, puis créer un dépôt nommé `anymalix`.
2. Pour GitHub Free, choisir un dépôt **public**. Le site publié et les fichiers du dépôt seront visibles par tout le monde ; n’y placer aucune information privée.
3. Ajouter à la racine du dépôt le contenu de ce dossier, y compris le dossier caché `.github` et le fichier `.nojekyll`.
4. Dans **Settings → Pages**, régler **Source** sur **GitHub Actions**.
5. Dans l’onglet **Actions**, attendre que **Publish AnymaLix** termine avec succès. Le lien HTTPS apparaîtra ensuite dans **Settings → Pages**.

À chaque nouvelle version, remplacer les fichiers du dépôt et envoyer les changements sur `main` : le workflow republiera le site à la même adresse. Le dépôt doit contenir les fichiers de l’application à sa racine pour que le workflow fonctionne.

## Installer sur les appareils

- **Windows** : ouvrir l’adresse HTTPS dans Edge ou Chrome, puis utiliser le bouton **Installer** d’AnymaLix ou la commande d’installation du navigateur.
- **iPhone et iPad** : ouvrir l’adresse dans Safari, toucher **Partager**, puis **Sur l’écran d’accueil**.
- **Ordinateur Apple** : ouvrir l’adresse dans Safari ou Chrome et utiliser la commande d’installation/ajout proposée par le navigateur.
- **Autres téléphones et tablettes** : ouvrir l’adresse dans Chrome ou le navigateur compatible et choisir **Installer** ou **Ajouter à l’écran d’accueil**.

## Publier une mise à jour

Remplacer les fichiers publiés par ceux de la nouvelle version, en gardant la même adresse. AnymaLix vérifie les mises à jour à l’ouverture, au retour dans l’application et périodiquement pendant son utilisation. Le menu **Aide → Vérifier les mises à jour** permet de lancer une vérification manuelle. Une mise à jour détectée est activée puis l’application se recharge.

L’application doit se connecter à Internet pour récupérer une nouvelle version. La version déjà chargée reste disponible hors ligne. Les projets `.anymalix` et les fichiers de dessin sont enregistrés localement sur chaque appareil ; publier une mise à jour de l’application ne synchronise pas les projets entre appareils.

Ce dossier ne constitue pas un installateur natif `.exe` ou `.ipa` et ne publie pas l’application sur Microsoft Store ou App Store. Il fournit l’installation depuis le navigateur, avec la même version pour Windows et les appareils Apple.
