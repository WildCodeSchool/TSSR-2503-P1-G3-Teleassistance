## Sommaire

1. [Prérequis technique](#prerequis-technique)
2. [Installation sur le serveur](#installation-sur-le-serveur)  
* a. [Renommer le pc](#renommer_le_pc)  
* b. [Configuration réseau](#configuration_reseau_serveur)  
* c. [Installation Ultra VNC](#installation_ultra_vnc_server)  
* d. [Désactivation du pare-feu](#desactivation_du_pare_feu_serveur)  
* e. [Droits d'accès](#droits_acces_serveur)  
3. [Installation sur le client](#installation-sur-le-client)  
* a. [Réseau VirtualBox](#virtualbox_reseau)  
* b. [Configuration réseau](#configuration_reseau_client)  
   * 1 . [Adressage réseau](#adressage_reseau)  
   * 2 .[Liaison nom et adresse IP](#liaison_nom_adresse_ip)  
* c. [Installation Ultra VNC](#installation_ultra_vnc_client)  
* d. [Désactivation du pare-feu](#desactivation_du_pare_feu_client)  
* e. [Droits d'accès](#droits_acces_client)  
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
<img src="https://github.com/user-attachments/assets/8ded1ca3-acea-4a44-b20b-ac1f42932cd5" width="600" height="400">

**Etape 2** : Sélectionnez le mode Expert  
<img src="https://github.com/user-attachments/assets/cd75eb0a-3537-47cb-8d20-7415a63df585" width="600" height="400">  

**Etape 3** : Cliquez sur "Réseau"  
<img src="https://github.com/user-attachments/assets/2e0f3cbe-41a1-46ca-b7a2-d489064621e8" width="600" height="400">  

**Etape 4** : Cliquez sur "Adapter 2", puis dans "Mode d'accès réseau" séléctionnez "Réseau interne", enfin cliquez sur le bouton "OK"  
<img src="https://github.com/user-attachments/assets/a4bb8fe3-ce1e-46e8-9809-8404b61c3ec4" width="600" height="400">  

**Etape 5** : Vous pouvez lancer votre machine virtuelle  
<img src="https://github.com/user-attachments/assets/74e3a4b0-04e5-4a38-a4ce-51dddfd09649" width="600" height="400">  



   **b. Configuration Réseau** 
<span id="virtualbox_reseau"></span>

        1. Adressage réseau
<span id="adressage_reseau"></span> 
**Etape 1** : En bas à droite, cliquez qur l'icône de l'ordinateur, une petite fenêtre apparaît  
<img src="https://github.com/user-attachments/assets/31de87e1-97de-4766-b92f-c3df42ee137a" width="600" height="400">

**Etape 2** : Cliquez sur "Paramètres du réseau ete internet"  
<img src="https://github.com/user-attachments/assets/37807f5c-02b0-4089-be3f-19eed16c5a06" width="600" height="400">

**Etape 3** : Une nouvelle fenêtre "Etat, statu du réseau" s'ouvre  
<img src="https://github.com/user-attachments/assets/0a3374c1-231f-4ed0-938c-14971adb6582" width="600" height="400">

**Etape 4** : Descendez jusqu'aux "Paramètres réseau avancés", puis cliquez sur "Modifier les options d'adaptateur"  
<img src="https://github.com/user-attachments/assets/f833bdc5-c6a6-4a48-b0e4-dc4723772a5a" width="600" height="400">

**Etape 5** : Une nouvelle fenêtre "connexion réseau" s'affiche  
<img src="https://github.com/user-attachments/assets/cda09895-ea8c-46fd-81ae-74d72f60f2d8" width="600" height="400">

**Etape 6** : Faites un clic droit sur "Ethernet 2", puis cliquez sur "Propriétés"  
<img src="https://github.com/user-attachments/assets/10e13df6-4128-4c3a-affb-b62a4e9e752d" width="600" height="400">

**Etape 7** : Vérifier que la case "Internet Protocol Version 4 (TCP/IPv4) soit coché, sinon cochez-là, puis cliquez sur "Propriétés"  
<img src="https://github.com/user-attachments/assets/19f49358-c22c-4a1d-8c41-079e1cbd51ce" width="600" height="400">

**Etape 8** : Une nouvelle fenêtre s'ouvre, séléctionnez "Utiliser l'adresse IP suivante" et notez pour "Adresse IP": 172.16.10.10, puis dans Masque de sous-réseau : 255.255.255.0 , puis cliquez sur "OK" pour valider :   
<img src="https://github.com/user-attachments/assets/d6b55b86-41e4-4a38-bc54-680035ecd750" width="600" height="400">


       2. Liaison nom et adresse IP
<span id="liaison_nom_adresse_ip"></span> 

**Etape 1** : Ouvrez votre explorateur de fichier, puis dans le menu à gauche, cliquez sur "Ce PC"   
<img src="https://github.com/user-attachments/assets/11a86726-dc7d-41ac-9066-c17a6b4aa840" width="600" height="400">

**Etape 2** : Double cliquez sur votre Disque local (C:)  
<img src="https://github.com/user-attachments/assets/92ff2f4d-5442-49f8-b6e0-05b9ab3ccece" width="600" height="400">

**Etape 3** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/010fb725-00f5-4ee8-80fb-b69a52611525" width="600" height="400">

**Etape 4** : Allez dans le dossier "System32"  
<img src="https://github.com/user-attachments/assets/a44ff4c5-95c4-4d05-95c8-61e64587c09f" width="600" height="400">

**Etape 5** : Allez dans le dossier "drivers"  
<img src="https://github.com/user-attachments/assets/47d5cff4-1482-4a51-83e9-2f4f2c08e559" width="600" height="400">

**Etape 6** : Allez dans le dossier "etc"  
<img src="https://github.com/user-attachments/assets/1eb6a204-d189-42b1-8f32-ac9bc7a6caa6" width="600" height="400">

**Etape 7** : Dans la liste des fichiers, trouvez le fichier "hosts"  
<img src="https://github.com/user-attachments/assets/36166d97-8497-4ead-8977-519ad49dbd05" width="600" height="400">

**Etape 8** : Faites un clic droit sur le fichier "hosts"  
<img src="https://github.com/user-attachments/assets/22d8fc0d-bb2f-41ba-a937-838cef9ce250" width="600" height="400">

**Etape 9** : Ouvrez le fichier avec un bloc note  
<img src="https://github.com/user-attachments/assets/35ea58b0-da93-4dd8-ae0f-4dd8703c90df" width="600" height="400">

**Etape 10** : Tout en bas du fichier, notez l'adresse IP de la machine server (dans l'exemple : 172.16.10.5), appuyer la touche TAB (tabulation) et notez le nom de la machine (dans l'exemple : SRVWIN01)  
<img src="https://github.com/user-attachments/assets/c88904ca-763b-4c33-8404-96cb35643399" width="600" height="400">



   **c. Installation Ultra VNC** 
<span id="installation_ultra_vnc_client"></span>

**Etape 1** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/92428263-8020-4456-97b4-b35902d15d8d" width="600" height="400">

**Etape 2** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/14d67231-38cf-4057-8e71-6e69f0b46207" width="600" height="400">

**Etape 3** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/6c52db49-cac3-4d9f-a982-400d9b9d272f" width="600" height="400">

**Etape 4** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/8a727397-2f57-4c0f-8aba-10d0e32400eb" width="600" height="400">

**Etape 5** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/0a1bf817-0272-4333-8cc3-6b0e2ffbc102" width="600" height="400">

**Etape 6** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/e42457f6-0555-41b7-8c1a-f593ce08b6c6" width="600" height="400">

**Etape 7** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/73638b1d-df07-49a1-8e54-8c71217a44cf" width="600" height="400">

**Etape 8** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/971ef5dd-efb2-4c62-8a4b-7155a24c8b7b" width="600" height="400">

**Etape 9** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/b2fa051b-edce-4906-b2c8-9ae1e95745df" width="600" height="400">

**Etape 10** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/a1cc74ab-c1e6-4005-a0e2-ba3780a280b7" width="600" height="400">

**Etape 11** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/491d78a5-802b-4b91-8226-2959b7fcccec" width="600" height="400">

**Etape 12** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/2e69adb2-2753-42ad-a18f-81eb7a909a79" width="600" height="400">

**Etape 13** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/5765ecb4-dc74-4268-abf4-05da6e7c4b95" width="600" height="400">

**Etape 14** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/7fb10a22-8dfa-4335-92a8-74467cfb1458" width="600" height="400">

**Etape 15** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/63ff6a42-0634-4b4d-9993-f24f18ee5cf7" width="600" height="400">

**Etape 16** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/54eba6ea-4357-45fd-8ccd-fd40f3e0d9d1" width="600" height="400">

**Etape 17** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/c7ae6434-4a9b-47a9-bcf9-f9e5613b09b1" width="600" height="400">

**Etape 18** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/6d4ade7d-1be6-4832-9a98-6bc9d86c9165" width="600" height="400">

**Etape 19** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/c5e460e2-9c99-4fa1-81dc-6ee0fb983420" width="600" height="400">

**Etape 20** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/2ee889b0-0ba5-4819-9875-3bf22d7744dc" width="600" height="400">



   **d. Désactivation du pare-feu** 
<span id="desactivation_du_pare_feu_client"></span>

**Etape 1** : Sur le bureau, dans la barre de recherche, tapez "Pare-feu" et cliquez sur l'icône de l'application "Pare-feu Windows Defender"  
<img src="https://github.com/user-attachments/assets/92d88ea8-8b37-4152-b91e-75462f15713a" width="600" height="400">

**Etape 2** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/af1b806f-2f8b-4252-bf59-8331b15f755b" width="600" height="400">

**Etape 3** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/c2e47211-a009-4e2c-9482-8b6e33740a05" width="600" height="400">

**Etape 4** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/8049a188-8c78-4682-984c-a8b3529b9d34" width="600" height="400">

**Etape 5** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/77ae2d9a-afc7-457e-8d31-114696f9587c" width="600" height="400">

**Etape 6** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/6bf4180a-ba26-49af-8d5f-f37a96d209cd" width="600" height="400">

**Etape 7** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/65a239f5-d51c-4706-9671-9e46259da5aa" width="600" height="400">

**Etape 8** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/3e594bf2-2f61-4004-82c4-781024b2d81f" width="600" height="400">

**Etape 9** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/e55c1673-d035-4302-ba65-62ee400f2513" width="600" height="400">

**Etape 10** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/5b9b26bb-c209-4fc4-8c16-174daaf011b8" width="600" height="400">

**Etape 11** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/ea00a0dd-e063-450a-bb01-9bfdb2975234" width="600" height="400">




   **e. Droits d' accès** 
<span id="droits_acces_client"></span>

**Etape 1** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/304f61f0-22f3-49cd-9b73-6a40e02ca616" width="600" height="400">

**Etape 2** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/6084995f-ab35-47fe-bc9d-c3827c823937" width="600" height="400">

**Etape 3** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/33a84c9a-bd5f-4884-83fd-a7bc7fb64dce" width="600" height="400">

**Etape 4** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/c0740af9-9836-4d5a-898b-23bfbe283b4e" width="600" height="400">

**Etape 5** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/365ee328-95c3-44eb-a83f-e4c3c585f038" width="600" height="400">

**Etape 6** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/97a1891a-5fcd-4ac7-9bbd-36430669acac" width="600" height="400">

**Etape 7** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/82b1c5b8-2463-4261-b58b-2f17ae380d6a" width="600" height="400">

**Etape 8** : Allez dans le dossier "Windows"  
<img src="https://github.com/user-attachments/assets/e2d50807-e8d3-4389-ae04-bbfce106f9d5" width="600" height="400">




# 4. FAQ
<span id="faq"></span>  

**Est-ce qu'un utilisateur standard peut se servir de la téléassistance ?**  
Non, seul les administrateurs peuvent se servier de l'assistance, que ce soit avec le bureau à distance ou UltraVNC.  

**J'essaie de tranférer un dossier avec UltraVNC mais j'ai un message d'erreur**  
Le transfert d'un dossier ne peut pas avoir lieu que s'il contient au moins un fichier. Les dossiers vides ne peuvent être transférés.  

**Est-il normal que UltraVNC Server soit sur le PC Client et UltraVNC Viewer soit sur le PC Server ?**  
Oui, c'est tout à fait normal, VNC Server sert à établir le lien avec le PC qui fera l'assistance. Ultra VNC viewer sert à prendre le contrôle du PC à dépanner.  

**Lors du paramétrage de UltraVNC, dans VNC authentification, j'ai un message d'erreur lorsque je rentre mon mot de passe et que je le confirme en l'entrant à novueau**  
Le VNC Password et le View-Only Password doivent être 2 mots de passe différent.  
Le VNC Password sert à prend le contrôle du PC à assister et à exécuter des tâches de dépannage, quand au View-Only Password il sert uniquement à voir le PC a assister sans pouvoir faire de dépannage.  


