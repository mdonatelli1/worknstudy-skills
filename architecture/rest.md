# REST API

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les verbes HTTP ✔️
- les statuts HTTP ✔️
- les endpoints ✔️
- CORS ✔️
- la nomenclature recommandée pour les routes ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```javascript
const express = require('express');
const app = express();
const port = 3000;

// Middleware pour parser le JSON
app.use(express.json());

// Exemple de données - simule une base de données
let users = [
    { id: 1, name: 'John Doe' },
    { id: 2, name: 'Jane Smith' },
];

// Route GET pour récupérer tous les utilisateurs
app.get('/users', (req, res) => {
    res.json(users);
});

// Route GET pour récupérer un utilisateur par ID
app.get('/users/:id', (req, res) => {
    const id = parseInt(req.params.id);
    const user = users.find(user => user.id === id);

    if (user) {
        res.json(user);
    } else {
        res.status(404).send('User not found');
    }
});

// Route POST pour ajouter un nouvel utilisateur
app.post('/users', (req, res) => {
    const newUser = {
        id: users.length + 1,
        name: req.body.name
    };
    users.push(newUser);
    res.status(201).json(newUser);
});

// Route PUT pour mettre à jour un utilisateur par ID
app.put('/users/:id', (req, res) => {
    const id = parseInt(req.params.id);
    const updateUser = req.body;
    let found = false;

    users = users.map(user => {
        if (user.id === id) {
            found = true;
            return {
                ...user,
                ...updateUser
            };
        }
        return user;
    });

    if (found) {
        res.json(users.find(user => user.id === id));
    } else {
        res.status(404).send('User not found');
    }
});

// Route DELETE pour supprimer un utilisateur par ID
app.delete('/users/:id', (req, res) => {
    const id = parseInt(req.params.id);
    users = users.filter(user => user.id !== id);
    res.status(204).send();
});

// Démarrage du serveur
app.listen(port, () => {
    console.log(`Server running at http://localhost:${port}`);
});
```

### Utilisation dans un projet ✔️

[Le Comptoir des Seelies](https://github.com/mdonatelli1/Projet-3)

Description : Site E-commerce d'artisanats faits main.

### Utilisation en production si applicable ❌

[lien du projet](...)

Description : /

### Utilisation en environement professionnel ❌

Description : /

## 🌐 J'utilise des ressources

### HTTP Status Codes

- lien : [restapitutorial](https://restapitutorial.com/httpstatuscodes)
- description : Liste des codes HTTP.

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
