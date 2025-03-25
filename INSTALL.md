## Sommaire

1. [Prérequis technique](#prerequis-technique)
2. [Installation sur le serveur](#installation-sur-le-serveur)  
   a. [Renommer le pc](#renommer_le_pc)  
   b. [Configuration réseau](#configuration_reseau_serveur)  
   c. [Installation Ultra VNC](#installation_ultra_vnc_server)  
   d. [Désactivation du pare-feu](#desactivation_du_pare_feu_serveur)  
   e. [Droits d'accès](#droits_acces_serveur)  
3. [Installation sur le client](#installation-sur-le-client)  
   a. [Réseau VirtualBox](#virtualbox_reseau)  
   b. [Configuration réseau](#configuration_reseau_client)  
      1. [Adressage réseau](#adressage_reseau)  
      2. [Liaison nom et adresse IP](#liaison_nom_adresse_ip)  
   c. [Installation Ultra VNC](#installation_ultra_vnc_client)  
   d. [Désactivation du pare-feu](#desactivation_du_pare_feu_client)  
   e. [Droits d'accès](#droits_acces_client)  
4. [FAQ](#faq)


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

<img src="https://github.com/user-attachments/assets/3649b699-7516-400a-aad9-8001bf936266" width="600" height="400">

**Etape 2** : La fenêtre du Dashboad s'affiche, dans le menu à gauche cliquez sur "Local Server" :

<img src="https://github.com/user-attachments/assets/e148995a-660e-4d62-935e-a6f37fce0033" width="600" height="400">

**Etape 3** : Cliquez ensuite sur l'adresse IP (lien en bleu) de l'ethernet 2 :

<img src="https://github.com/user-attachments/assets/00a41860-3262-449a-80fd-a9bd7621dbf4" width="600" height="400">

**Etape 4** : Une nouvelle fenêtre s'affiche avec vos connexions réseaux :  

<img src="https://github.com/user-attachments/assets/a3b614e1-dcb4-4cab-b8bd-a83c16aa851e" width="600" height="400">

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

**Etape 1** : Ouvrez votre navigateur internet et tapez "ultravnc" et cliquez sur le premier lien (logiquement cela devrait être le lien officiel  https://uvnc.com) :  

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">


**Etape 2** : Vous arrivez sur la page d'accueil du site :  

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">


**Etape 3** : Descendez jusqu'à la section download et cliquez sur le lien bleu "download ultravnc 1.4.3.6" (la plus récente à l'heure actuelle; il y a une version en développement mais nous nous contenterons de la dernière version finalisé qui est suffisante et fonctionnelle)  :  

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">

**Etape 4** : Vous arrivez sur une nouvelle page de téléchargement de la version 1.4.3.6  :  

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">

**Etape 5** : Descendez jusqu'à la section download et cliquez sur le lien bleu "download ultravnc 1.4.3.6" encore une fois  :  

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">

**Etape 6** : Vous arrivez sur une nouvelle page :

<img src="https://github.com/user-attachments/assets/63e16a63-f2f0-4cda-8070-9fd7dc46b95b" width="600" height="400">

**Etape 7** : Descendez jusqu'à voir ultravnc 1436 X64 setup, cliquez sur le bouton orange "Download"  
Nb : Si vous êtes en 32 bits, séléctionnez la version X86, si vous êtes en 64 bits séléctionnez la version X64  
Pour connaître l'architecture de votre PC, allez dans le panneau de configuration...................



**Etape 8** : Une fenêtre s'ouvre avec un décompte avant de pouvoir télécharger votre fichier.


**Etape 9** : Cliquez sur le bouton "I accept the above conditions", puis cliquez sur le bouton orange "Download"

**Etape 10** : Une fois le téléchargement terminé, ouvrez votre dossier où est téléchargé votre executable, dans l'exemple ("download")

**Etape 11** : Une fenêtre s'ouvre avec votre exécutable

**Etape 12** : Faites un clic droit dessus et cliquez sur "Run as administrator"

**Etape 13** : Cliquez sur OK

**Etape 14** : Séléctionnez "I accept the agreement", puis cliquez sur "Next"

**Etape 15** : Cliquez sur Next

**Etape 16** : Cochez la case "UltraVNC Viewer" puis cliquez sur "Next"

**Etape 17** : Cochez la case "Create UltraVNC desktop icons" puis cliquez sur "Next"

**Etape 18** : Cliquez sur "Install"

**Etape 19** : Cliquez sur "Next"

**Etape 20** : Cliquez sur "Finish"

   **d. Désactivation du pare-feu**  
<span id="desactivation_du_pare_feu_serveur"></span>  

**Etape 1** : Sur le bureau, dans la barre de recherche, tapez "Firewall", puis cliquez sur l''application "Windows Defender Firewall with Advanced Security"


**Etape 2** : Une novuelle fenêtre s'ouvre, cliquez sur le lien bleu "Windows Defender Firewall Properties"

**Etape 3** : Une novuelle fenêtre s'ouvre et vous arrivez sur l'onglet "Domain Profile", dans Firewall state séléctionnez "off"

**Etape 4** : Cliquez sur l'onglet "Private Profile", dans Firewall state séléctionnez "off"

**Etape 5** : Cliquez sur l'onglet "Public Profile", dans Firewall state séléctionnez "off" , puis cliquez sur le bouton "Apply", puis "OK"


   **e. Droits d' accès**  
<span id="droits_acces_serveur"></span>  

**Etape 1** : Sur le bureau, dans la barre de recherche, tapez "Setting", puis cliquez sur l'application "Settings"

**Etape 2** : Une nouvelle fenêtre s'ouvre, cliquez sur "Accounts"

**Etape 3** : Sur le bureau, dans la barre de recherche, tapez "Setting", puis cliquez sur l'application "Settings"

**Etape 4** : Dans le menu à gauche, cliquez sur " Other users"


**Etape 5** : Cliquez sur l'utilisateur (dans l'exemple : Wilder) et cliquez sur "Change account type"


**Etape 6** : Dans "Account type" sélectionnez "Standard User"


**Etape 7** : Cliquez sur le bouton "OK"

**Etape 8** : L'utilisateur "Wilder" est maintenant sélectionné en Local account. Fermez la fenêtre.

**Etape 9** : Sur le bureau, dans la barre du menu, cliquez sur l'icône de la fenêtre Windows tout en bas à gauche et cliquez sur "Change account settings"

**Etape 10** : Séléctionnez "Wilder", puis entrez votre mot de passe (par défaut : Azerty1*)

**Etape 11** : Sur le bureau, dans la barre de recherche, tapez "Ultra" et cliquez sur l'icône de l'application "UltraVNC Viewer"

**Etape 12** : L'application s'ouvre

**Etape 13** : Entrez l'adresse IP du PC client (ici: 172.16.10.10)

**Etape 7** : Cliquez sur le bouton "OK"

**Etape 7** : Cliquez sur le bouton "OK"

**Etape 7** : Cliquez sur le bouton "OK"
<img src="https://github.com/user-attachments/assets/57b250c5-819c-4419-872f-861de0eb5eb3" width="600" height="400">!


**Etape 7** : Cliquez sur le bouton "OK"!








# 3. Installation sur le client  
<span id="installation-sur-le-client"></span>  


   **a. Réseau VirtualBox** 
<span id="virtualbox_reseau"></span>

**Etape 1** : Lancez VirtualBox et cliquez sur votre machine virtuelle (dans l'exemple : Win01), puis cliquez sur la roue crantée en orange "Configuration"


**Etape 2** : Sélectionnez le mode Expert


**Etape 3** : Cliquez sur "Réseau"


**Etape 4** : Cliquez sur "Adapter 2", puis dans "Mode d'accès réseau" séléctionnez "Réseau interne", enfin cliquez sur le bouton "OK"


**Etape 5** : Vous pouvez lancer votre machine virtuelle




   **b. Configuration Réseau** 
<span id="virtualbox_reseau"></span>

        1. Adressage réseau
<span id="adressage_reseau"></span> 


       2. Liaison nom et adresse IP
<span id="liaison_nom_adresse_ip"></span> 




   **c. Installation Ultra VNC** 
<span id="installation_ultra_vnc_client"></span>



   **d. Désactivation du pare-feu** 
<span id="desactivation_du_pare_feu_client"></span>



   **e. Droits d' accès** 
<span id="droits_acces_client"></span>



# 4. FAQ
<span id="faq"></span>        
