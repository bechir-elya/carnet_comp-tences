# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- Comment développer en utilisant un système de *livereloading* (`nodemon` par exemple) ✔️
    Nodemon est un outil très populaire dans l'écosystème Node.js. Il permet aux développeurs de redémarrer automatiquement leur application Node.js chaque fois qu'un fichier est modifié dans le projet.
  
- La connexion de mon application à une base de données avec et sans ORM/ODM (avec `mongodb` puis `mongoose` par exemple) ✔️
  ex : Configuration base de données avec mongoose et mongoDB :
      
      import mongoose from "mongoose";
      import dotenv from "dotenv";

      dotenv.config();

      export const connectDB = async () => {
        try {
          await mongoose.connect(process.env.DB_URI);
          console.log('Connected');
        } catch (error) {
            console.log(error);
        }
      }

    Création d'un modèle avec Mongoose :

      import mongoose from "mongoose";

      export const userSchema = mongoose.Schema({
        username: String,
        email: String,
        password: String,
        image: String,
        resetToken: String,
        task: {type: mongoose.Schema.Types.ObjectId, ref: 'Task'}
      });

      const User = mongoose.model('User', userSchema);
      export default User;
  
- Le développement d'une API REST et GraphQL (avec les packages `express` et `graphql` par exemple) ✔️
  exemple d'une API REST avec `express`:

      export const addTask = async (req, res) => {

        const data = await Task.create({
        title: req.body.title,
        content: req.body.content,
        deadline: req.body.deadline,
        priority: req.body.priority,
        userId: req.body.userId
        })
        res.json(data);
      }

  exemple d'une API GraphQL avec `graphql` :

      @Mutation(() => Clothes)
      @Authorized("ADMIN")
      async createClothes(@Arg("data") data: ClothesInput) {
        let clothe = new Clothes();
        clothe = Object.assign(clothe, data);
        const sizes = await Size.findBy({ id: In(data.sizes) })
        if (sizes.length === 0) {
            throw new Error("Invalid sizes provided");
        }
        clothe.sizes = sizes;
        await clothe.save()
        return clothe;
      }
  
- *Bonus : la manipulation des fichiers système avec `fs` et l'utilisation des streams en NodeJS* ❌

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️

```javascript
// this function takes a path to a .md file of the host system and write the HTML version of this file
// the .html file is given back
const convertMDFileToHTML = (pathToMDfile) => /* ... path to HTML file */
```

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
