# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE ✔️
    L’intérêt de TypeScript dans un IDE (comme VS Code) est d’améliorer la productivité des développeurs grâce à un meilleur typage, une auto-complétion avancée, et une détection précoce des erreurs.
    Principaux avantages :

    ## Auto-complétion intelligente
    - Permet à l’IDE de mieux comprendre la structure du code, offrant une auto-complétion plus précise.
      Exemple de définition d'une interface :
  
          interface User {
            id: number;
            name: string;
            email?: string;
          }

          const user: User = { id: 1, name: "Alice" };

    L’IDE proposera automatiquement `id`, `name` et `email` comme propriétés disponibles.


    ## Détection des erreurs en temps réel
    - Contrairement à JavaScript, TypeScript permet d'identifier les erreurs avant l'exécution.
      Exemple :

          let age: number = "25"; // ❌ Erreur détectée avant l'exécution
      L’IDE surligne l’erreur et propose des corrections.

    ## Refactoring sécurisé
    -  Lorsqu'on modifie une variable, une fonction ou un type, TypeScript ajuste automatiquement tout le code concerné, réduisant le risque de bugs.
 

    ## Documentation instantanée
    - Grâce aux types et interfaces, l’IDE peut afficher la structure des objets et des fonctions sans devoir consulter une doc externe.
 
       
- les types de bases ✔️
    Les types de base permettent de définir des valeurs avec des types spécifiques pour éviter les erreurs.
    Les principaux :

    ## Types primitifs
    `string`: chaîne de caractères

      let message: string = "Hello, TypeScript!";

    `number`: Nombres (entiers et flottants)

      let age: number = 25;
      let price: number = 99.99;

    `boolean`: Valeurs `true` ou `false`

      let isActive: boolean = true;

    `null` et `undefined`: Valeurs spéciales pour indiquer l’absence de données

      let emptyValue: null = null;
      let notDefined: undefined = undefined;

    ## Types complexes
    `any`:  Désactive le typage (⚠️ à éviter autant que possible)

      let anything: any = "Hello";
      anything = 42; // Aucun avertissement

    `unknown`: Type sécurisé pour les valeurs inconnues (nécessite un contrôle de type)

      let notSure: unknown = "Hello";
      if (typeof notSure === "string") {
        console.log(notSure.toUpperCase());
      }

    `array`: Tableau de valeurs d’un type donné

      let numbers: number[] = [1, 2, 3, 4, 5];
      let names: Array<string> = ["Alice", "Bob"];

    `tuple`: Tableau avec un nombre défini d’éléments et des types précis

      let person: [string, number] = ["Alice", 30];


    `object`:  Objet avec des propriétés

      let user: { name: string; age: number } = { name: "Bob", age: 25 };


    ## Types avancés
    `union` (`|`):  Une variable peut avoir plusieurs types possibles

      let id: string | number = "123";
      id = 123; // OK


    `literal`:  Valeurs spécifiques

      let status: "success" | "error" | "loading";
      status = "success"; // OK


    `enum`:  Liste de valeurs nommées

      enum Direction {
        Up = "UP",
        Down = "DOWN",
        Left = "LEFT",
        Right = "RIGHT"
      }
      let move: Direction = Direction.Up;


    `void`: Indique qu'une fonction ne retourne rien

      function logMessage(): void {
        console.log("Hello!");
      }


- comment et pourquoi étendre une interface ✔️
  L’extension d’une interface permet de réutiliser et enrichir une interface existante sans la modifier. Cela favorise :
    - Réutilisabilité → Évite de dupliquer du code.
    - Flexibilité → Permet d’ajouter des propriétés spécifiques à un type sans casser la structure de base.
    - Lisibilité → Organise le code en hiérarchisant les interfaces.
 
  ### Comment étendre une interface ?
    On utilise le mot-clé `extends` pour créer une nouvelle interface basée sur une autre.

    - Héritage d’une interface
 
          interface Person {
            name: string;
            age: number;
          }
          
          interface Employee extends Person {
            jobTitle: string;
          }
          
          const employee: Employee = {
            name: "Alice",
            age: 30,
            jobTitle: "Developer"
          };

    - Étendre plusieurs interfaces (héritage multiple)

          interface Address {
            street: string;
            city: string;
          }
          
          interface Contact {
            email: string;
            phone: string;
          }
          
          interface Employee extends Person, Address, Contact {
            jobTitle: string;
          }
          
          const employee: Employee = {
            name: "Bob",
            age: 35,
            street: "123 Main St",
            city: "Paris",
            email: "bob@example.com",
            phone: "123456789",
            jobTitle: "Designer"
          };

      - Étendre une interface générique

            interface ApiResponse<T> {
              data: T;
              status: number;
            }
            
            interface User {
              id: number;
              name: string;
            }
            
            interface UserResponse extends ApiResponse<User> {}
            
            const response: UserResponse = {
              data: { id: 1, name: "Alice" },
              status: 200
            };


- les classes et les decorators ❌ / ✔️

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
