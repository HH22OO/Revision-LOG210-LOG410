# Cours 10

# Notes de cours

## Développement itératif, évolutif et agile

Points importants du processus itératif et adaptatif ainsi que les concepts fondamentaux du Processus Unifié

- Le développement itératif et évolutif implique de programmer et de tester précocement un système partiel selon des cycles répétitifs
- Un cycle est nommé une itération et dure un temps fixe comprenant les activités d'analyse, de conception, de programmation et de test, ainsiqu'une démonstration pour solliciter des rétroactions du client
- La durée d'une itération est limitée dans le temps, de 2 à 6 semaines. Il n'Est pas permis d'ajouter du temps à la durée d'une itération si le projet avance plus lentement que prévu, car cela impliquerait un retard de la rétroaction du client. Si le respect des délais semble compromis on supprime plutôt des tâches ou des spécifications et on les inclut dans l'itération suivante.
- Les premières itérations peuvent semble chaotiques, car elles sont loin de la bonne voie. Avec la rétroaction du client et l'Adaptation, le système à développer converge vers une solution appropriée
- Il y a plusieurs avantages du développement itératif et incrémental :
  - moins d'échecs, amélioration de la productivité et de la qualité
  - gestion précoce des risques élevés (risques techniques, exigences, objectifs, convivialité ...)
  - rétroaction, implication des utilisateurs et adaptations précoces
  - complexité gérée (par itération)
  - possibilité d'exploiter méthodiquement les leçons tirées d'une itération

## Besoins (exigences)

Exigences d'une foncitonnalité : ce que le système fait
Exigences sur la qualité de la performance : a quel point le système fait-il bien les choses

### FURPS+ manuel : section 5.4

C'est un modèle pour classer les exigences d'un logiciel

- **Functionality | Fonctionnalité :** exigences exprimées souvents par les cas d'utilisation
- **Usability | Aptitude à l'utilsation :** Convivialité - les facteurs humains du logiciel, facilité d'utilisation/compréhension
- **Reliability | Fiabilité :** comportement lors des pannes
- **Performance :** comportement lors de surcharges de système
- **Supportability | Possibilité de prise en charge :** adaptabilité ou maintenabilité, facilité de modifications pour les changements imprévus
- **+ :** comprends implémentaiton, interface, exploitation, Aspect juridiques

# Manuel

## Chapter 2 Iterative, Evolutionnary and Agile

we talk here of agile, iterative development and Unified process as a relatively popular sample iterative method

Contrasted with a sequential or waterfall lifecycle, iterative and evolutionary development involves early programming and testing of a partial system, in repeating cycles.

Development start before all requirements are defined
Rely on short, quick development steps, feedback, and adaptation to clarify the requirements and design.

### What is the UP

**Definition:** a software development process describes an approach to building, deploying, and possibly maintaining software. The **Unified Process** has emerged as a popular **_Iterative_ software development process** for building object oriented systems.

It is common and promotes widely recognized best practices. It is very flexible and open, encourages including other skillful practices from other iterative methods - extreme programming - scrum - TDD - refactoring - continuous integration

It combines commonly accepted best practices :

- iterative lifecycle
- risk-driven development
- well documented process description

**The result of each iteration is an executable but incomplete system; it is not ready to deliver into production. The output of an iteration is _not_ an experimental or throw away prototype**

### Agile Methods and attitudes

usually applies timeboxed iteratives and evolutionary development, employ adaptative planning, promote incremental delivery -- includes practices that envourage agility

### UP phases :

- Inception : approximate vision, business case, scope, vague estimates
- Elaboration : Refined vision, iterative implementation of the core architecture, resolution of high risks, identification of most requirements and scope
- Construction : iterative implementation of the remaining lower risk and easier elements and preparation for deployment
- Transition : beta test, deployment

# Quiz

## Takeaways

- Selon UP, activités de conception sont requise, mais ne sont que des esquisses de la solution
- UP favorise l'adoption d'uml avec des pratiques de modélisation agiles
- caractéristiques désirables d'un design :
  - complexité minimale
  - couplage faible
  - extensibilité
  - facilité de maintenance
  - réutilisabilité
  - protabilité
  - cohésion forte
- UP phases : Inception, Elaboration, Construction, Transition
- L'Exigence de supportability | possibilités de prise en charge est appuyé par le principe de réduction d'écart de représentation
- Il n'y a pas de plan détaillé du projet entier dans le UP
- Le processus unifié n'est pas simplement une variation du modèle en cascade, Inception != analyse, élaboratin != conception et construction != implémentation
- Objectif du UP : réduire les risques (techniques, spécifications objectifs). Comment : en faisant du développment itératif et évolutif, organisé dans les courtes itérations
- La construction est utilisé pour guider le codage dans chaque itération, pas pour traduire en code tous les modèles de conception définis durant l'élaboration
- Duré typique d'un cycle = 3 semaines
