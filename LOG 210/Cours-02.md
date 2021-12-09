# Révision Cours 2

# Cours

## Raisons du MDD

- Favorise une solution claire en termes de classes et d'objets logiciels
- Comprends tous les concepts importants dans le contexte du problème que le logiciel va résoudre
- Fait pour respecter le processus unifié
- MDD est la base de toutes les classes logicielles

### Création de MDD :

- Réutiliser modèle existant
- Catégories de classes
- Groupes nominaux

**Catégories de classes:**

![](/imgs/Categories-classes.png "Categories")

## DSS

**But : Définir l'API (Haut niveau)**

- Identifier l'acteur principal
- Modéliser le système comme objet **sans détail**
- Identifier les événements systèmes :
  - événements externes en entrée
  - Décrits dans un cas d'utilisation
- Proposer une opération système pour chaque événement système
  - Types primitifs pour arguments
  - Messages de retour si nécessaire

## RDCU

**Définitions:**

- Conception des opérations système
- Diagrammes d'intereactions (de séquence)

![Exemple](/imgs/Exemple-dss-rdcu.png "Exemple de DSS")

### Pourquoi RDCU

- apprendre a faire une solution modulaire et intuitive

**Aspects:**

- Proposer des classes logicielles correspondant aux classes conceptuelles
  - Inpirées du MDD
  - Pour réduire le décalage des représentations
- Utiliser les principes GRASP
  - **Faible Couplage** et **Forte Cohésion**
  - **Contrôleur** (architecture en couches)

## Principe Contrôleur GRASP:

**Problème:** quel est le premier objet en dehors de la couche présentation qui reçoit et coordonne ("Contrôle") les opérations système

**Solution:** Affectez une responsabilité à la classe correspondant à l'une des définitions

1. **Contrôleur de facade:** Elle représente le **système global**, un **objet racine**, un **équipement** ou un **sous-système**
1. **Contrôleur de session:** Elle correspond au cas d'utilisation

---

---

# Notes de Cours

**1.2 - 1.3 - 1.4 sont dans le cours 1**

### 4. Modele du domaine

- Les classes conceptuelles ne sont pas des classes logicielles
- Les classes conceptuelles **N'ONT PAS DE MÉTHODES**
- Les classes ont des noms commençant avec une lettre majuscule, les classes ne sont jamais au pluriel

### 4.1 Classes conceptuelles

Pour les identifiers :

- Réutiliser / modifier des modèles existants
- Utiliser une liste de catégories
- Identifier des groupes nominaux

---

---

# Manuel

## Domain Models

- Act as a source of inspiration for designing some software objects
- Input to several artifacts explored in case studies

### 9.2 What is a domain Model

**Definition:** visual representation of conceptual classes or real-situation objects in a domain (not software objects)

- Focuses on one domain
- It is a visual dictionnary of the noteworthy abstractions, domain vocabulary and information content of the domain

**ELEMENTS NOT SUITABLE FOR A IN A DOMAIN MODAL:**

- Software artifacts
- Responsibilities or methods

---

---

# Quiz

## Takeaways :

- Classes conceptuelles n'ont pas de méthodes
- Classes logicielles ont des méthodes
- L'écart des représentation est l'écart des modèles :
  problème vs solution logicielle
- Des classes comme String sont des classes logicielles
- Complexité inhérente provient du logiciel
- Complexité environnementale est hors du contrôle de l'ingénieur
- Classe conceptuelle est une abstraction de concept important dans le cadre du problème que résout le logiciel à développer
- On fait un modèle du domaine pour favoriser une solution claire en termes de classes et d'objets logiciels
- Pour trouver des classes conceptuelles:
  réutiliser un modèle du domaine existant
  identifier les noms dans les CU
  trouver des classes conceptuelles à partir des catégories typiques
  **NOT :** réutiliser les noms des classes logicielles , s'il existe une version antérieur du logiciel

**Artefacts permettant de démontrer l'analyse de CU:**

- DSS
- MDD
- Contrat

_(ceux qui ne peuvent pas : DCL, RDCU, Diagramme de séquence)_

**Aspects liés à l'analyse:**

- Investigation du poblème
- Détermination des exigences
- Observation plutôt que création

**Aspects liés à la conception:**

- Élaboration d'une solution
- Création qui répond aux exigences
