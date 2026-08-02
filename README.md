# Mallette

Mallette est une application de stockage de fichiers **auto-hébergée**. Elle permet de garder la maîtrise de ses données tout en retrouvant facilement ses photos, ses vidéos et ses documents depuis une interface web ou mobile.

## Fonctionnalités

- Importer des photos, des vidéos et des documents ;
- consulter et prévisualiser les fichiers compatibles ;
- télécharger ses fichiers ;
- organiser ses données dans un espace personnel ;
- déposer et consulter des fichiers dans des espaces partagés.

L'espace personnel est réservé à son propriétaire. Les espaces partagés permettent à plusieurs utilisateurs d'accéder à des fichiers communs.

## Architecture du projet

Le dépôt est organisé sous la forme d'un monorepo :

- `apps/backend` : API construite avec AdonisJS ;
- `apps/web` : application web Nuxt ;
- `apps/mobile` : application mobile Vue et Capacitor.

Les tâches du monorepo sont orchestrées avec Turborepo et les dépendances sont gérées avec pnpm.

## Développement

### Prérequis

- Node.js 24 ou une version ultérieure ;
- pnpm 10.33.2.

### Installation

```sh
pnpm install
```

### Lancer les applications en développement

```sh
pnpm dev
```

### Commandes utiles

```sh
pnpm build      # Compiler toutes les applications
pnpm test       # Exécuter les tests
pnpm lint       # Vérifier la qualité du code
pnpm typecheck  # Vérifier les types TypeScript
pnpm format     # Formater le code
```
