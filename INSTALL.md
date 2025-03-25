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

<img src="https://github.com/user-attachments/assets/a3769acf-2343-4665-9d66-227d571f18ef" width="600" height="400">

**Etape 6** : Cliquez sur "properties", une nouvelle fenêtre s'ouvre:  

<img src="https://github.com/user-attachments/assets/488251b8-95cf-4813-8ccb-e04c61af2822" width="600" height="400">  

**Etape 7** : Vérifier que la case "Internet Protocol Version 4 (TCP/IPv4) soit coché, sinon cochez-là, puis cliquez sur "Properties" :  

<img src="https://github.com/user-attachments/assets/60c9d0bf-79cd-44f6-801a-75073ab7b95a" width="600" height="400">  

**Etape 8** : Une nouvelle fenêtre s'ouvre, séléctionnez "Use the following IP adress" et notez pour "IP adress": 172.16.10.5, puis dans Subnet mask : 255.255.255.0 , puis cliquez sur "OK" pour valider :  

<img src="https://github.com/user-attachments/assets/4fe3d904-735a-43fa-accb-23ad9030dcfc" width="600" height="400">


   **c. Installation ULTRA VNC**  
<span id="installation_ultra_vnc_server"></span>  

**Etape 1** : Ouvrez votre navigateur internet et tapez "ultravnc" et cliquez sur le premier lien (logiquement cela devrait être le lien officiel  https://uvnc.com) :  

<img src="https://github.com/user-attachments/assets/b6146973-dabb-4412-b4cf-75201005a19b" width="600" height="400">


**Etape 2** : Vous arrivez sur la page d'accueil du site :  

<img src="https://github.com/user-attachments/assets/b5d4d41c-bd01-40e9-a03e-93980b531d7d" width="600" height="400">


**Etape 3** : Descendez jusqu'à la section download et cliquez sur le lien bleu "download ultravnc 1.4.3.6" (la plus récente à l'heure actuelle; il y a une version en développement mais nous nous contenterons de la dernière version finalisé qui est suffisante et fonctionnelle)  :  

<img src="https://github.com/user-attachments/assets/e59a612b-1689-497b-86d6-6e40fdb74a28" width="600" height="400">

**Etape 4** : Vous arrivez sur une nouvelle page de téléchargement de la version 1.4.3.6  :  

<img src="https://github.com/user-attachments/assets/87be99f6-8096-4cd0-b4f3-0563ef5ffbfd" width="600" height="400">

**Etape 5** : Descendez jusqu'à la section download et cliquez sur le lien bleu "download ultravnc 1.4.3.6" encore une fois  :  

<img src="https://github.com/user-attachments/assets/e645fc83-d98e-4432-9620-11c900d14f95" width="600" height="400">

**Etape 6** : Vous arrivez sur une nouvelle page :

<img src="https://github.com/user-attachments/assets/d0a6d84c-efbe-46bb-a3fa-997e88782160" width="600" height="400">

**Etape 7** : Descendez jusqu'à voir ultravnc 1436 X64 setup, cliquez sur le bouton orange "Download"  
Nb : Si vous êtes en 32 bits, séléctionnez la version X86, si vous êtes en 64 bits séléctionnez la version X64  
Pour connaître l'architecture de votre PC, allez dans le panneau de configuration...................

<img src="https://github.com/user-attachments/assets/1a39e9e3-e34b-4e8d-86fa-5eb45f0aebd4" width="600" height="400">


**Etape 8** : Une fenêtre s'ouvre avec un décompte avant de pouvoir télécharger votre fichier.
<img src="https://github.com/user-attachments/assets/aaec19fa-f246-482c-8a6c-a1db43f99064" width="600" height="400">

**Etape 9** : Cliquez sur le bouton "I accept the above conditions", puis cliquez sur le bouton orange "Download"
<img src="https://github.com/user-attachments/assets/0fdaca98-0afa-4ac0-823a-7ae82efabb94" width="600" height="400">  

**Etape 10** : Une fois le téléchargement terminé, ouvrez votre dossier où est téléchargé votre executable, dans l'exemple ("download")
<img src="https://github.com/user-attachments/assets/b2dc52ec-e958-4724-8b81-a1b998b274dd" width="600" height="400">  

**Etape 11** : Une fenêtre s'ouvre avec votre exécutable  
<img src="https://github.com/user-attachments/assets/6aab6c72-fcf5-4e93-850d-2c9ff5e94adc" width="600" height="400">  

**Etape 12** : Faites un clic droit dessus et cliquez sur "Run as administrator"  
<img src="https://github.com/user-attachments/assets/a0bee6d3-2172-4f1a-8338-a39ffc2fb493" width="600" height="400">  

**Etape 13** : Cliquez sur OK  
<img src="https://github.com/user-attachments/assets/9f800f87-eabc-4186-a72c-14074dae8198" width="600" height="400">  

**Etape 14** : Séléctionnez "I accept the agreement", puis cliquez sur "Next"  
<img src="https://github.com/user-attachments/assets/791edb90-e35f-4b01-ad23-2750d54fddea" width="600" height="400">  

**Etape 15** : Cliquez sur Next  
<img src="https://github.com/user-attachments/assets/213fd4e6-1d35-4cff-add6-4e82f96760da" width="600" height="400">  

**Etape 16** : Cochez la case "UltraVNC Viewer" puis cliquez sur "Next"  
<img src="https://github.com/user-attachments/assets/1404779c-7682-4d0e-a3e7-20efba772391" width="600" height="400">  

**Etape 17** : Cochez la case "Create UltraVNC desktop icons" puis cliquez sur "Next"  
<img src="https://github.com/user-attachments/assets/52cb97b0-625d-48c9-ac02-61e8376d5d64" width="600" height="400">  

**Etape 18** : Cliquez sur "Install"  
<img src="https://github.com/user-attachments/assets/e4788497-71b2-4669-8032-13c4321d9a31" width="600" height="400">  

**Etape 19** : Cliquez sur "Next"  
<img src="https://github.com/user-attachments/assets/c286c3f1-ed63-4764-9475-de3ff04cab15" width="600" height="400">  

**Etape 20** : Cliquez sur "Finish"  
<img src="https://github.com/user-attachments/assets/d69b28eb-745c-4eda-a9ef-6f1df44d95c4" width="600" height="400">  

   **d. Désactivation du pare-feu**  
<span id="desactivation_du_pare_feu_serveur"></span>  

**Etape 1** : Sur le bureau, dans la barre de recherche, tapez "Firewall", puis cliquez sur l''application "Windows Defender Firewall with Advanced Security"  
<img src="https://github.com/user-attachments/assets/06937f9e-e52e-4d5f-b86d-1129b0a0ad09" width="600" height="400">

**Etape 2** : Une nouvuelle fenêtre s'ouvre, cliquez sur le lien bleu "Windows Defender Firewall Properties"  
<img src="https://github.com/user-attachments/assets/bf8fcfa7-fad4-410e-9545-f37e746f5897" width="600" height="400">

**Etape 3** : Une nouvelle fenêtre s'ouvre et vous arrivez sur l'onglet "Domain Profile", dans Firewall state séléctionnez "off"  
<img src="https://github.com/user-attachments/assets/77a7282e-bae7-423b-b58e-866e08ca3081" width="600" height="400">

**Etape 4** : Cliquez sur l'onglet "Private Profile", dans Firewall state séléctionnez "off"  
<img src="https://github.com/user-attachments/assets/a79c713c-3f7e-4d0d-a59b-072f735e3790" width="600" height="400">  

**Etape 5** : Cliquez sur l'onglet "Public Profile", dans Firewall state séléctionnez "off" , puis cliquez sur le bouton "Apply", puis "OK"  
<img src="https://github.com/user-attachments/assets/242e478d-178e-48a2-b2b7-07c1a6c12c0e" width="600" height="400">


   **e. Droits d' accès**  
<span id="droits_acces_serveur"></span>  

**Etape 1** : Sur le bureau, dans la barre de recherche, tapez "Setting", puis cliquez sur l'application "Settings"  
<img src="https://github.com/user-attachments/assets/da853e0d-7dc5-4a0e-afdc-ef4b3dbb791e" width="600" height="400">  

**Etape 2** : Une nouvelle fenêtre s'ouvre, cliquez sur "Accounts"  
<img src="https://github.com/user-attachments/assets/2d0941c8-c6df-4cff-9875-3b6b4c10e3ac" width="600" height="400">  

**Etape 3** : Sur le bureau, dans la barre de recherche, tapez "Setting", puis cliquez sur l'application "Settings"  
<img src="https://github.com/user-attachments/assets/720942f8-f83d-4c99-93b3-d7d2ef521e13" width="600" height="400">  

**Etape 4** : Dans le menu à gauche, cliquez sur " Other users"  
<img src="https://github.com/user-attachments/assets/d8fe9ee7-9a65-4ed4-a6bf-5344a1295473" width="600" height="400">  

**Etape 5** : Cliquez sur l'utilisateur (dans l'exemple : Wilder) et cliquez sur "Change account type"  
<img src="https://github.com/user-attachments/assets/806e5697-f708-4e2a-83d0-adf8b89b0058" width="600" height="400">  

**Etape 6** : Dans "Account type" sélectionnez "Standard User"  
<img src="https://github.com/user-attachments/assets/cccd9b88-d3fa-4177-ad92-f8dcf004a555" width="600" height="400">  

**Etape 7** : Cliquez sur le bouton "OK"  
<img src="https://github.com/user-attachments/assets/148c9cd0-d35d-4746-aee8-8aed24469d95" width="600" height="400">  

**Etape 8** : L'utilisateur "Wilder" est maintenant sélectionné en Local account. Fermez la fenêtre.  
<img src="https://github.com/user-attachments/assets/1e353067-96dd-4803-b9b6-2b94d685cdd5" width="600" height="400">  

**Etape 9** : Sur le bureau, dans la barre du menu, cliquez sur l'icône de la fenêtre Windows tout en bas à gauche et cliquez sur "Change account settings"  
<img src="https://github.com/user-attachments/assets/08b306d7-fa23-48f7-938d-5dd4b0316d0b" width="600" height="400">  

**Etape 10** : Séléctionnez "Wilder", puis entrez votre mot de passe (par défaut : Azerty1*)  
<img src="https://github.com/user-attachments/assets/5eb8bf66-0090-4113-8d0a-93fb477cc119" width="600" height="400">  

**Etape 11** : Sur le bureau, dans la barre de recherche, tapez "Ultra" et cliquez sur l'icône de l'application "UltraVNC Viewer"  
<img src="https://github.com/user-attachments/assets/ab7970b4-75c3-4c9c-9d7a-6d2c2f0cd262" width="600" height="400">

**Etape 12** : L'application s'ouvre  
<img src="https://github.com/user-attachments/assets/8b1edd64-5b35-4780-9fe0-899084da195a" width="600" height="400">

**Etape 13** : Entrez l'adresse IP du PC client (ici: 172.16.10.10)  
<img src="https://github.com/user-attachments/assets/d18a21fd-83f6-4d71-97e5-e87b67fe5b5e" width="600" height="400">  

**Etape 14** : Cliquez sur le bouton "OK"  
<img src="https://github.com/user-attachments/assets/43751ee2-8a64-428b-9d66-e0239cdc428e" width="600" height="400">

**Etape 15** : Cliquez sur le bouton "OK"  
<img src="https://github.com/user-attachments/assets/5eb8bf66-0090-4113-8d0a-93fb477cc119" width="600" height="400">

**Etape 16** : Cliquez sur le bouton "OK"  
<img src="https://github.com/user-attachments/assets/5eb8bf66-0090-4113-8d0a-93fb477cc119" width="600" height="400">


**Etape 17** : Cliquez sur le bouton "OK"!








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
