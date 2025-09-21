# Application de Gestion Locative

Une application complète pour gérer vos propriétés de location saisonnière.

## Fonctionnalités

- 📊 Tableau de bord avec statistiques
- 📅 Calendrier des tarifs et disponibilités
- 🏠 Gestion des propriétés
- 👥 Gestion des clients
- 📋 Gestion des réservations
- 💰 Suivi des paiements
- 📄 Génération de contrats et factures PDF
- 📧 Envoi d'emails automatisés
- 📈 Rapports de taxe de séjour

## Configuration

### Variables d'environnement

Créez un fichier `.env` avec les variables suivantes :

```
VITE_SUPABASE_URL=votre-url-supabase
VITE_SUPABASE_ANON_KEY=votre-cle-anonyme-supabase
```

### Maintien de Supabase actif

Ce projet utilise GitHub Actions pour maintenir la base de données Supabase active et éviter qu'elle se mette en pause après 7 jours d'inactivité.

#### Configuration des secrets GitHub

Pour que le système fonctionne, vous devez configurer les secrets suivants dans votre repository GitHub :

1. Allez dans **Settings** > **Secrets and variables** > **Actions**
2. Ajoutez les secrets suivants :
   - `SUPABASE_URL` : Votre URL Supabase (ex: https://xxxxx.supabase.co)
   - `SUPABASE_ANON_KEY` : Votre clé anonyme Supabase

#### Comment ça fonctionne

- Le workflow s'exécute automatiquement tous les jours à 8h00 UTC
- Il fait une requête simple vers votre base de données Supabase
- Cela maintient la base active et évite la mise en pause automatique
- Vous pouvez aussi déclencher le workflow manuellement depuis l'onglet "Actions" de GitHub

## Installation

1. Clonez le repository
2. Installez les dépendances : `npm install`
3. Configurez les variables d'environnement
4. Lancez l'application : `npm run dev`

## Déploiement

L'application peut être déployée sur Netlify ou tout autre service d'hébergement statique.

## Technologies utilisées

- React + TypeScript
- Tailwind CSS
- Supabase (base de données et authentification)
- React PDF (génération de documents)
- React Router (navigation)
- Date-fns (gestion des dates)
- Recharts (graphiques)