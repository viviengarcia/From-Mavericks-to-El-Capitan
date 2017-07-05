# Checklist de Pré-Migration


Le but de ce document est de lister les tâches à effectuer ainsi que de permettre la validation de leur progression avant de démarrer l'installation proprement dite du nouveau système.

## Checklist

### Méthode d'installation - vérifier les points suivants
- [x] compatibilité du matériel
- [x] méthode d'installation
- [x] versions des utilitaires d'installation
- [ ] problèmes rencontrés par les utilisateurs

### Tri des fichiers et des dossiers
- [x] .dotfiles
- [x] création numérique *(dû : tri et réorganisation car c'est une des seules arborescences qui va persister)*
- [x] desktop
- [x] documents
- [x] downloads
- [x] application support
    + [x] tagspaces -> transfert vers Evernote
- [x] ebooks
- [-] multimédia
    + [x] films
    + [-] images
        * [-] photos *(dû : tri des doublons à faire après migration)*
        * [x] captures
- [x] public
- [x] référentiels
- [x] ressources
    + [x] informatique *(dû : )*
    + [x] outils de création

### Dotfiles
- [x] création d'un dépot git
- [ ] création de fichiers d'installation et de configuration
    + [x] préférences bash
    + [x] préférences système, etc.
    + [x] homebrew
    + [x] cask
    + [x] mackup
    + [ ] symlinks
    + [ ] script d'installation
- [x] mise en ligne du dépot sur github

### Applications
####Voir `/_include/_pics/Applications.number`.
- [x] compatibilité des applications avec la nouvelle version du système
- [x] choix du parc applicatif
- [x] configuration des applications via Mackup
    + [x] installation de Mackup
    + [x] sauvegarde des préférences des applications
    + [x] création d'un fichier de configuration pour Mackup
- [x] configuration des applications via Dropbox + symlink
    + [x] vérifications des applications compatibles
    + [x] déplacement des préférences compatibles dans Dropbox et création de symlinks

### Ajustement du montage du pc
- [x] sélectionner les disques restants
- [ ] demontage des composants
- [ ] nettoyage/aspiration
- [ ] remontage du pc