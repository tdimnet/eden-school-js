# Exercices sur les arguments et paramètres

## 1. Addition de deux nombres

Le code suivant essaie d'effectuer une addition de deux nombres en utilisant une fonction. Cependant, il y a une confusion entre les paramètres et les arguments. Identifiez cette confusion et corrigez le code pour qu'il renvoie la somme correcte de 3 et 5.

```javascript
function addition(a, b) {
  return a + b;
}

const resultat = addition(3, 5, 2); // Devrait retourner 8
```

## 2. Concaténation de chaînes de caractères

Dans le code ci-dessous, une fonction tente de concaténer deux chaînes de caractères pour former une salutation. Cependant, il y a une confusion entre les paramètres et les arguments. Identifiez cette confusion et corrigez le code pour qu'il renvoie la chaîne "Bonjour, monde!" en concaténant "Bonjour, " et "monde!".

```javascript
function concatenation(chaine1, chaine2) {
  return chaine1.concat(chaine2);
}

const resultat = concatenation("Bonjour, ", "monde!", "Salut"); // Devrait retourner "Bonjour, monde!"
```

## 3. Multiplication de nombres

Dans le code ci-dessous, une fonction devrait effectuer une multiplication de deux nombres. Cependant, il y a une confusion entre les paramètres et les arguments. Identifiez cette confusion et corrigez le code pour qu'il renvoie le produit correct de 10 et un autre nombre de votre choix.

```javascript
function multiplication(a, b) {
  return a * b;
}

const resultat = multiplication(10); // Devrait retourner le produit correct
```

## 4. Calcul du périmètre d'un rectangle

Le code suivant tente de calculer le périmètre d'un rectangle en utilisant une fonction. Cependant, il y a une confusion entre les paramètres et les arguments. Identifiez cette confusion et corrigez le code pour qu'il renvoie le périmètre correct d'un rectangle avec une longueur de 5 unités et une largeur de 3 unités.

```javascript
function calculerPerimetre(longueur, largeur) {
  return 2 * (longueur + largeur);
}

const resultat = calculerPerimetre(); // Devrait retourner le périmètre correct
```

## 5. Calcul de la puissance d'un nombre

Dans le code ci-dessous, une fonction devrait calculer la puissance d'un nombre en utilisant un exposant donné. Cependant, il y a une confusion entre les paramètres et les arguments. Identifiez cette confusion et corrigez le code pour qu'il renvoie la puissance correcte de 2 avec un exposant de votre choix.

```javascript
function puissance(base, exposant) {
  return Math.pow(base, exposant);
}

const resultat = puissance(2); // Devrait retourner la puissance correcte
```
