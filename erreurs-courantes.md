# Erreurs courantes lors de l'apprentissage des fonctions en JavaScript

Lorsque l'on apprend les fonctions en programmation, il est courant de commettre certaines erreurs.

Voici quelques-unes des erreurs les plus courantes quand on apprend les fonctions en JavaScript. Vous trouverez aussi des conseils pour les éviter :


## 1. Oublier de retourner une valeur
L'omission de l'instruction `return` ou de la valeur de retour dans une fonction peut entraîner des résultats inattendus. Assurez-vous que chaque chemin d'exécution de la fonction renvoie une valeur appropriée si nécessaire.

```javascript
// Mauvais exemple
function ajouter(a, b) {
    a + b; // Oubli du return
}

// Bon exemple
function ajouter(a, b) {
    return a + b;
}
```


## 2. Confondre paramètres et arguments
Les débutants ont souvent du mal à comprendre la différence entre les paramètres (déclarés dans la signature de la fonction) et les arguments (fournis lors de l'appel de la fonction). Assurez-vous que les noms et les positions correspondent correctement.

```javascript
function multiplier(x, y) {
  return x * y;
}

multiplier(2, 3); // 2 et 3 sont des arguments
```

## 3. Déclarer des variables globales inutiles
Évitez de créer des variables globales lorsque cela n'est pas nécessaire. Utilisez plutôt des variables locales dans la fonction pour éviter les conflits de noms et améliorer la lisibilité du code.

```javascript
// Mauvais exemple
let total = 0;

function ajouter(a, b) {
  total = a + b; // Modifie la variable globale
}

// Bon exemple
function ajouter(a, b) {
  let total = a + b; // Utilise une variable locale
  return total;
}
```

## 4. Utiliser des noms de variables ambigus
Utilisez des noms de variables et de fonctions descriptifs pour rendre votre code plus lisible et éviter les confusions. Évitez les noms de variables tels que x, y, ou data.

```javascript
// Mauvais exemple
function calc(x, y) {
  return x + y;
}

// Bon exemple
function additionner(nombre1, nombre2) {
  return nombre1 + nombre2;
}
```

## 5. Ne pas appeler la fonction
Oublier d'appeler la fonction peut être une erreur courante. Assurez-vous d'appeler la fonction avec les arguments appropriés lorsque vous souhaitez exécuter son code.

```javascript
function saluer(nom) {
  console.log(`Bonjour, ${nom} !`);
}

// Oubli de l'appel à la fonction
saluer("Alice");
```

## 6. Modifier les paramètres
Évitez de modifier les paramètres directement à l'intérieur de la fonction, car cela peut provoquer des effets secondaires inattendus. Utilisez des variables locales pour effectuer des modifications si nécessaire.

```javascript
// Mauvais exemple
function doubler(x) {
  x = x * 2; // Modifie le paramètre directement
  return x;
}

// Bon exemple
function doubler(x) {
  let resultat = x * 2; // Utilise une variable locale
  return resultat;
}
```
