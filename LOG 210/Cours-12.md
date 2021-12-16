# Cours 12

# Notes de cours

## Présences des GRASP dans les pattenrs GoF.

Chaque principe GRASP est défini avec un énoncé d'un problème de conception et une solution pour le résoudre

Pour mieux comprendre l'application des patterns GoF, on doit imaginer la situation du logiciel avant l'application du pattern

Dans une situation ou l'on voudrait ajouter des morceaux, on entrainerait du code ilisible (moins compréhensible)

Exemple :
On peut voir le pattron Adaptateur comme une spécialisation des principes GRASP :

- Polymorphisme
- Indirection
- Fabrication Pure
- Faible Couplage
- Forte Cohésion
- Protection des variations

## Identifier les GRASP dans les GoF

pour les identifier, on rappelle la définition de chaque principe GRASP et on essaie d'imaginer le problème qui pourrait exister et comment le principe ( et le pattern GoF) résout le problème.

### Polymorphisme

p : qui est responsable quand le com portement varie selon le type
s : lorsqu'un comportement varie selon le type, affectez la responsabilité de ce comportement, avec des opérations polymorphes, aux types pour lesquels le comportement varie

Le comportement qui varie est la manière d'adapter les méthodes utilisées par le calculateur de taxes. La responsabilité est affectée au type interface

### Fabrication pure

p: En cas de situation désespérée, que faire quand vous ne voulez pas transgresser les principes de faible couplage et de fore cohésion
s: affectez un ensemble très cohésif de responsabilités à une classe comportementale artificielle qui ne représente pas un concept du domaine - une entité fabriquée pour augmenter la cohésion, diminuer le couplage et faciliter la réutilisation

### Indirection

p: comment affecter les responsabilités aux objets, sous-sytèmes et systèmes de sorte que les variations ou l'instabilité de ces éléments n'aient pas d'impact négatif sur les autres
s: identifiez les points de variation ou d'instabilité prévisibles et affectez les responsabilités afin de créer une interface stable autour d'eux

## GRASP et réusinage

il y a des liens entre les GRASP et les activités de réusinage

- Grasp polymorphisme est relié a replace type code with subclasses ...
- Grasp Frabication pure est relié à Extract class
- Grasp indirection est relié à extract function et move function

# Quiz
