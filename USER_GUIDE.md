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
- Lancer le logiciel **UltraVNC Viewer**, vous devriez arriver sur la fenêtre de connexion principal. Une fois dessus, renseigner l'adresse du réseau de votre intervention.

_(EX: Ici on choisi l'ip de notre machine client connecté en local)_

![connect_ultra](https://github.com/user-attachments/assets/5746aac8-5349-44ed-b6e7-58905d163f1b)


### **Etape 2:**
-------------------
- Une fois l'adresse ip renseignée, vous devrez rentrer le mot de passe(**VNC Password**) que vous auriez pré-configuré dans **UltraVNC SERVER** pour lancer l'accès à distance. 

**NOTE: Ne rentrez pas le mot de passe que vous avez configuré dans le **VIEW-Only Password**, vous aurez un accès seulement visuel sur la session et aucun pouvoir d'action.**

![authentification_ultra](https://github.com/user-attachments/assets/7f6da396-208e-4bdf-ba51-ed6b8f16f5c6)

### **Etape 3:**
------------------
- Vous êtes maintenant connecté ! La fenêtre de contrôle de la machine distante apparaîtra sur votre interface comme si vous étiez devant l'écran et ainsi pouvez faire toutes les intéractions possibles ...

![connexion_client](https://github.com/user-attachments/assets/e6500229-dd3e-4d34-ab6b-669905256375)

# 2. Utilisation avancée
<span id="utilisation-avancee"></span>

------------------
## A. Utilisations et options disponibles lors d'une intervention distante

### **Interaction avec les fichiers**:
------------------
  - Via UltraVNC vous avez la possibilité une fois connecté, d'avoir un accès complet aux dossiers et fichiers de votre machine **"hôte"** et de la machine **"Remote"** via "**l'interface File Transfer**" :

![transfer_file_serveur_client](https://github.com/user-attachments/assets/57afd03d-a007-410f-9012-0b20de65f0e8)

![acceuil_transfer_file](https://github.com/user-attachments/assets/3c4239a4-62c9-4264-baf8-0f3db4d1ecac)

------------------
  - Une fois sur l'interface vous avez plusieurs possibilités qui s'offrent à vous selon vos besoins:
  - Vous pouvez transférer des fichiers et dossiers déjà existants vers l'une ou l'autre machine :
    
  ---> Une fois le fichier et/ou dossier séléctionné, cliquer sur "**SEND**" pour l'envoyer sur la machine **Remote** ou "**RECEIVE**" pour la recevoir sur votre machine **Hôte**

  _(EX: Ici nous envoyons le dossier "**New_Folder_Test**" de la machine **Hôte** vers la machine **Remote**(en l'occurence le client). Vous pouvez apercevoir le chemin des dossiers/fichiers sur les deux machines dans la  barre de titre située en haut._

  **Important**: Pour transférer un dossier d'une machine à l'autre il ne doit pas être vide sinon le transfert ne s'effectuera pas. Cela ne s'applique pas aux fichiers.
  ![envoie_file_vers_client](https://github.com/user-attachments/assets/730c613e-8f77-43bd-904b-5ce1d44a6036)

  ![envoie_file_vers_client](https://github.com/user-attachments/assets/ee0057ae-fa17-41d7-949a-231c4b044972)

  **(EX: Récupération du fichier _Client_Folder_ sur la machine 'Hôte'**)
  ![client_folder_recuperation_finished](https://github.com/user-attachments/assets/1f5fc9e0-afbd-4544-8a88-ada0834e4030)
  
------------------
  - Vous pouvez aussi renommer et supprimer un fichier/dossier sur les deux machines **Hôte** et **Remote** via cette interface :

  ---> Pour supprimer un fichier/dossier, cliquez sur le bouton **Delete** après l'avoir sélectionner

  ![delete_file_client](https://github.com/user-attachments/assets/6a45bbcb-35c9-4129-8aca-0ac9444097a0)

  ---> Pour renommer un fichier/dossier cliquez sur **RENAME** après l'avoir sélectionner

  ![rename_folder2](https://github.com/user-attachments/assets/d2843bda-5379-4fc0-b871-4b8a6504cf2b)

  ---> Pour avoir un aperçu des différentes branches de dossiers disponibles sur chaque machine, vous pouvez vous déplacer à l'aide du menu déroulant (flèche rouge) situé à coté de "**LOCAL MACHINE**" et **REMOTE MACHINE** ou 
  via la barre de titre pour le chemin complet (flèche verte).
  
  ![chemin_de_destination](https://github.com/user-attachments/assets/99de2db3-3218-4de3-a550-6d79b8d7a82f)
  
------------------

  - Lors d'une prise de contrôle, vous serez peut-être amené à utiliser des commandes ou vous déplacez dans des dossiers qui, par sécurité,  ne peuvent être connus que de vous "**l'administrateur**". Et donc par conséquent UltraVNC a pensé à vous en mettant une fonction vous permettant de cacher l'écran de la machine **REMOTE** empéchant ainsi au client dépanné de voir l'intervention sensible en cours.  

![connexion_client2](https://github.com/user-attachments/assets/4abf98af-3e11-489b-b4b2-4d3d1dc8aa12)

  (Lorsqu'il est activé, l'écran s'affiche noir avec un cadenas montrant qu'il est actif)
  ![ecran_client_cacher](https://github.com/user-attachments/assets/9385332d-b7f6-4714-8444-663cb6dc2ab1)


  (Point de vue de la machine **REMOTE** une fois l'écran de sécurité activé)
  ![ecran_client_cacher2](https://github.com/user-attachments/assets/9489c8c4-f30d-4049-bf3b-a804fe291279)

------------------
  - Vous pouvez regarder l'historique des actions effectuées dans la barre déroulante située en bas à coté de **"History"**
![history_file_transfer](https://github.com/user-attachments/assets/430a82f7-8722-450e-959c-039e9ce93378)

------------------
  - Lors d'une intervention si vous n'avez aucun contacte avec la personne nécéssitant l'assistance, il existe un tchat intégré à **UltraVNC**:

  --> Pour lancer le tchat, appuyer sur les deux bulles vertes. Une fenêtre apparaîtra sur votre machine **Hôte** et sur la machine **REMOTE**
![connexion_client_3](https://github.com/user-attachments/assets/e348d5a5-20bf-4f12-9d09-6c729b40810b)

![tchat_serveur_client](https://github.com/user-attachments/assets/55a860e4-78ca-4bef-a912-a4a1c503e396)

(Fenêtre de tchat apparaissant sur la machine **REMOTE**)
![tchat_client_serveur](https://github.com/user-attachments/assets/7e80ac97-e024-43a7-ba33-e7f29f11095c)

------------------
  - Pour éviter d'avoir des conflits avec votre machine, le raccourci CTRL+ALT+SUPPR peut être lancé via les trois petites touches dans la barre d'outils à gauche:  
![ctrl_alt_suppr_option](https://github.com/user-attachments/assets/844dd1cf-9df4-43c7-826c-e8829b34e695)

![send_ctrl_alt_supp_client](https://github.com/user-attachments/assets/d23b4277-0829-46c4-8eba-f8c15536d828)

  - Il est possible également de faire un screenshot via **UltraVNC**
  
  ---> Cliquez sur l'appareil photo situé dans la barre d'outil pour effectuer une capture d'image
  ![screenshot_option](https://github.com/user-attachments/assets/0957f843-25c3-4bd7-9fd2-5ca33daea74a)
  
  - Evidemment une fois la connexion établie vous pouvez très bien vous servir de la machine **REMOTE** comme si c'était votre machine et effectuer diverses actions...

  **(EX: Prendre le contrôle du Powershell pour vous aider dans votre intervention)**
  ![prise_de_contrôle_powershell_](https://github.com/user-attachments/assets/aa6b3fac-6a1d-4acd-828a-1dbf843c70f5)

  
# 3. Utilisation de Bureau à Distance
<span id="utilisation-de-Bureau-à-distance"></span>
## **Etape 1**:
----------------
- Cherchez l'application **_Bureau à distance_** dans la recherche windows:

![Lancement_Bur_à_Dist](https://github.com/user-attachments/assets/73414fa6-ee71-4d1b-95e8-5885277a14ab)

- Une fenêtre apparaîtra pour vous connecter, renseignez l'IP de la machine sur laquelle vous voulez intervenir puis appuyez sur **Connexion**

![connexion_hôte_client](https://github.com/user-attachments/assets/2c8690bd-7933-42df-8381-48ea26c1746c)

- Choissisez la session à ouvrir sur la machine **REMOTE** puis cliquez sur **_OK_**, en l'occurence lors d'une intervention il est préférable d'utiliser la session Administrateur pour une intervention optimisé du client. Vous devez donc au préalable savoir si le compte dispose d'un mot de passe ou non.
![authentification_session_à_ouvrir](https://github.com/user-attachments/assets/f47ace68-2073-4ce4-a7ff-378a8b29c985)


--> **NOTE:** Contrairement à UltraVNC, la connexion via le Bureau à Distance fonctionne en utilisant une session, ce qui implique la déconnexion de cette dernière si elle est ouverte sur la machine qui subit l'intervention. Le client n'a donc pas d'accès à ce que vous êtes en train de faire.

------------------
- Une fois la connexion établie et la session ouverte, vous avez un accès total sur la machine et sur ses fonctionnalitées en disposant des autorisations Administrateur.

(EX:Prise de contrôle)    
![prise_de_contrôle_standard](https://github.com/user-attachments/assets/6a0c454d-a23d-4655-bf32-e22946b28437)

(EX:Prise de contrôle de **PowerShell** et du **ServerManager**)
![controle_server_et_powershell](https://github.com/user-attachments/assets/8fb16d5a-cc9e-45d4-9d88-4b1c6d4721fb)
------------------
- Le presse-papier est pris en charge lors de la connexion. Vous pouvez donc transferez des fichiers/dossier ou même du texte via cette fonctionnalité. Nous allons copier un dossier sur la machine **REMOTE** et le coller sur notre machine **Hôte** :


(**EX: Pour transférez un fichier/dossiers faites un clique droit(ou CTRL+C) et séléctionner copier(Copy)**
![Copie_fichier](https://github.com/user-attachments/assets/3ebe62d0-e753-40a4-b958-c68c3df19d9d)

(**Puis faites un clic droit vers l'endroit ou vous voulez copier le fichier/dossier puis séléctionner coller (ou CTRL+V)**

![Coller_fichier](https://github.com/user-attachments/assets/148b5080-aff0-41b5-b18b-fcad96d00b4f)

(**Dossier bien transférer entre les deux machines**)
![fichier_transferer](https://github.com/user-attachments/assets/508e6cc0-a632-46c8-bb77-20ee69578e48)

**Note : Le Bureau à distance permet le transfert de dossiers vide contrairement à UltraVNC**
-----------------

![65a65f61a5dc0fccb6a01af8_FAQSINEA](https://github.com/user-attachments/assets/f8b4fb51-678c-4d9c-b9c6-a955b5ee453f)
<span id="faq"></span>

1. **J'essaie de tranférer un dossier avec UltraVNC mais j'ai un message d'erreur**

--> Le transfert d'un dossier ne peut avoir lieu que s'il contient au moins un fichier. Les dossiers vides ne peuvent être transférés.

2. **Pourquoi ne puis-je pas me connecter à un PC distant via le Bureau à Distance ?**

--> Par défaut, seulement les comptes avec des droits Administrateur peuvent se connecter à distance. Si vous pouvez voir l’écran de connexion du PC distant, mais que vous ne pouvez pas vous connecter, vous n’êtes peut-être pas ajouté au groupe _Utilisateurs Bureau à distance_ ou à un groupe avec des droits d’administrateur sur le PC distant. Demandez à votre administrateur système de vous ajouter au groupe approprié.

3. **Est-il possible de se connecter à distance sur des systèmes d'exploitations différents ?**

--> Oui c'est possible. Seulement il peut être nécéssaire de télécharger des logiciels tiers pour permettre la télé-assistance ou un fonctionnement optimal.

