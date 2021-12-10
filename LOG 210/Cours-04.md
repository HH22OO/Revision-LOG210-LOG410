# Cours 4

# Notes de cours

## Contrats d'opérations manuel : section 11

- Pas de spécifications des préconditions dans les contrats
- Correspond à une opération système provenant d'un DSS
- Pas confondre les postconditions d'un contrat d'opération et d'un cas d'utilisation.
- Postcondition décrit les modifications de l'état des objets dans le modèle du domaine. Il s'agit des noms de classes, d'Attributs et d'associations qu'on trouve dans le MDD
- Chaque postcondition doit avoir labonne forme -**création ou suppression d'instances** -**modification des valeurs des attributs** -**formation ou rupture d'associations**

### Définition :

document décrivant ce qui est arrivé après l'exécution d'une opération système.

- présenté sous forme de postconditions
- Permet de spécifier tous les changements dans lMDD qui doivent avoir lieu lors de l'opération système
- les postconditions du contrat saisissent l'évolution du MDD

# Manuel

## Chapter A17.10 GRASP Créateur

### Problem

who should be responsible for creating new instance of some class? It is useful to have a general principle for the assignment of creation responsibilities.
Creation well assigned support :

- low coupling;
- increased clarity
- encapsulation
- reusability

### Solution

Assiggn class B the responsibility to create an instance of class A if \*\*one of these is try(the more the better)

- B "contains" or compositely aggregates A
- B records A
- B closely uses A
- B has the initializing data fgor A that will be passed to A when it is created. Thus B is an expert with respect to creating A

### Discussion

We want to fiund a creator that needs to be connected to the created object in any event. Choosing it as the creator supports low coupling

### Contraindications

creation requires signigicant complexity (recycled instances, conditionnally creating an instance from one of a family...). It is advisable, in this case, to delegate creation to a helper class called a _Concrete Factory_ or an _Abstract Factory_

### Benefits

Low coupling is supported, implies lower maintenance dependencies and higher opportunities for reuse. Coupling is probably not increased

## Chapter A17.11 information Expert

### Problem

what is a general principle of assigning responsibilities to objects ?
During object design, when the interactions between objects are defined, we make choices about the assignement of responsibilities to software calsses. Chosen well, system is easier to understand, maintain and extend

### Solution

Assign a responsibility to the information expert --- the class that has the information necessary to fulfull the responsibility

### Discussion

frequently used in the assignment of responsibilities, basic guiding principle used continuously in object design.

Expert leads to designs where a software object does those operations that are normally done to the inanimate real-world thing it represnets : **Do it Myself**.

- all software objects are alive, animated
- tehy can take responsibilities and do things
- do things related to the information they know

### Contraindications

In some situations, a solution suggested by Expert is undesirabvle, usually because of problems in coupoling and cohesion.

- The class now contains l ogic related to database handling (bad)
- The class no longer focuses on just the pure application logic

### Benefits

- information encapsulation is maintained since objects use their own information to fulfill tasks.
- Support low coupling, leads to more robust and maintainable systems.
- Behavior is distributed across the classes that have the required information, encouraging more cohesive "lightweight" class definitions that are easier to understand and maintain.
- High Cohesionis usually supported

## Chapter A17.13 Controleur

### Problem

What first object beyond the UI layer receives and coordinates ("controls") a system opration

**Definitions:** A controller is the first object beyond the UI Layer that is responsible for receiving or handling a system operation message

### Solution

Assign the responsibility to a class representing one of the following choices :

- Represent the overall "System", a "root-object", a device that the software is running within, or a major subsystem --> _Facade controller_
- Represent a use case scenario within which the system event occurs, often named </UseCaseName/>Handler of Coordinator or Session
  - Use the same controller class for all system events in the same use case scenario
  - informally, a session is an instance of a conversation with an actor. Sessions coan be of any length but are often organized in terms of use cases

### Discussion

this is a delegation pattern. UI layer shouldn't contain application logic , UI layer objects must delegate work requests to another layer
Common defect in the design of controllers results from **over-assignment** of responsibility.
Then, this controller will suffer from low cohesion.

Facade controller are suitable when there are not too many system events, or when the UII cannot redirect system event messages to alternating controllers.
Use case controller, creates multiple different controller for each use case. This kind of controller is not a domain object

When to chose one or the other ? Consider both as alternatives.
If facade leads to high coupling and low cohesion, try use case controllers.

### Benefits

- increased potential for reuse and pluggable interfaces
- application logic is not handled in the interface layer
- opportunity to reason about the state of the use case -- Sometimes we must ensure that system operations occur in a legal sequence, or we want to be able to reason about the current state of activity and operations within the use case that is underway.

# Quiz

## Takeaways

- Partie la plus importantes des contrats sont les postconditions
- L'erreur la plus fréquente selon larman est l'omission de la formation d'association entre les instances
- On applique Createur dans ces scénarios :
  - objets de la classe doigt peuvent etre instanciés par la classe main -- contient
  - objets de la classe ligneVente peuvent etre instanciés par la classe Vente -- étroitement lié + possède Objets
- Principe grasp indiquant qu'il faut donner une responsabilité à une classe qui possède des inforamtions nécessaires pour s'en acquitter : Expert en Information
- Principe grasp qui est une directive générale pour la conception d'objets et d'affectation des responsabilités = Expert en information
- **grasp qui est toujours appliqué lorsqu'on fait une réalisation de cas d'utilisation = Controleur**
- Le modèle du domaine est directement liés aux contrats d'opérations
  - lers postconditions du contrat sont exprimées en termes des éléments du modèle du domaine
- Principe suggèrant ou assigner la responsabilité d'effectuer une opération système = controleur
- On fait des contrats d'opération pour expliciter les détails d'une opération système
- Pour affecter la responsabilité d'instanciation d'objets d'une autre classe, appliquer Créateur
- Pour qu'une postcondition soit valide :
  - **temps de conjugaison au passé**
  - exemple de mauvaise forme : r a été sauvegardé (pas de creation, modification assignation)
- Pour contrat d'opérations : **DSS et MDD** Sont utilisés
