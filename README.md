# Synchronisation des utilisateurs SM2 – BI

## Contexte

Ce projet répond à un besoin de synchronisation des comptes utilisateurs entre **SM2** et l’environnement **BI**.

L’objectif est d’éviter les mises à jour manuelles des comptes et de garantir que les accès BI restent cohérents avec les droits définis dans SM2.

> Le code source de ce projet est privé. Ce dépôt ne contient aucune donnée personnelle, configuration d’environnement ou information sensible.

## Données

Le programme utilise les informations utilisateurs disponibles dans SM2 pour contrôler les comptes présents dans l’environnement BI.

Les données traitées concernent les comptes utilisateurs et leurs droits d’accès. Elles ne sont pas incluses dans le dépôt.

## Démarche

Le programme automatise les étapes suivantes :

1. initialisation des logs et de l’audit ;
2. connexion aux systèmes SM2 et BI ;
3. récupération de la liste des utilisateurs depuis SM2 ;
4. comparaison avec les comptes existants dans BI ;
5. création ou mise à jour des comptes BI si nécessaire ;
6. désactivation des comptes ne répondant plus aux conditions d’accès ;
7. génération d’un suivi d’exécution et d’alertes si nécessaire.

## Résultats

L’outil permet de fiabiliser et d’automatiser la gestion des utilisateurs entre les deux systèmes.

Les principaux bénéfices sont :

- réduction des opérations manuelles ;
- cohérence accrue entre les comptes SM2 et BI ;
- gestion plus rapide des créations, mises à jour et désactivations ;
- traçabilité des traitements grâce aux logs et aux audits ;
- détection d’éventuelles alertes liées aux licences.

## Limites et pistes d’amélioration

Le fonctionnement dépend de la disponibilité et de la qualité des données utilisateurs dans les deux systèmes.

Des évolutions possibles seraient :

- ajouter un tableau de bord de suivi des synchronisations ;
- conserver un historique centralisé des modifications ;
- enrichir les alertes en cas d’anomalie ;

## Technologies utilisées

- Java
- SQL
- SAP BusinessObjects
- Logs et audit d’exécution
