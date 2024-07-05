# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'état (_state_) pour contrôler l'affichage d'un composant ✔️
- les composants enfants et les _props_ qu'on leur passe ✔️
- le déclenchement d'instructions en fonction des actions de l'utilisateur ✔️
- le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ✔️
- l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant ❌
- l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```javascript
import PropTypes from "prop-types";

// Définition du composant PokemonCard
function PokemonCard({ pokemon }) {
    return (
        <figure>
            {/* Condition pour afficher l'image du Pokémon */}
            {pokemon.imgSrc !== undefined ? <img src={pokemon.imgSrc} alt={pokemon.name} /> : <p>???</p>}
            {/* Affichage du nom du Pokémon */}
            <figcaption>{pokemon.name}</figcaption>
        </figure>
    );
}

// Spécification des types des propriétés attendues avec PropTypes
PokemonCard.propTypes = {
    // pokemon est un objet avec une structure spécifique
    pokemon: PropTypes.shape({
        // name est une chaîne de caractères requise
        name: PropTypes.string.isRequired,
        // imgSrc est une chaîne de caractères optionnelle
        imgSrc: PropTypes.string
    }).isRequired // pokemon est requis
};

// Export du composant PokemonCard pour pouvoir l'utiliser ailleurs
export default PokemonCard;
```

### Utilisation dans un projet ✔️

[Casino666](https://github.com/mdonatelli1/Casino666)

Description : Escape Game dans un casino.

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
