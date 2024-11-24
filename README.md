# **Contexte du projet**

Dans le cadre du projet “LifeSense”, nous avons besoin d’échanger des gros fichiers (plusieurs GO). Nous souhaitons le faire sans passer par un drive tierce, de façon simple par un navigateur web, avec des accès sécurisés par utilisateur. Pour répondre à ce ticket, vous allez déployer une infrastructure de 3 serveurs et le logiciel Nextcloud :
1 VM d’administration linux (qui servira aux rebonds pour l’administration) 1 VM applicative linux (pour l’application Nextcloud) 1 VM BDD linux (base de données nécessaire à Nextcloud)

# **Modalités pédagogiques**

Les déploiements sont à faire manuellement en utilisant le portail web Azure et en exécutant des commandes via SSH sur les VM.
​
En groupe vous allez :
Préparer minutieusement votre plan d’action comprenant :
- un plan réseau,
- la liste des ressources Azure que vous prévoyez de déployer,
- la liste des tâches que vous avez identifiées.
- Déployer les 3 VM interconnectées par un réseau local (10.0.<numéro de groupe>.0/24)
- Déployer et configurer la base de données
- Déployer et configurer Nextcloud
- Créer des utilisateurs et tester l’infrastructure
​
BONUS

- Créer un workspace Azure Sentinel et y envoyer les logs de tous les serveurs

- Créer une ressource Application Insights liée au workspace Sentinel et ajouter un test de disponibilité pour monitorer l’application

- BONUS pour les plus motivés

- Mettre en place TLS avec un certificat Let’s Encrypt sur le port tcp/443
