# Exercices sur les variables globales

## 1. Correction d'une variable globale inutile

Corrigez le code pour éviter l'utilisation de la variable globale

```javascript
let total = 0; // Variable globale inutile

function ajouter(a, b) {
  total = a + b; // Utilisation de la variable globale
  return total;
}
```

## 2. Correction de plusieurs variables globales inutiles

Corrigez le code pour éviter l'utilisation des variables globales

```javascript
let x = 10; // Variable globale inutile
let y = 20; // Variable globale inutile

function multiplier() {
  return x * y; // Utilisation des variables globales
}
```

## 3. Correction de variables globales inutiles dans une application

Corrigez le code pour éviter l'utilisation de la variable globale

```javascript
let utilisateurConnecte = false; // Variable globale inutile

function connecterUtilisateur() {
  utilisateurConnecte = true; // Utilisation de la variable globale
}

function deconnecterUtilisateur() {
  utilisateurConnecte = false; // Utilisation de la variable globale
}
```

## 4. Conversion de température de Celsius en Fahrenheit

Corrigez le code pour éviter l'utilisation de la variable globale

```javascript
let elements = []; // Variable globale inutile

function ajouterElement(element) {
  elements.push(element); // Utilisation de la variable globale
  return elements;
}
```

## 5. Correction de variables globales inutiles dans une fonction complexe

Corrigez le code pour éviter l'utilisation de la variable globale

```javascript
let resultat = 0; // Variable globale inutile

function calculerResultat() {
  for (let i = 1; i <= 10; i++) {
    resultat += i; // Utilisation de la variable globale
  }
  return resultat;
}
```
