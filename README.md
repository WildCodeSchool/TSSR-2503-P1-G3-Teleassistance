![Téléassistance](https://i.pinimg.com/736x/a3/10/ee/a310eec1336087c9735736621aba4c7d.jpg)

## Sommaire 

- [🎯 Présentation du projet](#presentation-du-projet)
- [📜 Introduction](#introduction)
- [👥 Membres du groupe par sprint](#membres-du-groupe-par-sprint)
- [⚙️ Choix Techniques](#choix-techniques)
- [🧗Difficultés rencontrées](#difficultes-rencontrees)
- [💡 Solutions trouvées](#solutions-trouvees)
- [🚀 Améliorations possibles](#ameliorations-possibles)
  
# 🎯 Présentation du projet
<span id="presentation-du-projet"></span>
# **La Téléassistance**

**Présentation**
> Le but du projet est de mettre en place une **_Télé-assistance_** entre un serveur et un client, via l'utilisation du logiciel **_UltraVNC_** et du **_Bureau à distance_** natif de Windows sur un réseau local entre les différentes machines

**Objectifs finaux**
- Etablissement d'une connexion Local entre 2 machines virtuelles, un _Serveur_ et un _Client_.
- Effectuer une assistance à distance
- Attribution de droits différents pour chaque logiciels et groupes d'utilisateurs pour le _Serveur_ et le _Client_


# 📜 Introduction
<span id="introduction"></span>

# 👥 Membres du groupe par sprint
<span id="membres-du-groupe-par-sprint"></span>
**Sprint 1**

| Membre   | Rôle       | Missions |
| -------- | ---------- | -------- |
| [Mamadou](https://github.com/DRAME1991) | PO         | -    Création Du Backlog - Organisation de la première présentation |
| [Florian](https://github.com/Juverios) | SM         | -    Mise en place de la Documentation et Organisations du Sprint 1 - Gestion des droits d'accès d'utilisateurs  |
| [Jonathan](https://github.com/TheHorusLab) | Technicien | -    Installation de **UltraVNC** _Serveur_ --> _Client_ - Paramétrage **UltraVNC** |


**Sprint 2**

| Membre   | Rôle       | Missions |
| -------- | ---------- | -------- |
| [Mamadou](https://github.com/DRAME1991)  | SM | -  Organisation du Sprint 2 - Mise en place de la présentation finale |
| [Florian](https://github.com/Juverios) | Technicien | - Documentation du USER_GUIDE.MD & README.MD  |
| [Jonathan](https://github.com/TheHorusLab) | PO         | - Documentation de INSTALL.MD  -  Vérification des attentes du client pour le Projets   |

# ⚙️ Choix techniques
<span id="choix-techniques"></span>
**Matériel**
**VM Client :**
  - Nom : **WIN01**
  - OS : **Windows 10 Pro**
  - Compte utilisateur : **Wilder**
  - Mot de passe : **Azerty1**
  - IP & Masque : **172.16.10.10 / 255.255.255.0**


**VM SERVEUR :**
  - Nom : **SRVWIN01**
  - OS : **Windows server 2022**
  - Compte utilisateur :  **Administrator** / **Wilder**
  - Mot de passe : **Azerty1**
  - IP & Masque : **172.16.10.5 / 255.255.255.0**

    
**Logiciel :**
- [**UltraVNC 1.4.3.6**](https://uvnc.com/downloads/ultravnc/159-ultravnc-1-4-3-6.html) 
- **Bureau à distance** Win10 Version 10.0.19041.5072 
- [**Oracle VirtualBox 7.1.6**](https://www.virtualbox.org/wiki/Downloads) / [**VirtualBox Extension pack**](https://www.virtualbox.org/wiki/Downloads)

# 🧗 Difficultés rencontrées
<span id="difficultes-rencontrees"></span>
- Logiciels inconnus [**UltraVNC 1.4.3.6**](https://uvnc.com/downloads/ultravnc/159-ultravnc-1-4-3-6.html)
- Problème de transfert de dossiers avec UltraVNC  
    

# 💡 Solutions trouvées
<span id="solutions-trouvees"></span>
- Instruction d'installation et d'utilisation du logiciel [**UltraVNC 1.4.3.6**](https://uvnc.com/downloads/ultravnc/159-ultravnc-1-4-3-6.html) via [Youtube](https://www.youtube.com/watch?v=QO-NhJYqR8I)
- Conditions de transfert d'un dossier via UltraVNC

  
# 🚀 Améliorations possibles
<span id="ameliorations-possibles"></span>
- Utilisation d'autres logiciels de télé-assistances possibles, [ici](https://www.appvizer.fr/services-informatiques/controle-distance) une liste d'autres logiciels utilisés (on y retrouve UltraVNC)  
- Communications possibles entre des OS différents ( Linux <--> Windows )
