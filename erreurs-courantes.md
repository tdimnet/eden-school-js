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

### 2.1. Exemple 1 :  Addition de deux nombres

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


### 2.3. Exemple 3 :  Calcul de l'aire d'un rectangle

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

### 3.1. Exemple 1 :  

```JavaScript
```

**Explications** :

### 3.2. Exemple 2 :  

```JavaScript
```

**Explications** :

### 3.3. Exemple 3 :  

```JavaScript
```

**Explications** :



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

### 4.1. Exemple 1 :  

```JavaScript
```

**Explications** :

### 4.2. Exemple 2 :  

```JavaScript
```

**Explications** :

### 4.3. Exemple 3 :  

```JavaScript
```

**Explications** :


## 5. Ne pas appeler la fonction
Oublier d'appeler la fonction peut être une erreur courante. Assurez-vous d'appeler la fonction avec les arguments appropriés lorsque vous souhaitez exécuter son code.

```javascript
function saluer(nom) {
  console.log(`Bonjour, ${nom} !`);
}

// Oubli de l'appel à la fonction
saluer("Alice");
```

### 5.1. Exemple 1 :  

```JavaScript
```

**Explications** :

### 5.2. Exemple 2 :  

```JavaScript
```

**Explications** :

### 5.3. Exemple 3 :  

```JavaScript
```

**Explications** :


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

### 6.1. Exemple 1 :  

```JavaScript
```

**Explications** :

### 6.2. Exemple 2 :  

```JavaScript
```

**Explications** :

### 6.3. Exemple 3 :  

```JavaScript
```

**Explications** :

