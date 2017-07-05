# Manifeste de Migration

Le but de ce document est de définir les moyens et objectifs de la migration de mon système informatique actuel vers sa nouvelle version majeure. I décrit la préparation, l'installation et la configuration ainsi que les éléments qui s'y rapportent.  

Une nouvelle version de ce document doit être rédigée pour chaque nouvelle migration.

## Objectifs

La migration doit être sûre, rapide et rester simple à exécuter.

Sûreté : la préparation inclut le tri et la sauvegarde des données ainsi que la vérification de la compatibilté des applications et du matériel (Hackintosh).  

Rapidité et simplicité : l'intervention humaine est limitée pendant l'installation. La configuration de l'OS ainsi que l'installation et la configuration des applications sont automatisables via l'éxecution de scripts dans un terminal.

## Moyens et détails

Différents outils et méthodes permettent d'atteindre les objectifs.

###Préparation

#### Tri des données

Recherche et suppression des doublons et des données inutiles, obsolètes ou qui ne correspondent pas à l'utilisation prévue de l'ordinateur (voir le document "Manifeste d'Utilisation").  

Reclassement des données dans l'arborescence des dossiers ou via l'application de Tags.

#### Sauvegarde

Les données triées et classées sont placées sur un disque physique séparé qui servira de nouvel espace utilisateur. Elles sont dupliquées via TimeMachine. Une fois l'installation terminées, la majorité des données sera placée dans le dossier Dropbox pour une duplication en ligne et une résilience accrue.

#### Tri logiciel

Recherche des applications qui ne pourront plus s'executer sur le nouveau système ou qui ne conviennent plus à l'utilisation prévue.

#### Compatibilté matérielle

Compatibilté des périphériques avec le nouvel OS. Recherche d'informations sur les sites spécialisés, et vérification des réglages de l'EFI préconisés par `http://tonymacx86.com`.

### Installation de l'OS

Procédure simple basée sur une clé USB et les réglages de l'EFI préconisés par http://tonymacx86.com

### Post Installation

Après l'installation de l'OS, installation des apps et de XCode via le Mac App Store, puis préparation à l'automatisation avec l'installation de Ruby, Git, Python, NodeJS, Cask et mackup).  

Installation des Dotfiles et des applications supportées par Cask, puis installation manuelle des applications restantes.  

Configuration de l'OS et des applications via Dotfiles, Mackup, Dropbox, et finalement manuellement.

