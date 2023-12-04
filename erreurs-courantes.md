# Erreurs courantes lors de l'apprentissage des fonctions en JavaScript

Lorsque l'on apprend les fonctions en programmation, il est courant de commettre certaines erreurs.

Voici quelques-unes des erreurs les plus courantes quand on apprend les fonctions en JavaScript. Vous trouverez aussi des conseils pour les éviter :

## 1. Oublier de retourner une valeur

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

### 1.1. Exemple 1 - Addition de deux nombres

```javascript
// Mauvais exemple
function ajouter(a, b) {
  a + b; // Oubli du return
}

const resultat = ajouter(3, 5);
console.log(resultat); // Affichera "undefined"
```

**Explications** :
Dans cet exemple, la fonction ajouter effectue l'addition de deux nombres, mais elle oublie de renvoyer le résultat à l'aide de l'instruction return. Par conséquent, lorsque nous appelons ajouter(3, 5), la valeur de retour est undefined, car la fonction ne renvoie rien.

### 1.2. Exemple 2 - Calcul de la somme des éléments d'un tableau

```javascript
// Mauvais exemple
function sommeTableau(tableau) {
  let somme = 0;
  for (let i = 0; i < tableau.length; i++) {
    somme += tableau[i];
  }
  // Oubli du return
}

const valeurs = [1, 2, 3, 4, 5];
const resultat = sommeTableau(valeurs);
console.log(resultat); // Affichera "undefined"
```

**Explications** :
Dans cet exemple, la fonction sommeTableau additionne les éléments d'un tableau, mais elle oublie également de renvoyer la somme calculée. Par conséquent, la valeur de retour est undefined.

### 1.3. Exemple 3 : Recherche de l'élément maximum dans un tableau

```javascript
// Mauvais exemple
function trouverMaximum(tableau) {
  let maximum = 0;
  for (let i = 0; i < tableau.length; i++) {
    if (tableau[i] > maximum) {
      maximum = tableau[i];
    }
  }
  // Oubli du return
}

const valeurs = [12, 45, 6, 78, 23, 56];
const resultat = trouverMaximum(valeurs);
console.log(resultat); // Affichera "undefined"
```

**Explications** :
Dans cet exemple, la fonction trouverMaximum parcourt un tableau pour trouver l'élément maximum, mais elle oublie de renvoyer la valeur maximale trouvée. Encore une fois, la valeur de retour est undefined.

## 2. Confondre paramètres et arguments

```javascript
function multiplier(x, y) {
  return x * y;
}

multiplier(2, 3); // 2 et 3 sont des arguments
```

### 2.1. Exemple 1 : Addition de deux nombres

```JavaScript
function ajouter(a, b) {
  return a + b;
}

const resultat = ajouter(3, 5);
console.log(resultat); // Affichera "8"
```

**Explications** :
Dans cet exemple, la fonction `ajouter` prend deux paramètres `a` et `b` et renvoie leur somme. L'appel `ajouter(3, 5)` fournit les arguments corrects, évitant ainsi la confusion entre les paramètres et les arguments.

### 2.2. Exemple 2 : Concaténation de chaînes

```JavaScript
function concatener(chaine1, chaine2) {
  return chaine1 + chaine2;
}

const resultat = concatener("Bonjour, ", "monde !");
console.log(resultat); // Affichera "Bonjour, monde !"
```

**Explications** :
Dans cet exemple, la fonction `concatener` prend deux paramètres `chaine1` et `chaine2` et renvoie la concaténation de ces deux chaînes. L'appel `concatener("Bonjour, ", "monde !")` utilise les arguments appropriés, évitant ainsi la confusion.

### 2.3. Exemple 3 : Calcul de l'aire d'un rectangle

```JavaScript
function calculerAireRectangle(longueur, largeur) {
  return longueur * largeur;
}

const aire = calculerAireRectangle(5, 10);
console.log(aire); // Affichera "50"
```

**Explications** :
Dans cet exemple, la fonction `calculerAireRectangle` prend deux paramètres `longueur` et `largeur` et renvoie l'aire du rectangle en multipliant ces deux valeurs. Les arguments fournis dans l'appel `calculerAireRectangle(5, 10)` sont corrects, évitant toute confusion entre paramètres et arguments.

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

### 3.1. Exemple 1 : Ajout de deux nombres avec une variable globale inutile

```JavaScript
let total = 0; // Déclaration d'une variable globale inutile

function ajouter(a, b) {
  total = a + b; // Modification de la variable globale
}

ajouter(3, 5);
console.log(total); // Affichera "8"
```

**Explications** : Dans cet exemple, une variable globale inutile `total` est déclarée en dehors de la fonction `ajouter`, puis elle est modifiée à l'intérieur de la fonction. Les variables globales devraient être évitées lorsque possible, et dans ce cas, elle est inutile.

### 3.2. Exemple 2 : Utilisation de variables globales pour le stockage temporaire

```JavaScript
let resultat = 0; // Déclaration d'une variable globale inutile

function multiplier(a, b) {
  resultat = a * b; // Modification de la variable globale
}

multiplier(4, 7);
console.log(resultat); // Affichera "28"
```

**Explications** : Dans cet exemple, une variable globale inutile `resultat` est utilisée pour stocker temporairement le résultat d'une multiplication à l'intérieur de la fonction. L'utilisation de variables locales serait préférable pour éviter les effets secondaires.

### 3.3. Exemple 3 : Gestion d'états avec des variables globales inutiles

```JavaScript
let compteur = 0; // Déclaration d'une variable globale inutile

function incrementer() {
  compteur++; // Modification de la variable globale
}

function afficherCompteur() {
  console.log(compteur); // Lecture de la variable globale
}

incrementer();
afficherCompteur(); // Affichera "1"
```

**Explications** : Dans cet exemple, une variable globale inutile `compteur` est utilisée pour stocker un état qui est modifié et lu par différentes fonctions. Cette utilisation de variables globales peut entraîner des problèmes de lisibilité et de gestion de l'état.

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

### 4.1. Exemple 1 : Calcul de la moyenne avec des noms de variables ambigus

```JavaScript
function calc(a, b, c) {
  const avg = (a + b + c) / 3; // Utilisation d'un nom de variable ambigu "avg" pour la moyenne
  return avg;
}

const result = calc(10, 20, 30);
console.log(result); // Affichera "20"
```

**Explications** : Dans cet exemple, la fonction utilise un nom de variable ambigu "avg" pour stocker la moyenne des nombres `a`, `b`, et `c`. Utiliser des noms de variables plus descriptifs comme "moyenne" rendrait le code plus compréhensible.

### 4.2. Exemple 2 : Concaténation de chaînes avec des noms de variables ambigus

```JavaScript
function concat(a, b) {
  const str = a + b; // Utilisation d'un nom de variable ambigu "str" pour la chaîne concaténée
  return str;
}

const result = concat("Bonjour, ", "monde !");
console.log(result); // Affichera "Bonjour, monde !"
```

**Explications** : Dans cet exemple, la fonction utilise un nom de variable ambigu "str" pour stocker la chaîne concaténée. Utiliser un nom de variable plus descriptif comme "chaineConcatenee" améliorerait la clarté du code.

### 4.3. Exemple 3 : Calcul de la somme avec des noms de variables ambigus

```JavaScript
function sum(numbers) {
  const total = numbers.reduce((acc, num) => acc + num, 0); // Utilisation d'un nom de variable ambigu "total" pour la somme
  return total;
}

const values = [10, 20, 30];
const result = sum(values);
console.log(result); // Affichera "60"
```

**Explications** : Dans cet exemple, la fonction utilise un nom de variable ambigu "total" pour stocker la somme des nombres dans un tableau. Utiliser un nom de variable plus explicite comme "somme" serait préférable pour améliorer la compréhension du code.

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

### 6.1. Exemple 1 : Modification du paramètre directement

```JavaScript
function doubler(x) {
  x = x * 2; // Modification du paramètre directement
  return x;
}

const resultat = doubler(5);
console.log(resultat); // Affichera "10"
```

**Explications** : Dans cet exemple, la fonction `doubler` prend un paramètre `x` et essaie de doubler sa valeur en modifiant `x` directement. Cela peut créer des effets secondaires inattendus, car cela modifie la valeur passée en argument.

### 6.2. Exemple 2 : Modification du tableau passé en paramètre

```JavaScript
function ajouterElement(tableau, element) {
  tableau.push(element); // Modification du tableau passé en paramètre
}

const maListe = [1, 2, 3];
ajouterElement(maListe, 4);
console.log(maListe); // Affichera "[1, 2, 3, 4]"
```

**Explications** : Dans cet exemple, la fonction `ajouterElement` prend un tableau et un élément à ajouter, puis elle modifie directement le tableau en ajoutant l'élément. Cette modification directe du tableau passé en paramètre peut provoquer des effets secondaires inattendus.

### 6.3. Exemple 3 : Modification de l'objet passé en paramètre

```JavaScript
function modifierPersonne(personne) {
  personne.age = 30; // Modification de l'objet passé en paramètre
}

const alice = { nom: "Alice", age: 25 };
modifierPersonne(alice);
console.log(alice); // Affichera "{ nom: 'Alice', age: 30 }"
```

**Explications** : Dans cet exemple, la fonction `modifierPersonne` prend un objet `personne` et modifie directement la propriété `age` de cet objet. Cette modification directe de l'objet passé en paramètre peut avoir des conséquences inattendues sur d'autres parties du code.
