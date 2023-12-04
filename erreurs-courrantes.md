# Erreurs courantes lors de l'apprentissage des fonctions en JavaScript

Lorsque l'on apprend les fonctions en programmation, il est courant de commettre certaines erreurs.

Voici quelques-unes des erreurs les plus courantes quand on apprend les fonctions en JavaScript. Vous trouverez aussi des conseils pour les éviter :

## 1. Oublier de retourner une valeur :
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
