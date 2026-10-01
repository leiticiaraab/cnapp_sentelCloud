# Fonctionnement d'un scan

## Déroulement

1. Sélection du compte AWS
2. Initialisation de la session AWS
3. Vérification de l'identité et des permissions disponibles
4. Détection des régions ou périmètres à analyser
5. Collecte des ressources par service
6. Normalisation des données
7. Application des contrôles CSPM
8. Création des findings
9. Calcul du score et de la couverture
10. Enregistrement des résultats
11. Mise à jour du tableau de bord

## Principe important

Une absence d'alertes ne signifie pas automatiquement que l'environnement est sûr.

SentinelCloud distingue :

- aucun risque détecté
- aucune donnée disponible
- couverture incomplète
- scan en échec

Cette distinction évite de présenter un score rassurant lorsque l'analyse n'a pas réellement couvert l'environnement.

## Catégories de résultats

Les findings peuvent être regroupés selon :

- configuration
- identité et accès
- protection des données
- réseau
- journalisation
- vulnérabilités
- menaces

## Sévérités

- critique
- élevée
- moyenne
- faible
