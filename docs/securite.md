# Modèle de sécurité

## Lecture seule

SentinelCloud est conçu pour collecter des informations sans modifier les ressources AWS analysées.

L'objectif est d'utiliser uniquement les permissions nécessaires à l'inventaire et à l'évaluation de la posture de sécurité.

## Authentification

### Profil AWS CLI

Le poste local peut utiliser un profil déjà configuré dans `~/.aws`.

### Session AWS temporaire

Une session obtenue via `aws login` évite l'utilisation de clés longues durées.

### Cross-account

Pour un scénario multi-comptes, SentinelCloud peut utiliser un rôle IAM dédié avec `sts:AssumeRole`.

## Principe du moindre privilège

Exemples de familles de permissions utiles :

```text
ec2:Describe*
s3:List*
iam:List*
rds:Describe*
cloudtrail:DescribeTrails
config:Describe*
securityhub:Describe*
```

Le périmètre exact dépend des contrôles activés.

## Données sensibles

Le dépôt public ne contient pas :

- Access Key ID
- Secret Access Key
- tokens de session
- clés de dashboard
- fichiers `.env`
- ARN personnels
- identifiants de compte AWS réels

## Publication GitHub

Les captures publiées utilisent des données de démonstration ou des informations masquées.
