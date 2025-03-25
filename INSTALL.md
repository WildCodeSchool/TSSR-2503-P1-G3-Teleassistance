## Sommaire

1. [Prérequis technique](#prerequis-technique)
2. [Installation sur le serveur](#installation-sur-le-serveur)  
   a. [Renommer le pc](#renommer_le_pc)  
   b. [Configuration réseau](#configuration_reseau_serveur)  
   c. [Installation Ultra VNC](#installation_ultra_vnc_server)  
   d. [Désactivation du pare-feu](#desactivation_du_pare_feu_serveur)  
   e. [Droits d'accès](#droits_acces_serveur)  
4. [Installation sur le client](#installation-sur-le-client)  
   a. [Réseau VirtualBox](#virtualbox_reseau)  
   b. [Configuration réseau](#configuration_reseau_client)  
   c. [Installation Ultra VNC](#installation_ultra_vnc_client)  
   d. [Désactivation du pare-feu](#desactivation_du_pare_feu_client)  
   e. [Droits d'accès](#droits_acces_client)  
6. [FAQ](#faq)


# **Projet Réalisé sur machines virtuelles**        


# 1. Prérequis techniques
<span id="prerequis-techniques"></span>
- Un Hyperviseur de type 1, dans notre cas = [**Oracle VirtualBox 7.1.6**](https://www.virtualbox.org/wiki/Downloads)
- Serveur = **Windows Server 2022** / Client = **Windows 10 Pro** ou Ultérieur


# 2. Installation sur le serveur 
<span id="installation-sur-le-serveur"></span>


   **a. Renommer son PC**  
<span id="renommer_le_pc"></span>
Lorsque vous vous connectez au mode administrateur, le Server Manager s'affiche:  

<img src="https://github.com/user-attachments/assets/0684b79d-9733-4014-9ed8-b77793043ef9" width="600" height="400">

**ETAPE 1** : Cliquez en haut à gauche sur le nom du PC en bleu (ex: WinServ)  

<img src="https://github.com/user-attachments/assets/9f654c7f-8dfc-4de0-9060-22c42fc27c57" width="600" height="400">

**Etape 2** : Une nouvelle fênetre s'ouvre, cliquez sur le bouton "change" :

<img src="https://github.com/user-attachments/assets/0218466a-62a7-418f-9df0-4720b4e6be5a" width="600" height="400">

**Etape 3** : Dans "Computer Name" taper le nouveau nom du PC (ex: SRVWIN01)

<img src="https://github.com/user-attachments/assets/ed9de3de-e500-410f-afae-9e498fdb88d4" width="600" height="400">

**Etape 4** : Cliquez sur le bouton OK,un message s'affiche pour vous indiquer qu'il faut redémarrer le PC pour que le nom soit prit en compte
<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">



   **b. Configuration Réseau**  
<span id="configuration_reseau_serveur"></span>  

**Etape 1** : Sur le bureau, dans la barre de recherche, taper "server" ou "man", vous devriez voir apparaître l'application du Server Manager:    

<img src="Ressources/VM_WSRWIN01/1-renommer_le_pc/etape_01.png" width="600" height="400">

**Etape 2** : La fenêtre du Dashboad s'affiche, dans le menu à gauche cliquez sur "Local Server" :

<img src="https://github.com/user-attachments/assets/0218466a-62a7-418f-9df0-4720b4e6be5a" width="600" height="400">

**Etape 3** : Cliquez ensuite sur l'adresse IP (lien en bleu) de l'ethernet 2 :

<img src="https://github.com/user-attachments/assets/ed9de3de-e500-410f-afae-9e498fdb88d4" width="600" height="400">

**Etape 4** : Une nouvelle fenêtre s'affiche avec vos connexions réseaux :  

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">

**Etape 5** : Faites un clic droit sur l'icône "Ethernet 2" :  

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">

**Etape 6** : Cliquez sur "properties", une nouvelle fenêtre s'ouvre:  

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">  

**Etape 7** : Vérifier que la case "Internet Protocol Version 4 (TCP/IPv4) soit coché, sinon cochez-là, puis cliquez sur "Properties" :  

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">  

**Etape 8** : Une nouvelle fenêtre s'ouvre, séléctionnez "Use the following IP adress" et notez pour "IP adress": 172.16.10.5, puis dans Subnet mask : 255.255.255.0 , puis cliquez sur "OK" pour valider :  

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">


   **c. Installation ULTRA VNC**  
<span id="installation_ultra_vnc_server"></span>  



   **d. Désactivation du pare-feu**  
<span id="desactivation_du_pare_feu_serveur"></span>  


   **e. Droits d' accès**  
<span id="droits_acces_serveur"></span>  



# 3. Installation sur le client  
<span id="installation-sur-le-client"></span>  


   **a. Réseau VirtualBox** 
<span id="virtualbox_reseau"></span>



   **b. Configuration Réseau** 
<span id="virtualbox_reseau"></span>



   **c. Installation Ultra VNC** 
<span id="installation_ultra_vnc_client"></span>



   **d. Désactivation du pare-feu** 
<span id="desactivation_du_pare_feu_client"></span>



   **e. Droits d' accès** 
<span id="droits_acces_client"></span>



# 4. FAQ
<span id="faq"></span>        
