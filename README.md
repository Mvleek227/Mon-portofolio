Portfolio – Abdoul Maliki 

### Projet 1 : Application de ticketing interne

Technologies : Python/Django, PostgreSQL, Linux  
Objectif : Faciliter le suivi et la gestion des incidents IT.  
Rôle : Développement complet, interface web, base de données, notifications email.

---

### Capture 1: Page de login
![Page de login](Images/Page_login.jpg)  

Description : Pour la sécurité du service il est nécessaire d'avoir des identifiants pour pouvoir y accéder. Cette page s'occupe également des redirections intelligente, ainsi en fonction des rôles elle redirige les utilisateurs vers la page de formulaire. Les techniciens vers celle des techniciens et les administrateurs vers celle des administrateurs.

### Capture 2 : Création d’un ticket
![Création d'un ticket](Images/Formulaire_ticket.jpg)  

Description : L’utilisateur peut créer un ticket avec un titre, une catégorie et notamment pour parler du niveau de priorité et les besoins. Le formulaire est simple, responsive et intuitif pour permettre une saisie rapide des incidents. 

---

### Capture 3 : Dashboard administrateur
![Dashboard administrateur](Images/Dashboard_admin.jpg)  

Description : Vue d’ensemble pour les administrateurs, avec suivi des tickets en temps réel. Les tickets sont triés par statut (ouvert, en cours, résolu) pour faciliter le traitement. Ils ont notamment la possibilité d'assigner un ticket à un technicien spécifique tout comme à un groupe de techniciens. Ils peuvent également trier les tickets et exporter un fichier pour les statistiques d’incidents mensuelles ou annuelles.

---

### Capture 4 : Dashboard technicien 
![Dashboard technicien](Images/Dashboard_technicien.jpg)  

Description : Les techniciens reçoivent uniquement le ticket qui leur est affecté. Ils n'ont pas la possibilité de voir les tickets assigner à un autre technicien sauf si le ticket a été assigné au groupe de techniciens auquel il fait parti.

---

### Capture 5 : Détails du tickets
![Détails du ticket ](Images/Détails_tickets.jpg)  

Description :Chaque ticket créé ou mis à jour déclenche l’envoi automatique d’un email aux parties concernées, pour assurer un suivi efficace. Sur sa page les tickets apparaîtront sous forme de liste et le technicien peut ainsi consulter les tickets en cliquant dessus pour avoir plus de détails.

---

 Bénéfices du projet
- Suivi centralisé des incidents IT  
- Notifications automatiques pour ne rien oublier  
- Interface web simple et intuitive  
- Démonstration des compétences en développement Django, administration de base de données et sécurité minimale des accès.

---

Note : Les captures d’écran sont fournies à titre illustratif. Le code source complet pour une démo est disponible sur demande.



### Projet 2 : Mise en place d'un contrôleur de domaine avec Samba 4

**Technologies :** Samba 4, Linux, Windows clients, WinRM, Ansible  

**Objectif :** Fournir une infrastructure Active Directory interne pour gérer utilisateurs, groupes, et appliquer des stratégies de sécurité aux postes Windows tout en automatisant la gestion.  

**Rôle :**
- Configuration du serveur Samba 4 en tant que contrôleur de domaine  
- Création et gestion des utilisateurs et groupes  
- Déploiement de stratégies de groupe (GPO) via les outils Windows (RSAT / GPMC)  
- Automatisation de la configuration et déploiement de logiciels sur les postes Windows avec WinRM et Ansible.

## Architecture Samba 4 (Active Directory)

```mermaid
graph TD
    A[Utilisateur Windows] -->|Authentification AD| B[Samba 4 DC]
    C[Utilisateur Linux] -->|Authentification LDAP/Kerberos| B
    B -->|Application des GPO| A
    B -->|Gestion DNS/DHCP| D[Services Réseau]
```

**Détails techniques:**
- Le serveur Samba 4 agit comme contrôleur de domaine, gérant authentification et permissions des utilisateurs Windows et Linux.  
- Les GPO sont déployées via les outils Windows pour appliquer les politiques de sécurité et configurations logicielles sur les postes clients.  
- L’accès distant et l’automatisation sont assurés par WinRM et Ansible, pour une meilleure maîtrise de la gestion à grande échelle et sécurisée des postes.  
- Le schéma illustre le flux centralisé de gestion et sécurité, avec la possibilité d’automatisation complète pour l’administrateur.  

**Bénéfices :**
- Gestion centralisée et sécurisée des utilisateurs et postes  
- Déploiement automatisé et maintenance simplifiée  
- Nouvelles aptitudes en administration AD, Linux, et automatisation  

---

### Projet 3 : Gestion des serveurs de messagerie avec Postfix

**Technologies :** Postfix, Dovecot, Roundcube, Linux  

**Objectif :** Fournir un service de messagerie interne sécurisé pour les utilisateurs.  

**Rôle :**
- Installation et configuration de Postfix pour l’envoi et la réception des emails  
- Configuration de Dovecot pour la récupération sécurisée des emails  
- Mise en place de Roundcube pour l’accès webmail  
- Gestion des utilisateurs et des droits d’accès  

## Architecture Postfix / Dovecot / Roundcube

Ce schéma illustre le flux complet de mon système de messagerie interne basé sur Postfix, Dovecot et Roundcube :

```mermaid
sequenceDiagram
    participant U as Utilisateur (Navigateur Web)
    participant R as Roundcube (Webmail)
    participant P as Postfix (MTA)
    participant D as Dovecot (IMAP/POP3)
    participant I as Internet

    U->>R: Connexion via navigateur
    R->>P: Envoi Email (SMTP)
    P->>I: Transfert vers Internet
    I->>P: Réception Email
    P->>D: Stockage Mail
    R->>D: Récupération Mail (IMAP)

```

Le schéma illustre le fonctionnement de notre système de messagerie interne. L’utilisateur accède au webmail Roundcube via un navigateur. Roundcube communique avec :

•Postfix (MTA) pour l’envoi et la réception des emails,

•Dovecot (IMAP/POP3) pour le stockage et la récupération des messages.

Cette architecture permet à tout utilisateur d’envoyer et de recevoir des emails de manière sécurisée, et le système reste compatible avec d'autres clients mail standard (Thunderbird, etc) si nécessaire.

**Bénéfices :**
- Messagerie interne fonctionnelle et sécurisée  
- Gestion simple des comptes utilisateurs  
- Nouvelles aptitudes en administration de serveurs Linux et services email


### Projet 4 : Système de Rappels Automatisés – Python (Desktop Application)

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey)
![Status](https://img.shields.io/badge/Status-Production-green)

---

## 📌 Présentation

Ce projet est une application desktop développée en Python permettant d’automatiser les rappels d’échéances réglementaires (fiscales et sociales) pour un service de comptabilité.

L'objectif est de réduire les oublis critiques et d'améliorer la gestion des obligations administratives dans un environnement professionnel.

---

## 🛠️ Stack technique

- **Langage :** Python  
- **UI :** Tkinter  
- **Gestion images :** Pillow  
- **Données :** JSON  
- **Packaging :** PyInstaller  
- **Automatisation :** Windows Task Scheduler  

## 🎯 Problématique

Dans de nombreuses organisations, les échéances fiscales et sociales reposent sur des rappels manuels ou la mémoire des employés, ce qui entraîne :

- ❌ Risque élevé d’oubli  
- ❌ Retards de déclaration  
- ❌ Pénalités financières  
- ❌ Mauvaise organisation interne  

---

## 💡 Solution proposée

Une application légère et automatisée qui :

- surveille les échéances
- génère des rappels intelligents
- affiche des notifications visuelles obligatoires
- s'intègre au démarrage du système

---

## 🚀 Fonctionnalités principales

### 🔔 Système de rappel intelligent
- Notifications automatiques en popup
- Rappels multi-niveaux :  
  - J-7
  - J-5  
  - J-3  
  - J-2  
  - J-1  
  - Jour J  

---

### 🎨 Interface utilisateur avancée
- Interface graphique moderne avec Tkinter
- Design professionnel inspiré des outils internes d’entreprise
- Logo intégré
- Affichage en cartes (cards UI)

---

### 🟧🔵 Gestion multi-catégories
- Fiscal → Couleur Orange  
- Social → Couleur Bleue  
- Identification rapide des types d’échéances

---

### 📊 Indicateurs visuels
- Compteur global des rappels actifs
- Mise en avant des priorités
- Hiérarchisation visuelle des informations

---

### 🔒 Interaction contrôlée
- Popup non fermable (obligation de validation)
- Bouton "J’ai pris connaissance"
- Traçabilité des actions utilisateur

---

### 📝 Journalisation
- Génération automatique de logs
- Historique des rappels affichés
- Suivi des validations utilisateur

---

### ⚙️ Automatisation système
- Lancement automatique via Windows
- Intégration avec le planificateur de tâches
- Fonctionnement sans intervention utilisateur

---

### 📦 Déploiement
- Compilation en exécutable (.exe)
- Distribution sur postes utilisateurs
- Installation simplifiée

---

## 📸 Aperçu de l'application

<img width="3870" height="3240" alt="1000882094" src="https://github.com/user-attachments/assets/d41e7e62-3ef3-4554-bf18-e71d002eaa96" />




























