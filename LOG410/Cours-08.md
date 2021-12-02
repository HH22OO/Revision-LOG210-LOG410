# Cours 8

## Pieges des CU :

- CU incompris par les utilisateurs
- Trop de CU
- CU trop complexes faire l'erreur de décrier l'interface utilisateur et les actions
- Se limiter à un seul modèle de requis

## CMMI modele dev

CMMI :

- Capability maturity model integrated for dev

- Collection des meilleures pratiques qui aide les entreprisesà amélioer leurs processus
- Possede 22 process areas

Structure du model :

- diviser en categorie de practices called process areas
- requirements development (RD)
- requirements management (RM)
- project planning
- project mo nitoring and control
- supplier agreement managment
- risk management
- technical solutions
- product integration
- verification
- validation
- organizational process focus
- organizational process definition
- integradeted project management
- organizational training
- organizational process performance
- quantitive project management
- organizational performance management
- casual analysis and resolution

process area :
practices specific of the work (specific practices)

- specific foals / practices
  Sustainning the work
- generic goals/pratices

## Étiquette RFID (Radio grequency ID)

## Video a regarder

### Clarifier les CU

- objectif : creer de lea valeur pour nos utilisateurs
- Faire en sorte que la valeur soit observable
- Les utilisateurs doivent pouvoir regarder les cu et trouver des problèmes
- Pas trop de CU -- simplifier
- **Pas plus que 12 etapes** dans le scénario principal
- On reste au niveau de la surface

### Précisions concernant les exigences

- Les gens vont verifier ce qu'on a deja entendu (pas de surprise)
- on considere ca comme étant le sweet spot.
- Toutes les informations pertinents on été capturés
- S'arreter à ce moment la
- Diagramme a état fini : modele pour les technologies utilisant des états

### CU vers cas de tests

- Implantation directe de la conception au code : merveilleux lorsque possible
- Difficulté de déterminer comment et ou sont implantées les exigences : problème d'orthogonalité :
  - peu de corrélation entre les exigences et la conception et l'implémentation
  - la forme de nos exigences et la form de conception et de l'implantation sont différentes
  - Il n'y a pas de facon facile de suivre ou de retracer de l'exigence à la conception et au code

**Types de test:**

- Module, composant ou test unitaire : vérifie les fonctions des composants dans un environnmenet controlé
- Test d'intégration : vérifie si les composants fonctionnent ensemble dans un système intégré
- Test fonctionnel: vérifie la conformité des fonctionnalités systèmes avec les exigences fonctionnels spécifiées au départ
- Tests de performance: s'assure du temps réponse, doit être fait dans le même environnement que celui utilisé par le client
- Test d'installation : le système est déployé dans l'environnement du client et nous devons nous assuer que tout foncitonne bien
  - Demande un roadback pour revenir en arrière en cas de problème

Des cas d'utilisation aux cas de test

1. Identifier les scenarios du cas d'utilisation
1. pour chaque scénarion, identifier un ou des cas de test
1. pour chaque cas de test, identifier les conditions qui vont causer son exécution
1. Completer le cas de test en ajoutant des valeurs aux données

**Scénario:** ou une instance d'un cas d'utilisation est une exéctution d'un cas d'utilisation dans laquelle un utilisateur particulier exécute le cas d'utilisation de manière spécifique

pour chaque scénario:

- On ajoute un ligne dans la matrice des cas de test
- On identifier les données concernees par l'exécution spécifique du scénario
- On identifier le resultat attendu
- Matrice des cas de test

On identifie les conditions de test : valide ou vrait, invalide ou fausse non applicable

### Gestion des changements

#### Facteurs externes du changement :

- Changement survient au problème que l'on tente de solutionner avec le nouveau système
- L'utilsateur change d'idees ou la perception de ce que le système doit faire Environnment externe a changé, créant ainsi de nouvealles contraintes et /ou de nouvelles opportunités
- un facteur externe est la venu du système lui même

#### Facteurs internes :

- oublier de demander aux bonnes personnes les bonnes questions
- Faillis à creer un processus pratique afin d'aider à géer les changements aux exigences
- L'itération des exigencesà la conception engendre de nouvelles exigences

#### Fuites des exigences :

- requetes transmise directement au développeur des erreurs qui doivent être supportées (deja livrées)
- Caractéristiques du matériels qui n'a pas été incluse ou qui ne foncitonne pas
- easter egg

Pour gérer les changements :

1. Reconnaitre que les changements son inébitables et les prévoir
1. Établir la base de référence des exigences
1. Étabkir un canal lunique pour controler le changement
1. Utiliser un système de controle afin de capturer les changements
1. Gérer le changement hiérarchiquement

### Modele CMMi-Dev
