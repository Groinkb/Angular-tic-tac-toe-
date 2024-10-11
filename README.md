# Angular Tic-Tac-Toe

**Date de création :** 19 juillet 2024  
**Dernière mise à jour :** 4 octobre 2024  

## Description

Ce projet est une implémentation d'un jeu **Tic-Tac-Toe** développé avec **Angular**. Il couvre plusieurs concepts clés du développement d'applications avec Angular :

- **Composants Angular** : Implémentation du composant `SquareComponent` pour représenter chaque case du jeu.
- **Tests unitaires** : Utilisation de **Jasmine** et **Karma** pour tester les composants Angular (exemple : tests pour `SquareComponent` et `AppComponent`).
- **Entrées/Sorties** : Utilisation de l'annotation `@Input()` pour transmettre des valeurs aux composants.
- **Templates** : Utilisation des directives Angular telles que `*ngIf` pour rendre dynamiquement les boutons selon l'état du jeu (X ou O).
- **Style réactif** : Intégration de **Nebular** pour styliser les boutons avec des statuts héroïques pour les valeurs X et O.

## Installation

### Prérequis

Avant de pouvoir utiliser ce projet, vous devez avoir les outils suivants installés sur votre machine :

1. **Node.js**  
   [Télécharger Node.js](https://nodejs.org/en/download/)

2. **Angular CLI**  
   Installez Angular CLI globalement :  
   ```bash
   npm install -g @angular/cli

Étapes d'installation
Clonez ce dépôt :

bash
Copier le code
git clone https://github.com/Groinkb/Angular-tic-tac-toe-.git
Accédez au dossier du projet :

bash
Copier le code
cd Angular-tic-tac-toe-
Installez les dépendances :

bash
Copier le code
npm install
Lancez le serveur de développement :

bash
Copier le code
ng serve
Le jeu sera disponible à l'adresse suivante : http://localhost:4200/.

Captures d'écran
Voici quelques captures d'écran illustrant l'état du projet à différentes étapes :

Premier rendu du composant Square :

Résultat attendu d'une partie gagnante pour X :

Test unitaire pour le composant App :

Support
Si vous rencontrez des problèmes ou avez des questions concernant ce projet, vous pouvez me contacter à l'adresse suivante :
benjamin@mossu.ch

Roadmap
Voici quelques améliorations à venir pour ce projet :

Ajouter la fonctionnalité de partie multijoueur en ligne.
Inclure des effets visuels lors de la victoire.
Optimisation pour les appareils mobiles.
Les suggestions d'amélioration peuvent être partagées dans le README ou via des issues.

Contributions
Les contributions sont les bienvenues. Si vous souhaitez contribuer à ce projet, voici quelques consignes :

Forkez le projet.
Créez une branche pour vos modifications.
Soumettez une pull request avec une description claire des modifications.
N'oubliez pas d'exécuter les tests unitaires (ng test) pour vérifier que votre code n'introduit pas de régressions.
Auteurs et remerciements
Développé par Groinkb.

N.B. : Ce projet est en cours de développement. Certains fichiers ou fonctionnalités peuvent changer à l'avenir.

bash
Copier le code

### Correct display:

1. **Titres** : Ils commencent par un `#` suivi d'un espace. Par exemple :  
   ```markdown
   # Mon Titre
Blocs de code : Utilisez trois accents graves 
‘
‘
‘
‘‘‘ avant et après vos blocs de code pour bien les formater, par exemple :
markdown
Copier le code
```typescript
import { Component, Input } from '@angular/core';

@Component({
  selector: 'app-square',
  template: `
    <button nbButton *ngIf="!value">{{ value }}</button>
    <button nbButton hero status="success" *ngIf="value == 'X'">{{ value }}</button>
    <button nbButton hero status="info" *ngIf="value == 'O'">{{ value }}</button>
  `,
  styles: ['button { width: 100%; height: 100%; font-size: 5em !important; }']
})
export class SquareComponent {
  @Input() value: 'X' | 'O';
}
