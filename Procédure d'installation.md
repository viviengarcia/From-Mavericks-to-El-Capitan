# Procédure d'Installation


## Installation d'OSX

### Préparation

S'assurer que tout est prêt **avant** de lancer l'installation. Les informations importantes doivent rester accessibles, via Dropbox ou Github.

1. [ ] vérifier si les étapes du document "Checklist de Migration" sont cochées
2. [ ] effectuer une sauvegarde TimeMachine
3. [ ] copier les données sur le disque Data 2 et éteindre l'ordinateur.
4. [ ] brancher le Clé d'installation d'El Capitan
5. [ ] avec l'iPad, se rendre sur[Tonymacosx86.com](https://www.tonymacx86.com/threads/unibeast-install-os-x-el-capitan-on-any-supported-intel-based-pc.172672/)
6. [ ] démarrer l'ordinateur sur l'EFI et vérifier que les réglages sont compatibles avec les préconisations de [Tonymacosx86.com](https://www.tonymacx86.com/threads/unibeast-install-os-x-el-capitan-on-any-supported-intel-based-pc.172672/). Changer les réglages si nécessaire. Redémarrer. 


### Installation + Multibeast

Installation de l'OS puis utilisation de l'application Multibeast pour pouvoir démarrer directement sur le disque, ainsi que que pour avoir le support de certains matériels (notamment la puce audio). On détermine aussi un (faux) type de Mac pour qu'il soit reconnu.

1. [ ] Suivre le tutoriel sur [Tonymacosx86.com](https://www.tonymacx86.com/threads/unibeast-install-os-x-el-capitan-on-any-supported-intel-based-pc.172672/) pour installer El Capitan.
2. [ ] Choisir UEFI Boot mode, Fake SMC, et le driver audio (ALC 887).  
Système MacPro 3,1.


## Post-installation

### Préparation

#### Résolution des problèmes de permissions

Dû à la protection SIP d'El Capitan, Homebrew peut avoir des difficultés à s'installer son emplacement habituel. Si l'utilisateur courant n'est pas propriétaire de `/usr/local`, executer ces étapes :  

1. [ ] Redémarrer en Recovery mode (maintenir Cmd+R au démarrage).  
    Dans Terminal, entrer :  
    `csrutil disable`
2. [ ] Redémarrer. Dans Terminal, entrer :  
    `sudo mkdir /usr/local && sudo chflags norestricted /usr/local && sudo chown vivien:admin /usr/local && sudo chown -R vivien:admin /usr/local`
3. [ ] Redémarrer en Recovery Mode. Dans Terminal, entrer :  
    `csrutil enable`
4. Redémarrer OSX

#### Mac App Store

Installation des applications et de XCode via le Mac App Store en une seule opération via l'onglet "Purchased".

1. [ ] installation des Apps via le Mac App Store
2. [ ] Installation d'XCode et des Command Line Tools via le Mac App Store

#### Automatisation

Installation des outils nécessaires à l'automatisation (Ruby, Git, Python, NodeJS, Cask, mackup)

1. [ ] Installation des command_line tools d'XCode. Dans Terminal, entrer :  
    `xcode-select --install`
2. [ ] Installation de la dernière version de Homebrew. Dans Terminal, entrer :  
    `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

#### Homebrew
[ ] installation de Git, Ruby, Python, NodeJS, Cask et Mackup via Homebrew
1. Dans Terminal, entrer :
    `brew update`
    puis
    `brew doctor`
2. Si `brew doctor` renvoie un message d'erreur, apporter les corrections demandées et relancer la commande jusqu'à ne plus avoir de message d'erreur.
3. Une fois que `brew doctor` arrête de se plaindre, entrer
    `brew install bash git ruby dockutil mackup bash-completion2 ssh-copy-id wget tree`
    ça devrait prendre un moment
4. Puis entrer : 
    `brew tap 'caskroom/cask'`
    puis :
    `brew tap 'caskroom/versions'`
    et finalement :
    `tap 'caskroom/fonts'`

Une fois Homebrew installé et ses dépots additionnels ajoutés, récupérer les dotfiles et lancer leur déploiement puis l'exécution du script d'installation :

## Ordre d'installation

Ce document est une liste ordonnée qui décrit les étapes du processus d'installation.

1. installation des Command Line Tools via terminal ou XCode via le Mac App Store
2. installation des applications via le Mac App Store
3. installation d'homebrew via curl
4. installation de git, ruby, cask, mackup, python et bash via homebrew
5. récupération des dotfiles via git
6. execution du script d'installation
    - déploiement des liens symboliques
    - configuration de Bash
    - installation des applications via cask
    - configuration d'OS X
    - configuration des applications via mackup
7. configuration des applications via création de liens symboliques vers dropbox
8. configuration manuelle du système via System Preferences
9. installation manuelle des applications
10. configuration manuelle des applications


## Post-installation

[ ] configuration de l'emplacement du dossier utilisateur
[ ] Configuration de Hazel
[ ] Test des apps spécialisées dans la gestiond des documents/fichiers/tags (Hazel/Together/Leap/Yep)
[ ] Application des tags sur l'ensemble des Datas
[ ] Import des Datas dans le dossier Dropbox
[ ] Création de la structure de dossiers, dossiers intelligents et alias

#### Tri des fichiers et dossiers
- [ ] Multimédia
    + [ ] Musique
    + [ ] Photos -> analyse des fichiers via une app spécialisée à définir (PhotoSweeper ?)
- [ ] Firefox -> Transfert des Scraps vers Evernote
    + [ ] Scrapbook 1
    + [ ] Scrapbook 2
    + [ ] Scrapbook X
- [ ] Pinboard -> Migration vers Evernote
- [ ] Evernote -> Sélection des éléments les plus pertinents et élimination des doublons et liens morts
- [ ] Création Numérique -> Réorganisation arborescence + tri
    + [ ] _Perso
        * [ ] Photo Noël

