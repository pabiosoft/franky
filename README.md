<p align="center">
  <img src=".github/franky.png" width="96" height="96" alt="">
</p>

<h1 align="center">Franky</h1>

<p align="center">
  Vos projets PHP en local, prêts en un clic, sur macOS et Windows.<br>
  <a href="https://github.com/pabiosoft/franky/releases/latest"><b>Télécharger la dernière version</b></a>
</p>

Franky installe [FrankenPHP](https://frankenphp.dev) et les services dont vos projets ont besoin, puis les sert en HTTPS sur un domaine `*.localhost`. Sans Docker Compose, sans configuration à écrire.

- **Projets PHP** servis par FrankenPHP, en HTTP ou HTTPS local, avec un certificat par projet.
- **Laravel, Symfony et WordPress** détectés dans un dossier existant ou créés depuis un modèle.
- **PostgreSQL, MariaDB, Redis et Mailpit** à la demande, avec Adminer.
- **`php` et `composer`** dans votre terminal et votre éditeur, workers et rechargement à chaud.
- **Tout reste sur votre ordinateur** : services limités à `127.0.0.1`, téléchargements vérifiés.
- **Mises à jour intégrées**, vérifiées par signature.

## Installer

Sur la page de la [dernière version](https://github.com/pabiosoft/franky/releases/latest), téléchargez le fichier qui correspond à votre ordinateur :

| Système | Fichier |
| --- | --- |
| macOS, Mac Apple Silicon (M1 et suivants) | `Franky_<version>_macos-apple-silicon.dmg` |
| macOS, Mac Intel | `Franky_<version>_macos-intel.dmg` |
| Windows 10 et 11 (64 bits) | `Franky_<version>_windows-x64-setup.exe` |

Franky n'est pas encore signé par Apple ni par Microsoft : chaque système affiche un avertissement au premier lancement. C'est attendu, et on ne le fait qu'une fois. Les versions suivantes s'installent depuis Franky (Réglages › Mises à jour).

### macOS

1. Ouvrez le `.dmg` et glissez Franky dans **Applications**.
2. Ouvrez Franky depuis **Applications** (pas depuis la fenêtre du `.dmg`). macOS indique qu'il ne peut pas vérifier l'app : cliquez sur **Terminé**, pas sur *Placer dans la corbeille*.
3. Ouvrez **Réglages Système › Confidentialité et sécurité**, descendez jusqu'à « Franky a été bloqué » et cliquez sur **Ouvrir quand même**, puis confirmez avec votre mot de passe.
4. Relancez Franky depuis **Applications**. Vous pouvez ensuite éjecter le `.dmg`.

Ne désactivez pas Gatekeeper pour tout le Mac : ce n'est pas nécessaire.

### Windows

1. Lancez `…-setup.exe`. Si SmartScreen affiche « Windows a protégé votre ordinateur », cliquez sur **Informations complémentaires**, puis **Exécuter quand même**.
2. L'installation se fait pour votre compte, sans droits administrateur.

### Bases de données

Les bases de données utilisent [Podman](https://podman.io), que Franky propose d'installer : avec Homebrew sur macOS, avec winget sur Windows, où Podman a aussi besoin de WSL 2. Pour des projets PHP sans base, FrankenPHP suffit.

## Vérifier le téléchargement

Chaque version publie `SHA256SUMS.txt`. L'empreinte de votre fichier doit y figurer à l'identique :

- macOS : `shasum -a 256 Franky_*.dmg`
- Windows (PowerShell) : `Get-FileHash .\Franky_*-setup.exe`

## Aide

- **Dans l'app** : la page **Aide et docs** contient des guides pas à pas et les problèmes courants.
- **Un bug, une idée** : ouvrez une [issue](https://github.com/pabiosoft/franky/issues) en précisant votre système, la version de Franky et, si possible, les journaux (Réglages › Journaux système).

---

Franky est développé par [Pabiosoft](https://pabiosoft.com). FrankenPHP, Podman, PostgreSQL, MariaDB, Redis, Mailpit et Adminer sont des projets tiers, téléchargés depuis leurs sources officielles.
