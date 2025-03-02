# GraphQL

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la différence entre REST et GraphQL ✔️

      1. Structure et Fonctionnement
          REST : Basé sur des ressources accessibles via des URL spécifiques et utilisant des méthodes HTTP standard (GET, POST, PUT, DELETE).
          GraphQL : Fournit une seule URL d'accès où les clients peuvent demander précisément les données souhaitées via des requêtes structurées.
      
      2. Flexibilité des Requêtes
          REST : Retourne généralement des réponses prédéfinies, ce qui peut entraîner un sur-chargement (trop de données) ou un sous-chargement (données manquantes nécessitant plusieurs requêtes).
          GraphQL : Permet aux clients de spécifier exactement les champs qu'ils veulent récupérer, réduisant ainsi la surcharge ou le sous-chargement.
      
      3. Gestion des Endpoints
          REST : Utilise plusieurs endpoints (/users, /users/{id}, /posts, etc.).
          GraphQL : Un seul endpoint (/graphql) qui sert toutes les requêtes.
      
      4. Performance et Efficacité
          REST : Peut nécessiter plusieurs appels pour récupérer des données liées (ex : récupérer un utilisateur, puis ses articles).
          GraphQL : Permet d'obtenir toutes les données nécessaires en une seule requête.
      
      5. Gestion des Versions
          REST : Nécessite souvent de versionner l’API (/v1/users, /v2/users).
          GraphQL : Évite le versionnement en permettant aux clients de demander uniquement les champs pertinents.
      
      6. Typage et Documentation
          REST : Peut nécessiter une documentation externe (ex : Swagger).
          GraphQL : Fournit un schéma fortement typé et auto-documenté.
      
      7. Quand utiliser REST ou GraphQL ?
          REST est souvent préférable pour des API simples, des services nécessitant du caching HTTP natif, ou des interactions standardisées.
          GraphQL est idéal pour les applications complexes avec de nombreuses relations entre les données, nécessitant de la flexibilité et une optimisation des requêtes.

- les besoins auxquels répond GraphQL ✔️
  
    ✅ Optimiser les requêtes (éviter le sur-chargement et le sous-chargement)
    ✅ Réduire le nombre d’appels API
    ✅ Simplifier l’évolution des API (pas besoin de versionner)
    ✅ Donner plus de contrôle aux clients (notamment les développeurs front-end)
    ✅ Fournir une API auto-documentée et typée

  
- la définition d'un schéma ✔️
    En GraphQL, un schéma est la structure qui définit la forme des données disponibles via l'API. Il décrit les types d’objets, leurs champs, leurs relations et les opérations possibles (queries, mutations).
    Exemple de schéma : 

      # Définition d'un type "User"
      type User {
        id: ID!
        name: String!
        email: String!
        posts: [Post]
      }
      
      # Définition d'un type "Post"
      type Post {
        id: ID!
        title: String!
        content: String!
        author: User!
      }
      
      # Définition des opérations possibles
      type Query {
        getUser(id: ID!): User
        getAllUsers: [User]
        getPost(id: ID!): Post
      }
      
      type Mutation {
        createUser(name: String!, email: String!): User
        createPost(title: String!, content: String!, authorId: ID!): Post
      }


- Query ✔️
    Ensemble de requêtes pour récupérer des données.
  
- Mutation ✔️
    Ensemble de requêtes qui permet d'ajouter/modifier des données.
  
- Subscription ✔️
    Permet d’écouter des mises à jour en temps réel.

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️

### Utilisation dans un projet ❌ / ✔️

[lien github](...)

Description :

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
