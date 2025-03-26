## Sommaire

1. [Utilisation de base de UltraVNC](#utilisation-de-base)
2. [Utilisation avancée de UltraVNC](#utilisation-avancee)
3. [FAQ](#faq)

# 1. Utilisation de base de Ultravnc - ADMINISTRATEUR
<span id="utilisation-de-base"></span>
## A. Intervention sur une machine distante :


### **Etape 1**:
-------------------
- Lancer le logiciel **UltraVNC Viewer**, vous devriez arrivez sur la fenêtre de connexion principal. Une fois dessus, renseigner l'adresse du réseau de votre intervention.

_(EX: Ici on choisis l'ip de notre machine client connecté en local)_

![connect_ultra](https://github.com/user-attachments/assets/5746aac8-5349-44ed-b6e7-58905d163f1b)


### **Etape 2:**
-------------------
- Une fois l'adresse ip renseigner, vous devrez rentrez le mot de passe(**VNC Password**) que vous auriez pré-configuré dans **UltraVNC SERVER** pour lancer l'accès à distance. 

**NOTE: Ne rentrez pas le mot de passe que vous avez configuré dans le **VIEW-Only Password**, vous aurez un accès seulement visuel sur la session et aucun pouvoir d'action.**

![authentification_ultra](https://github.com/user-attachments/assets/7f6da396-208e-4bdf-ba51-ed6b8f16f5c6)

### **Etape 3:**
------------------
- Vous êtes maintenant connecté ! La fenêtre de contrôle de la machine distante apparaîtra sur votre interface comme si vous etiez devant l'écran et ainsi pouvez faire toute les interactions possibles ...

![connexion_client](https://github.com/user-attachments/assets/e6500229-dd3e-4d34-ab6b-669905256375)

# 2. Utilisation avancée
<span id="utilisation-avancee"></span>
## A. Utilisations et options disponibles lors d'une intervention distante

### **Interaction avec les fichiers**:
- Via UltraVNC vous avez la possibilité une fois connecté, d'avoir un accès complet au dossier et fichier de votre machine **"hôte"** et de la machine **"Remote"** via "**l'interface File Transfer**" :


![transfer_file_serveur_client](https://github.com/user-attachments/assets/57afd03d-a007-410f-9012-0b20de65f0e8)

![acceuil_transfer_file](https://github.com/user-attachments/assets/3c4239a4-62c9-4264-baf8-0f3db4d1ecac)

- Une fois sur l'interface vous avez plusieurs possibilité qui s'offrent à vous selon vos besoins:
  - Vous pouvez transférez des fichiers et dossier déja existant vers l'une ou l'autre machine :
    
  ---> Une fois le fichier et/ou dossier séléctionner cliquer sur "**SEND**" pour l'envoyer sur la machine **Remote** ou "**RECEIVE**" pour la recevoir sur votre machine **Hôte**

_(EX: Ici nous envoyons le dossier "**New_Folder_Test**" de la machine **Hôte** vers la machine **Remote**(en l'occurence le client). Vous pouvez apercevoir le chemin des dossiers/fichiers sur les deux machines dans la barre situé en haut._

**Important**: Pour transférer un dossier d'une machine à l'autre il ne doit pas être vide ou le transfert ne s'effectuera pas. Cela ne s'applique pas aux fichiers.

![envoie_file_vers_client](https://github.com/user-attachments/assets/730c613e-8f77-43bd-904b-5ce1d44a6036)

![envoie_file_vers_client](https://github.com/user-attachments/assets/ee0057ae-fa17-41d7-949a-231c4b044972)
  - Vous pouvez aussi renommer et supprimer un fichier/dossier sur les deux machines **Hôte** et **Remote** via cette interface :

  ---> Pour ce faire, après avoir séléctionner un dossier cliquez sur le bouton **Delete**

  ---> Pour renommer un fichier/dossier cliquez sur **RENAME** après l'avoir séléctionner

![envoie_file_vers_client_finished2](https://github.com/user-attachments/assets/6a45bbcb-35c9-4129-8aca-0ac9444097a0)





  
# 3. FAQ
<span id="faq"></span>
