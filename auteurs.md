# ISS_TP1_TTT_MD
# Travaux Pratique 1
 
## 2023-06-06
### Tenekeu Tene Thomas
###  Maxime Dubois

#### Dans le cadre de **INSTALLATION DES SERVEURS ET DES SERVICES** le professeur nous a demandé 
#### d'expliquer la procédure pour installer un serveur.

## Sites de référence:
##### https://lecrabeinfo.net/installer-ubuntu-22-04-lts-le-guide-complet.html
#### https://doc.ubuntu-fr.org/gestionnaire_de_mises_a_jour#:~:text=Sous%20Kubuntu%20%3A%20Applications%E2%86%92Syst%C3%A8me,%2Dmanager%20%C2%BB%20depuis%20un%20terminal.
##### https://github.com/claude-roy/420-W45-SF_4371/blob/main/Exercices/Exercice02_InstallationServeur.md

# Etapes d'installation d'un serveur

## Caractérisation de la machine serveur ::

#### - Dossier dans vSphere : DFC DS/VM DFC/E23_4371_420W45_ISS_CR/
##### - Nom hostname
##### - Un utilisateur avec pour nom d'utilisateur: 'nomDeVotreChoix'
##### - Un port HTTP : 80 HTTPS : 443
##### - CPU: 2
#### - Storage (disque vSphere) : ESXDFC2
##### - Mémoire 4 Go
##### - Disque dur : 2 disques, 20 Go chacun en **partitionnement dynamique (Thin provision)**
##### - Carte réseau : VM DFC2 (réseau 10.100.2.0)
##### - CD/DVD : Ubuntu 22.04 LTS

## Les mises à jour préalables à l'installation et ajout de composants nécessaires

### Une fois la VM créée, lancez la VM et installez le serveur Ubuntu selon les spécifications suivantes :

##### Pour vous déplacer dans les fenêtres, utiliser votre touche tabulation. Pour sélectionner un item, appuyez sur la touche Entrée(enter). Pour cocher un item cliqué sur la barre d'espacement.

##### L’installeur d’Ubuntu, alias Ubiquity, se lance. 
##### Sélectionnez la langue Française puis cliquez sur le bouton Installer maintenant

##### Vous avez également la possibilité de tester Ubuntu sans l’installer en sélectionnant Essayer Ubuntu (les données nécessaires au fonctionnement de l’OS seront copiés dans la mémoire vive) puis de lancer l’installation depuis l’icône sur le Bureau

##### Indiquez la disposition de votre clavier : Selectionnez French Canada 


### À l’écran suivant, sélectionnez les options suivantes :
##### Installation normale ou minimale : l’installation minimale installe la base du système, l’environnement graphique, un navigateur web et quelques outils. Et c’est tout ! Environ 80 paquets sont supprimés, parmi lesquels Thunderbird, Transmission, Rythmbox, LibreOffice, Cheese ou Shotwell. L’installation occupe 3,5 Go d’espace, contre 4 Go en moyenne pour l’installation normale.
##### Télécharger les mises à jour pendant l’installation de Ubuntu.
##### Installer un logiciel tiers pour le matériel graphique et Wi-Fi et des formats de média supplémentaires : installe le paquet ubuntu-restricted-addons (qui contient des codecs audio et vidéo) et les drivers nécessaires au support des cartes Wi-Fi et cartes graphiques.


### - Le Type d'installation selectionner : Ubuntu Server

##### En cliquant sur le bouton Fonctions avancées, vous avez la possibilité de chiffrer Ubuntu (avec LVM) et d’utiliser le système de fichiers ZFS

##### Sélectionnez votre pays puis faites Continuer.



### - Configuration du profil :

##### Votre nom : ;-)
##### Le nom de la machine: hostname
##### Nom d'utilisateur : à votre choix
##### Mot de passe : à votre choix


### - Configuration SSH : Cochez Installer le serveur OpenSSH (taper sur la barre d'espace) 
#####  N'importez pas la clé SSH.  

##### -  Featured Server Snaps ne cocher rien et choisit Terminé

##### - Patientez! L'INSTALLATION EST EN COURS.

##### Redemarer votre serveur avec la commande: **reboot**

## Procédure de validation de l'installation.

#### Mettre à jour les système avec les commandes:
#### sudo apt update
#### sudo apt upgrade

#### verifier les partitions avec la commande avec la commande: df -h
#### Vérifier la version d'ubuntu avec la commande: lsb_release -a
#### Vérifier l'état du système: systemctl avec la commande: status
#### Vérifier l'utilisation des ressources avec la commande: top
#### Vérifier les connexions réseau actives avec la commande: netstat -tuln
#### Vérifier l'interface réseau avec la commande: ip addr show
