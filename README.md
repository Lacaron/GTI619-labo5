# GTI619-labo5
Ce modèle de projet a été créé dans le cadre du Laboratoire #5 du cours GTI619 Sécurité des Systèmes à l'École de technologie supérieure (ETS). Ce code vise à fournir aux étudiants une base pour développer une application avec des fonctionnalités d'authentification et de gestion de session.

## Partie 1 - RBAC
L'application doit intégrer une gestion d'accès basée sur les rôles (RBAC - Role-Based Access Control). Trois rôles doivent être implémentés :
- Administrateur
- Préposé aux clients résidentiels
- Préposé aux clients d'affaires

Trois utilisateurs doivent être créés :
- "Administrateur" avec le rôle "Administrateur"
- "Utilisateur1" avec le rôle "Préposé aux clients résidentiels"
- "Utilisateur2" avec le rôle "Préposé aux clients d'affaires".

L'application doit inclure plusieurs pages avec les fonctionnalités suivantes :
- Page d'authentification pour la connexion des utilisateurs.
- Page d'administration pour la configuration des options de sécurité, uniquement accessible aux administrateurs.
- Page affichant une liste de clients résidentiels, accessible aux préposés aux clients résidentiels et aux administrateurs.
- Page affichant une liste de clients d'affaires, accessible aux préposés aux clients d'affaires et aux administrateurs.

## Partie 2 - Authentification
L’implémentation de votre authentification devra répondre aux objectifs suivants :

1. **Objectif de contrôle** : Protocole de communication et d'échange d'information  
   **Description de la mise en œuvre** : Les informations d'authentification doivent être protégées.  
   **Paramètres** : Non paramétrable dans la plateforme admin.  

2. **Objectif de contrôle** : Gestion du mot de passe  
   **Description de la mise en œuvre** : Changement de mot de passe périodiquement ou suite à un événement (oubli, dépassement de la limite de tentatives).  
   **Paramètres** : Paramétrable dans la plateforme admin.  

3. **Objectif de contrôle** : Norme configurable pour les mots de passe  
   **Description de la mise en œuvre** : Complexité du mot de passe (longueur, classes de caractères, etc.). Impossibilité d'utiliser les anciens X mots de passe.  
   **Paramètres** : Paramétrable dans la plateforme admin.  

4. **Objectif de contrôle** : Stocker le mot de passe de façon sécuritaire  
   **Description de la mise en œuvre** : Un salt par utilisateur (visible lors de la démo). Complexité : plusieurs itérations de hachage, etc.  
   **Paramètres** : Non paramétrable dans la plateforme admin.  

5. **Objectif de contrôle** : Journalisation des connexions, des changements reliés à la sécurité  
   **Description de la mise en œuvre** : Connexions réussies et non réussies. Modification du mot de passe.  
   **Paramètres** : Non paramétrable dans la plateforme admin.  

6. **Objectif de contrôle** : Réauthentification pour certaines fonctions critiques  
   **Description de la mise en œuvre** : Redemander le mot de passe pour compléter les taches critiques (une fois connecté). Exemple : ajout d'un utilisateur.  
   **Paramètres** : Non paramétrable dans la plateforme admin.

## Partie 3 - Gestion de session
L’implémentation de votre gestion de session devra répondre aux objectifs suivants :

1. **Protection de l'identifiant de session** :
Les identifiants de session sont des clés uniques attribuées à chaque utilisateur.
Ils doivent être protégés contre toute tentative de régénération ou de réutilisation frauduleuse. 
Les identifiants de session ne doivent pas être accessibles via JavaScript.

2. **Stockage sécurisé des informations de session (côté serveur)** :
Toutes les informations liées à la session de chaque utilisateur doivent être stockées de manière sécurisée sur le serveur.

