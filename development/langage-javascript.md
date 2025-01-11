# Langage Javascript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les `structures` de base du langage ✔️
  - Tpes primitifs :
      - String (chaines de caractères)
          ex : let nom = "Bechir";
      - Number (entiers ou décimaux)
          ex : let age = 32;
      - Boolean (true ou false)
          ex : let estAdulte = true;
      - Undefined (variable déclarée mais non initialisée)
          ex : let variable;
      - Null (valeur vide explicitement définie)
          ex : let vide = null;

  - Types non primitifs :
      - Objets (conteneurs de paires clé-valeur)
          ex : let personne = { nom: "Behcir", age: 32 };
      - Arrays (listes indexées)
          ex : let fruits = ["pomme", "banane", "orange"];
      - Fonctions (bloc de code réutilisables)
          ex : function myFucntion() {
                  console.log("Hello World !);
                }
      - Classes (modèles pour créer des objets)
          ex : class Animal {
                  constructor(nom) {
                    this.nom = nom;
                  }
                }

    - Structures de contrôle :
        - if...else
            ex : if (age > 18) {
                  console.log("Adulte");
                } else {
                    console.log("Mineur");
                }

        - switch
            ex : switch (jour) {
                    case 1:
                      console.log("Lundi");
                      break;
                    default:
                      console.log("Jour inconnu");
                  }

    - Boucles :
        - for
            ex : for (let i = 0; i < 5; i++) {
                    console.log(i);
                  }

        - while
            ex : let i = 0;
                while (i < 5) {
                  console.log(i);
                  i++;
                }

        - do...while
            ex : let i = 0;
                 do {
                  console.log(i);
                  i++;
                } while (i < 5);


    - Structures de données avancées :
       - Maps (objets clé-valeur abec des clés de tout type)
           ex : const array1 = [1, 4, 9, 16];
                const map1 = array1.map((x) => x * 2);
                console.log(map1);

      - Filter (pour filtrer un tableau selon une condition déterminée)
          ex : const words = ['spray', 'elite', 'exuberant', 'destruction', 'present'];
               const result = words.filter((word) => word.length > 6);

      - forEach (exécuter une fonction donnée sur chaque élément du tableau)
          ex : const array1 = ['a', 'b', 'c'];
               array1.forEach((element) => console.log(element));

      - etc...


  - Les modules (permettent de structurer le code en fichiers séparés)
      - Exportation
          ex : export const nom = "Bechir";
      - Importation
          ex : import { nom } from './module.js';

  - Gestion des erreurs :
      - try...catch
          ex : try {
                let x = y + 1; 
              } catch (err) {
                  console.log("Erreur attrapée :", err.message);
              }

  - Asynchronicité :
      - Callbacks
          ex : setTimeout(() => console.log("Bonjour après 1 seconde"), 1000);

      - Promises
          ex : fetch('url').then(response => response.json()).catch(err => console.error(err));

      - async/await
          ex : async function fetchData() {
                try {
                  let data = await fetch('url');
                  console.log(await data.json());
                } catch (err) {
                  console.error(err);
                }
            }


- les normes `ecmascript` ✔️
    - Strict Mode : Écriture de code plus sûre.
    - Méthodes utiles pour les objets et tableaux : Array.forEach().
    - JSON intégré : JSON.parse(), JSON.stringify().
    - Variables modernes : let, const.
    - Fonctions fléchées : ()=> {}.
    - Classes : Syntaxe orientée objet.
    - Modules : import/export.
    - Promises pour gérer l'asynchronicité.
    - Méthode Array.prototype.includes().


- l'utilisation de l'`asynchrone` ✔️
    - Requêtes réseau (HTTP/Fetch API) :
        ex :
            async function fetchData() {
              const response = await fetch('https://api.example.com/data');
              const data = await response.json();
              console.log(data);
            }
            fetchData();

    - Interaction avec des bases de données :
        ex. avec mongoose :
            import mongoose from "mongoose";

            const connectDB = async () => {
              try {
                mongoose.connect(http://localhost:3000/mydb);
                console.log("Connected to database");
              } catch(error) {
                  console.log(error);
                }
            }

    - Timers et délais :
        ex. avec setTimeOut ou setInterval :
          setTimeout(() => {
            console.log('Cette tâche est exécutée après 2 secondes.');
          }, 2000);

    
    - Gestion d'événements (Event Listeners) :
          ex :
            document.getElementById('myButton').addEventListener('click', async () => {
              await new Promise(resolve => setTimeout(resolve, 1000));
              console.log('Bouton cliqué après 1 seconde.');
            });


      
- les spécifités du mot-clef `this` ✔️
    - Contexte d'une méthode d'objet :
        ex :
          const obj = {
            name: 'Alice',
            greet() {
              console.log(`Hello, ${this.name}!`);
            }
          };
          obj.greet();

    - Contexte dans un constructeur :
        ex :
          function Person(name) {
            this.name = name;
          }
          const person = new Person('Bob');
          console.log(person.name);

## 💻 Je code en Javascript

### Un exemple de code commenté ❌ / ✔️

```javascript
(e) => mc2;
```

### Utilisation dans un projet ❌ / ✔️

[lien github](...)

Description :

### J'ai utilisé ce langage en production ❌ / ✔️

[lien du projet](...)

Description :

### J'ai utilisé ce langage en environement professionnel ❌ / ✔️

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

