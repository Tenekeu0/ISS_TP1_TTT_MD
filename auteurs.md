# ISS_TP1_TTT_MD
# Travaux Pratique 1
 
## 2023-06-06
###  Maxime Dubois
### Tenekeu Tene Thomas

#### Dans le cadre de **INSTALLATION DES SERVEURS ET DES SERVICES** le professeur nous a demandé 
#### d'expliquer la procédure pour installer un serveur.

# Etapes d'installation d'un serveur
##### Créez une machine virtuelle selon les spécifications suivantes:
#### - CPU: 2
#### - Mémoire 4 Go
### - Disque dur : 2 disques, 20 Go chacun en **partitionnement dynamique (Thin provision)**
### - Carte réseau : VM DFC2 (réseau 10.100.2.0)
### - CD/DVD : Ubuntu 22.04 LTS

# Une fois la VM créée, lancez la VM et installez le serveur Ubuntu selon les spécifications suivantes :

## Pour vous déplacer dans les fenêtres, utiliser votre touche tabulation. Pour sélectionner un item, appuyez sur la touche Entrée(enter). Pour cocher un item cliqué sur la barre d'espacement.

### L’installeur d’Ubuntu, alias Ubiquity, se lance. 
### Sélectionnez la langue French (Canada) ou English (US) puis cliquez sur le bouton Installer maintenant
![installer-ubuntu-installation-ubuntu-22-04-lts-625fc3be21fb5](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/72732730/a9750241-91d9-4f08-9685-aa9af5972918)

### - Le Type d'installation selectionner : Ubuntu Server
### - Connexions réseau : DHCPv4
### - Configurer le proxy : Laissez vide et cliquer Terminé.
### - Miroir d'archive Ubuntu : ne rien changer et cliquer sur Terminé.

### - Configuration de stockage guidée :
### Utiliser un disque entier
###     Laisser "Set up this disk as an LMV group"

###     Confirmer l'action même s’il est en rouge.

## - Configuration du profil :

### Votre nom : ;-)
### Le nom de la machine 
### Nom d'utilisateur : à votre choix
### Mot de passe : à votre choix

## - Configuration SSH : Cochez Installer le serveur OpenSSH (taper sur la barre d'espace) 
##  N'importez pas la clé SSH.  

## -  Featured Server Snaps ne cocher rien et choisit Terminé

## - Patientez! L'INSTALLATION EST EN COURS.

## Redemarer votre serveur avec la commande: **reboot**
