# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- Comment développer en utilisant un système de *livereloading* (`nodemon` par exemple) ✔️
- La connexion de mon application à une base de données avec et sans ORM/ODM (avec `mongodb` puis `mongoose` par exemple) ✔️
- Le développement d'une API REST et GraphQL (avec les packages `express` et `graphql` par exemple) ✔️
- *Bonus : la manipulation des fichiers système avec `fs` et l'utilisation des streams en NodeJS* ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```javascript
const dotenv = require('dotenv').config();

const connectDB = require("./config/db");
const express = require("express");
const router = require("./routes");
const cookieParser = require("cookie-parser");
const cors = require("cors");

const port = process.env.PORT;

// Connexion à la DB
connectDB();

const app = express();

// Middlewares
app.use(cors({
  origin: 'http://localhost:8081',
  credentials: true
}));
app.use(express.json());
app.use(cookieParser());

app.get("/", (req, res) => {
  res.status(200).send("L'API est connectée !");
});

app.use("/api", router);

app.get("*", (req, res) => {
  res.status(404).json({ message: "Not Found !" });
});

// Lancer le serveur
app.listen(port, (err) => {
  if (err) {
    console.log(err);
  } else {
    console.log("Le serveur a démarré au port " + port);
  }
});
```

### Utilisation dans un projet ✔️

[Projet4](https://github.com/mdonatelli1/Projet4/tree/dev)

Description : Mon quatrième projet durant mon BootCamp à la Wild, portant sur React Native.

### Utilisation en production si applicable ❌

[lien du projet](...)

Description : /

### Utilisation en environement professionnel ❌

Description : /

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description: /

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution : /

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌
- J'ai fait une [présentation](...) ❌
