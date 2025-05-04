---
title: "Projets Lycée"
date: 2025-05-03T22:41:10+05:30
draft: false
github_link: "https://github.com/gurusabarish/hugo-profile"
author: "Kaze"
tags:
  - Projets
  - GSB
  - SDIS29
image: /images/post.jpg
description: ""
toc: 
---

> Blog sur mes projets au lycée Le Castel pendant mon BTS SIO !

# Projet GSB : Mission "Compte-rendu"

##🎯 **Objectif** :  
> Mettre en œuvre, pour chaque groupe d'AP, une **infrastructure virtuelle complète** composée de quatre serveurs hébergés sur **Proxmox** :

- 🗄️ **Serveur MariaDB** : héberge toutes les bases de données du projet  
- 🛠️ **Serveur Gitea** : plateforme de gestion des dépôts Git  
- 🌐 **Serveur Apache/PHP** :  
  - héberge l’application web en production  
  - fournit l’accès à **phpMyAdmin** pour administrer les bases  
  - contient un **Wiki** pour la documentation technique  
- 💾 **Serveur de sauvegarde** : sauvegarde automatique des bases deux fois par jour

### Résultat :
- Environnement de développement et de production stable  
- Données sécurisées et facilement récupérables  
- Documentation intégrée et accessible

# Projet SDIS29 : Mission 

##🎯 **Objectif** :  
> Créer un **environnement complet de production, de test et de supervision** sur Proxmox à l’aide de **VM KVM**.

### Tâches réalisées :
- Déploiement d’un **serveur de production (ap3x-prod)** :  
  - Tomcat 10 pour héberger l’application web  
  - Base de données **MariaDB** pour le stockage des données
- Mise en place d’un **serveur de test (ap3x-test)** identique à la prod, pour les essais et validations
- Installation d’un **serveur de supervision (ap3x-mon)** pour surveiller l’état des autres machines (ressources, services)

### Résultat :
- Environnement isolé et modulaire pour tester et déployer sereinement  
- Capacité de **surveillance** en temps réel de l’activité des serveurs  
- Bonne pratique Dev/Prod respectée
