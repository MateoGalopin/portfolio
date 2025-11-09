---
title: Infra web
publishDate: 2025-10-28 00:00:00
img: /portfolio/assets/crowdsec.png
img_alt: crowdsec
description:
  Mise en place des infrastructures et services Web sécurisés
tags:
  - Systèmes & réseaux
  - Gantt
---

Mise en place des infrastructures et services Web sécurisés pour une société avec deu sites, un public accessible à tous (extranet) et un privé pour le personnel (intranet).

Étape 1 : Installation du serveur linux

  Une machine virtuelle Linux fonctionnelle :
  - avec deux interfaces réseau correctement configurées ; 
  - sans environnement graphique.
  Deux pattes réseaux pour le serveur Linux :
  - une sur le 192.168.10.0/24 pour l’interne ;
  - une pour simuler l’externe en 150.10.0.0/16.

Étape 2 : Configuration du service web Apache

  Un serveur Apache fonctionnel avec deux virtual hosts sécurisés par SSL : 

  - accessibles sur des réseaux distincts, 

  - avec les droits d'accès appropriés.

Étape 3 : Configuration du service FTP

  Un serveur FTP sécurisé : 

  - accessible uniquement depuis le réseau privé, 

  - permettant un accès différencié aux ressources des sites web selon le profil de l'utilisateur (développeur ou graphiste).

  - ajout d'un certificat SSL

Étape 4 : Implémentation du filtrage réseau

  Un filtrage réseau qui n'autorise que 

  - HTTP/HTTPS sur l'interface extranet

  - SSH, FTP + HTTP/HTTPS (5501/5502) sur l'interface intranet.

Étape 5 : Renforcement de la protection contre les attaques

  Configuration des modules natifs d'Apache pour limiter les connexions abusives. 

  Installation de CrowdSec et configuration pour protéger l'extranet contre les attaques distribuées.
