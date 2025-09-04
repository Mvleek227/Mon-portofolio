Portfolio – Abdoul Maliki 

Projet 1 : Application de ticketing interne

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
