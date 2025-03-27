## Sommaire

1. [Utilisation de base de UltraVNC](#utilisation-de-base)
2. [Utilisation avancée de UltraVNC](#utilisation-avancee)
3. [Utilisation de Bureau à Distance](#utilisation-de-Bureau-à-distance)
4. [FAQ](#faq)

# 1. Utilisation de base de Ultravnc - ADMINISTRATEUR
------------------
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

------------------
## A. Utilisations et options disponibles lors d'une intervention distante

### **Interaction avec les fichiers**:
------------------
  - Via UltraVNC vous avez la possibilité une fois connecté, d'avoir un accès complet au dossier et fichier de votre machine **"hôte"** et de la machine **"Remote"** via "**l'interface File Transfer**" :

![transfer_file_serveur_client](https://github.com/user-attachments/assets/57afd03d-a007-410f-9012-0b20de65f0e8)

![acceuil_transfer_file](https://github.com/user-attachments/assets/3c4239a4-62c9-4264-baf8-0f3db4d1ecac)

------------------
  - Une fois sur l'interface vous avez plusieurs possibilité qui s'offrent à vous selon vos besoins:
  - Vous pouvez transférez des fichiers et dossier déja existant vers l'une ou l'autre machine :
    
  ---> Une fois le fichier et/ou dossier séléctionner cliquer sur "**SEND**" pour l'envoyer sur la machine **Remote** ou "**RECEIVE**" pour la recevoir sur votre machine **Hôte**

  _(EX: Ici nous envoyons le dossier "**New_Folder_Test**" de la machine **Hôte** vers la machine **Remote**(en l'occurence le client). Vous pouvez apercevoir le chemin des dossiers/fichiers sur les deux machines dans la  barre de titre situé en haut._

  **Important**: Pour transférer un dossier d'une machine à l'autre il ne doit pas être vide ou le transfert ne s'effectuera pas. Cela ne s'applique pas aux fichiers.
  ![envoie_file_vers_client](https://github.com/user-attachments/assets/730c613e-8f77-43bd-904b-5ce1d44a6036)

  ![envoie_file_vers_client](https://github.com/user-attachments/assets/ee0057ae-fa17-41d7-949a-231c4b044972)

  **(EX: Récupération du fichier _Client_Folder_ sur la machine 'Hôte'**)
  ![client_folder_recuperation_finished](https://github.com/user-attachments/assets/1f5fc9e0-afbd-4544-8a88-ada0834e4030)
  
------------------
  - Vous pouvez aussi renommer et supprimer un fichier/dossier sur les deux machines **Hôte** et **Remote** via cette interface :

  ---> Pour supprimer un fichier/dossier, cliquez sur le bouton **Delete** après l'avoir séléctionner

  ![delete_file_client](https://github.com/user-attachments/assets/6a45bbcb-35c9-4129-8aca-0ac9444097a0)

  ---> Pour renommer un fichier/dossier cliquez sur **RENAME** après l'avoir séléctionner

  ![rename_folder2](https://github.com/user-attachments/assets/d2843bda-5379-4fc0-b871-4b8a6504cf2b)

  ---> Pour avoir un aperçu des différentes branches de dossiers disponible sur chaque machine, vous pouvez vous déplacez à l'aide du menu déroulant (flèche rouge) situé à coté de "**LOCAL MACHINE**" et **REMOTE MACHINE** ou 
  via la barre de titre pour le chemin complet (flèche verte).
  
  ![chemin_de_destination](https://github.com/user-attachments/assets/99de2db3-3218-4de3-a550-6d79b8d7a82f)
  
------------------

  - Lors d'une prise de contrôle, vous serez peut être amenez à utiliser des commandes ou vous déplacez dans des dossiers qui, par sécurité ne peuvent être connu que de vous "**l'administrateur**". Et donc par conséquent          UltraVNC a pensez à vous en mettant une fonction vous permettant de cacher l'écran de la machine **REMOTE** empéchant ainsi au client dépanné de voir l'intervention sensible en cours.  

![connexion_client2](https://github.com/user-attachments/assets/4abf98af-3e11-489b-b4b2-4d3d1dc8aa12)

  (Lorsqu'il est activé l'écran s'affiche noir avec un cadenas montrant qu'il est actif)
  ![ecran_client_cacher](https://github.com/user-attachments/assets/9385332d-b7f6-4714-8444-663cb6dc2ab1)


  (Point de vue de la machine **REMOTE** une fois l'écran de sécurité activé)
  ![ecran_client_cacher2](https://github.com/user-attachments/assets/9489c8c4-f30d-4049-bf3b-a804fe291279)

------------------
  - Vous pouvez regardez l'historique des actions effectuer dans la barre déroulante situé en bas à coté de **"History"**
![history_file_transfer](https://github.com/user-attachments/assets/430a82f7-8722-450e-959c-039e9ce93378)

------------------
  - Lors d'une intervention si vous n'avez aucun contact avec la personne nécéssitant l'assistance, il existe un tchat intégré a **UltraVNC**:

  --> Pour lancer le tchat, appuyer sur les deux bulles vertes. Une fenêtre apparaîtra sur votre machine **Hôte** et sur la machine **REMOTE**
![connexion_client_3](https://github.com/user-attachments/assets/e348d5a5-20bf-4f12-9d09-6c729b40810b)

![tchat_serveur_client](https://github.com/user-attachments/assets/55a860e4-78ca-4bef-a912-a4a1c503e396)

(Fenêtre de tchat apparaissant sur la machine **REMOTE**)
![tchat_client_serveur](https://github.com/user-attachments/assets/7e80ac97-e024-43a7-ba33-e7f29f11095c)

------------------
  - Pour éviter d'avoir des conflits avec votre machine, le raccourci CTRL+ALT+SUPPR peut être lancer via les trois petites touches dans la barre d'outils à gauche :
![ctrl_alt_suppr_option](https://github.com/user-attachments/assets/844dd1cf-9df4-43c7-826c-e8829b34e695)

![send_ctrl_alt_supp_client](https://github.com/user-attachments/assets/d23b4277-0829-46c4-8eba-f8c15536d828)

  - Il est possible également de faire un screenshot via **UltraVNC**
  
  ---> Cliquez sur l'appareil photo situé dans la barre d'outil pour effectuer une capture d'image
  ![screenshot_option](https://github.com/user-attachments/assets/0957f843-25c3-4bd7-9fd2-5ca33daea74a)
  
  - Evidemment une fois la connexion établie vous pouvez très bien vous servir de la machine **REMOTE** comme si c'était votre machine et effectuer diverses actions...

  **(EX: Prendre le control du Powershell pour vous aidez dans votre intervention)**
  ![prise_de_contrôle_powershell_](https://github.com/user-attachments/assets/aa6b3fac-6a1d-4acd-828a-1dbf843c70f5)

  
# 3. Utilisation de Bureau à Distance
<span id="utilisation-de-Bureau-à-distance"></span>
## **Etape 1**:
----------------
- Cherchez l'application **_Bureau à distance_** dans la rechercher windows:

![Lancement_Bur_à_Dist](https://github.com/user-attachments/assets/73414fa6-ee71-4d1b-95e8-5885277a14ab)

- Une fenêtre apparaîtra pour vous connecter, renseigner l'IP de la machine sur laquel vous voulez intervenir puis appuyez sur **Connexion**

![connexion_hôte_client](https://github.com/user-attachments/assets/2c8690bd-7933-42df-8381-48ea26c1746c)

- Choissisez la session à ouvrir sur la machine **REMOTE** puis cliquez sur **_OK_**, en l'occurence lors d'une intervention il est préférable d'utiliser la session Administrateur pour une intervention optimisé du client. Vous devez donc au préalable savoir si le compte dispose d'un mot de passe ou non.
![authentification_session_à_ouvrir](https://github.com/user-attachments/assets/f47ace68-2073-4ce4-a7ff-378a8b29c985)


--> **NOTE:** Contrairement à UltraVNC, la connexion via le Bureau à Distance fonctionne en utilisant une session, ce qui implique la déconnexion de cette dernière si elle est ouverte sur la machine qui subit l'intervention. Le client n'a donc pas d'accès à ce que vous êtes en train de faire

------------------
- Une fois la connexion établie et la session ouverte, vous avez un accès total sur la machine et sur ces fonctionnalitées en disposant des autorisations Administrateur.

(EX:Prise de contrôle)    
![prise_de_contrôle_standard](https://github.com/user-attachments/assets/6a0c454d-a23d-4655-bf32-e22946b28437)

(EX:Prise de contrôle de **PowerShell** et du **ServerManager**)
![controle_server_et_powershell](https://github.com/user-attachments/assets/8fb16d5a-cc9e-45d4-9d88-4b1c6d4721fb)

# 4. FAQ
<span id="faq"></span>

1. **J'essaie de tranférer un dossier avec UltraVNC mais j'ai un message d'erreur**
--> Le transfert d'un dossier ne peut avoir lieu que s'il contient au moins un fichier. Les dossiers vides ne peuvent être transférés.

