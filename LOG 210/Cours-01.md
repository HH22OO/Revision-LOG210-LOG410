# Révisions Cours 1

# Cours

### Création d'un logiciel

**On souhaite appliquer un processus pour la réalisation:**

- Application d'une méthodologie d'analyse
- Application d'une méthodologie de conception
- Identification des méthodologies existante pour l'implémentation

#### Spectre de la conception

![](/imgs/spectre-de-la-conception.png "Spectre de la conception")

- Effectuer suffisament d'analyse de conception pour savoir ou l'on s'en va.
- Limiter la conception pour éviter de travailler inutilement

### Modèles utilisés

#### Aspect Analyse

##### Diagrammes de cas d'utilisation

- Acteurs couplés à des cas d'utilisations
- C'est une table des matières
- Qui sont les acteurs et les cas d'utilisations qui lui sont liés

**À partir du DCU, on trouve le MDD**

##### Modèle du domaine

**Définition:**
Représentation visuelle des calsses conceptuelles | objets du monde réel dans un domaine donné :

- modèle conceptuel
- modèle objet du domaine
- modèle objet d'analyse

**Création d'un MDD:**

- On identifie les classes conceptuelles
- On les représente sous formes de classes dans un diagramme UML
- On identifie les associations et les attributs des classes
- On ajoute des verbe pour décrire des associations
- On identifie la multiplicité entre les associations

C'est l'aspect de représentation des données, un aspect statique.
Normalement, le MDD se calque sur les cas d'utilisations. L'information retrouvée dans les CU est présente dans le MDD.

##### Diagramme de séquences système

**Définition:**
C'est une interaction avec le système. L'interaction est entre un acteur, qui génère des événements, et le système, qui envoie des réponses. Le DSS illustre ces opérations

- Un acteur interagit avec un système
- Le système est une boîte noire
- On retrouve les interactions acteur <--> système (opérations systèmes)

##### Contrat

- Définit les transformations dans le modèle
- Présent pour chaque opération système

#### Aspect Conception

##### Réalisation d'un cas d'utilisation

- Composé d'un diagramme de séquence et de patron GRASP
- Un diagramme de séquence par opération système / contrat
- Ces deux artefacts contraignent le RDCU (les postconditions sont respectées, les retours sont présents)

##### Diagramme de classe logiciel DCL

- Construit à l'aide des RDCU : rajoute les opérations/méthodes
- On ramène l'information contenue dans le MDD

Après cela, implémentation

On implément les classes avec le moins de couplage pour la solution

![](/imgs/relations-entre-artefacts.png "Spectre de la conception")

---

### Partie Humilité | Confiance | Respect

**Jugée non importante**

---

---

# Notes de cours

### Analyse vs Conception

**Analyse:**

- L'analyse met l'accent sur une investigation du problème et des besoins

**Conception:**

- La conception met l'accent sur la recherche d'une solution
- Élaboration d'une solution conceptuelle pas de mise en oeuvre de la solution

### Décalage des représention

- Modèle du problème ressemble beaucoup au modèle de la solution
- Différence car un esolution comporte des détails sur la dynamique du jeu qui sera codée
- Le modèle du problème et le modèle de la solution ne sont pas identiques
- **On veut que la solution(conception) ressemble à une description (modèle d'analyse) du problème**
- Se mefier des classes importantes au noms difficiles à tracer au problème

### Complexité et ses sources

**Définition:** caractère de ce qui est complexe, difficle à comprendre, de ce qui content plusieurs éléments.

**Complexité inhérente (provenant du problème):**

- Au sein du problème résolu par le logiciel
- Composée des parties du logiciels qui sont des problèmes difficiles
- Un logiciel tentant de résoudre ces problèmes aura une manifestation de cette complexité dans son implémentation

**Complexité circonstancielle (provenant des choix de conception):**

- Choix fait par les ingénieurs
- Le singénieurs doivent contrôller cette complexité peut être due à des contraintes imposées sur la conception
- Peut-être gérée avec des technologies (débogueurs patrons de conception)

**Complexité environnementale (provenant de l'environnement d'exécution)**

- Comprend des aspects d'une solution hors du contrôle des ingénieurs

### Développement itératif, évolutif et agile

- Développement itératif et évolutif implique de programmer et de tester précocement un système partiel selon des cycles répétitifs
- Un cycle est une itération, dure un temps fixe, comprends des activités d'analyse, de conception de programmation et de test, ainsi qu'une démonstration
- La durée d'un eitération est limitée dans le temps
- On ne peut pas ajouter de temps, on reporte

#### Avantages :

- Moins d'échecs, améliorations de la productivité et de la qualité
- Gestion précoces des risques élevés
- Progrès immédiatement visibles
- Rétroaction, implication des utilisateurs et adaptations précoces
- Complexité gérée (par itération)
- Possibilité d'exploiter méthodiquement les leçons tirées

---

---

# Manuel

## Chapter 1

### OOD Principles and Patterns

- How should **responsabilities** be allocated to classes of objects
- How should obects collaborate
- What classes should do what

### Analysis and Design

**Analysis:**

- Emphasizes an investigation of the problem and requirements, rather than a solution
- Requirements analysis : investigation of the requirements
- Object -oriented analyss : investigation of the domain objects

**Design:**

- Emphasizes a conceptual solution fulfilling the requirements, rather than its implementation
- Design ideas often includes low level | "obvious" details
- Ultimately, designs can be implemented
- Object-oriented design
- Database design

##### SUMMARIZE OF ANALYSIS AND DESIGN : do the right thing (analysis), and do the thing right (design)

### What is Object-Oriented Analyse and Design (OOA/D)

- During **object-oriented analysis**, there is an emphasis on finding and describing the objects | concepts in the problem domain
- During **object-oriented design**, there is an emphasis on defining software objects and how they collaborate to fulfill the requirements
- During implementation, or object-oritend programming, design objects are implemented

### Definitions

#### Use Cases

- Not an OO artifact
- Written stories

#### Domain Model

- Identification of the concepts, attribtues and associations that are considered noteworthy
- Not a description of software objects; visualisation of the concepts or mental models of a real world domain
- Also called a **conceptual object model**

#### Interaction Diagrams

- **Sequence diagrams** shows the flow of messages between software objects, and thus, the invocation of methods
- Not direct models or simulations of the real world

#### Design Class Diagrams

- Static view of the class definitions
- Illustrates the attributes and methods of the classes
- In contrast to the domain model, it shows software classes
- Content are similar between the two (**lower representational gap**)

## Chapter 9.3 - Why create a Domain Model

- Understand key concepts and vocabulary
- Use software class names in the domain layer inspired from names in the the domain model

## Chapter 2

**Iterative and evolutionary development** involves:

- Early programming
- Testing of a partial system
- Repeating cycles

### What is UP? Are other methods complementary

- Software development process describes an approach to building, deploying maintaining software
- **Unified process** (UP) is an iterative software development process for building object-oriented systems
- **Rational Unified Process** (RUP) is a detailed refinement of the UP
