# Etapes d'installation d'un serveur

## Caractérisation de la machine serveur :

      - Dossier dans vSphere : DFC DS/VM DFC/E23_4371_420W45_ISS_CR/
      - Nom hostname
      - Un utilisateur avec pour nom d'utilisateur: 'nomDeVotreChoix'
      - Un port HTTP : 80 HTTPS : 443
      - CPU: 2
      - Storage (disque vSphere) : ESXDFC2
      - Mémoire 2 Go
      - Disque dur : 2 disques, 20 Go chacun en **partitionnement dynamique (Thin provision)**
      - Carte réseau : VM DFC2 (réseau 10.100.2.0)
      - CD/DVD : ISO ubuntu-22.04-live-server-amd64.iso

## Instalation Serveur
Pour vous déplacer dans les fenêtres, utiliser votre touche tabulation. Pour sélectionner un item, appuyez sur la touche Entrée(enter). Pour cocher un item cliqué sur la barre d'espacement.

L’installeur d’Ubuntu, alias Ubiquity, se lance. Installez le serveur Ubuntu selon les spécifications suivantes.

### Configurer la langue
Sélectionnez la langue Française puis cliquez 'Enter'
![langueSysteme](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/86843996/22d462da-7d7b-4d86-b635-5b587b45d4e9)

### Configurer le clavier
Selectionnez 'French Canada'
![langueClavier](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/86843996/46845cec-4086-4fba-ad24-5d2b9538c3dd)

### Connection réseau
Selectionnez : DHCPv4
![reseau](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/86843996/360d08d8-26ad-4807-aed4-35dd762174b0)

### Configurer le proxy
Choisit 'Terminé'
![proxy](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/86843996/4dff2853-ca82-48f9-9628-7588a5ffe395)

### Configure ubuntu archive miroir
Choisit 'Terminé'
![miroir](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/86843996/4e5ecf7c-9238-411a-bd67-ebfa4ad2ae81)

### Guide de configuration de stockage
Choisit 'Terminé'
![stoquage](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/86843996/c2dc63c4-86ca-4be1-861a-dd13f09d1cda)

### Configuration de stockage 
Choisit 'Terminé'
![comfiquration](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/86843996/7a56147d-b612-4717-8235-033de552d6cd)

### Configuration du profil

      Votre nom : 'nomDeVotreChoix'
      Le nom de la machine: 'hostname'
      Nom d'utilisateur : 'nomDeVotreChoix'
      Mot de passe : 'deVotreChoix'

![profil](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/86843996/5c730b9f-dd70-4f84-950c-0aff04920b4f)

### Configuration SSH 
Cochez Installer le serveur OpenSSH (taper sur la barre d'espace)

N'importez pas la clé SSH.
![ssh](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/86843996/f4cc67f8-8135-4963-8254-229ff599d274)


### Execution du server snaps
Ne cocher rien et choisit 'Terminé'
![snap](https://github.com/Tenekeu0/ISS_TP1_TTT_MD/assets/86843996/f5632f8e-e0d5-4119-b5ff-f5f66d3453e8)

#### Patientez! L'INSTALLATION EST EN COURS.

#### Retire le DVD

#### Redemarer votre serveur avec la commande:
```
reboot
```
## Techniques pour sécuriser votre serveur SSH
#### Ouvrez le fichier de configuration du serveur ssh avec cette commande
```
sudo nano /etc/ssh/sshd_config
# ou
sudo vim /etc/ssh/sshd_config
```
#### Désactiver les mots de passe vides 
  - PermitEmptyPasswords no
#### Changer le port SSH
  - changer le port 22 en port 2522 
#### Supprimer le #
#### Redémarrez le démon ssh avec
  - sudo systemctl restart sshd.service
#### Vérifier que la connexion de root est désactivée avec l'option 
  - PermitRootLogin no
#### Configurer le délai d'inactivité
  - ClientAliveInterval 300
### Autoriser l'accès SSH à des utilisateurs sélectionnés uniquement
  - AllowUsers User1 User2
 
### Installation des programmes
#### Installez docker avec la commade
```
sudo apt install docker
```
##### Utilisez cette commande pour vérifier son UID et son GID
```
id docker
```
#### Installez mysql-server avec  la commade
```
sudo apt install mysql-server
```
son UID et GID : mysql

#### installez nginx avec  la commade
```
sudo apt install nginx
```
##### Utilisez cette commande pour vérifier son UID et son GID
```
id nginx
```
#### installez php avec  la commade
```
sudo apt install php
```
##### Utilisez cette commande pour vérifier son UID et son GID
```
id php
```

## Procédure de validation de l'installation

#### Mettre à jour les système avec les commandes:
```
sudo apt update && sudo apt full-ugrade -y
```

#### Verifier les partitions avec la commande avec la commande: 
```
df -h
```
#### Vérifier la version d'ubuntu avec la commande: 
```
lsb_release -a
```
#### Vérifier l'état du système avec la commande : 
```
systemctl 
```
quité avec 'q'
#### Vérifier l'utilisation des ressources avec la commande: 
```
top
```
#### Vérifier les connexions réseau actives avec la commande: 
```
netstat -tuln
```
#### Vérifier l'interface réseau avec la commande: 
```
ip addr show
```

## Sites de référence:
#### https://doc.ubuntu-fr.org/gestionnaire_de_mises_a_jour#:~:text=Sous%20Kubuntu%20%3A%20Applications%E2%86%92Syst%C3%A8me,%2Dmanager%20%C2%BB%20depuis%20un%20terminal.
##### https://github.com/claude-roy/420-W45-SF_4371/blob/main/Exercices/Exercice02_InstallationServeur.md
#### https://github.com/claude-roy/420-W45-SF_4371/blob/main/Exercices/Exercice03_PriseEnMainSrv.md
