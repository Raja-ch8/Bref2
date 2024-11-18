# **Contexte du projet**

Maintenant que vous êtes bien installé à votre poste de travail et familiarisé avec les ressources à votre disposition, vous allez traiter un premier ticket entrant.
_— Ticket 42 — Bonjour,
Dans le cadre du projet “LifeSense”, nous avons besoin d’échanger des gros fichiers (plusieurs GO). Nous souhaitons le faire sans passer par un drive tierce, de façon simple par un navigateur web, avec des accès sécurisés par utilisateur. Pour répondre à ce ticket, vous allez déployer une infrastructure de 3 serveurs et le logiciel Nextcloud :
1 VM d’administration linux (qui servira aux rebonds pour l’administration) 1 VM applicative linux (pour l’application Nextcloud) 1 VM BDD linux (base de données nécessaire à Nextcloud)_

# *Modalités pédagogiques*

Les déploiements sont à faire manuellement en utilisant le portail web Azure et en exécutant des commandes via SSH sur les VM.
​
En groupe de 3 personnes, vous allez :

- Préparer minutieusement votre plan d’action comprenant :
1. un plan réseau,
2. la liste des ressources Azure que vous prévoyez de déployer,
3. la liste des tâches que vous avez identifiées.
4. Restitution collective en groupe
5. Déployer les 3 VM interconnectées par un réseau local (10.0.<numéro de groupe>.0/24)
6. Déployer et configurer la base de données
7. Déployer et configurer Nextcloud
8. Créer des utilisateurs et tester l’infrastructure
​
## *BONUS*
Créer un workspace Azure Sentinel et y envoyer les logs de tous les serveurs
Créer une ressource Application Insights liée au workspace Sentinel et ajouter un test de disponibilité pour monitorer l’application
BONUS pour les plus motivés
Mettre en place TLS avec un certificat Let’s Encrypt sur le port tcp/443
Modalités d'évaluation


## **Critères de performance**

- Pouvoir accéder à Nextcloud par Internet en HTTP (par le port tcp/8080) chacun nominativement et pouvoir s’échanger des fichiers
- Pouvoir accéder à l’application en utilisant un FQDN
- Pouvoir administrer les 2 serveurs en SSH depuis la VM de rebond (accessible par Internet en SSH par le port tcp/10022)
- Ne pas pouvoir accéder en SSH aux VM applicative et BDD directement depuis internet

*BONUS*
- Les logs des 3 serveurs se retrouvent dans Azure Sentinel
- Le test de disponibilité est fonctionnel et bien configuré avec Application Insights

*BONUS* pour les plus motivés
- L’application est accessible de manière sécurisée via TLS. Le certificat est reconnu comme sûr par le navigateur.
