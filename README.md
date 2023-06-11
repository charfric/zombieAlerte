# Alerter face à une menace zombie
## Tables des matières
1. [Introduction](#introduction)
2. [Module de transmission](#module-de-transmission)
3. [Module GPS](#module-gps)
4. [PCB et intégration](#pcb-et-intégration)
5. [Guide d'utilisation](#guide-dutilisation)
6. [Conclusion](#conclusion)

## Introduction
***
Pendant 40 heures, nous avons été enfermés dans le laboratoire d'électronique de l'ENSEA car l'école était assiégée par une horde de zombies mutants. Notre équipe était chargée de communiquer avec l'extérieur et d'alerter les potentiels survivants de notre présence dans l'école. 

Plusieurs moyens de communication étaient envisageables comme un signal lumineux ou un haut-parleur mais nous avons choisi de transmettre notre position par radio FM. 

Notre équipe:
* Charlotte Fricot: Cheffe de projet
* Laël Bitaud Canoën: Responsable intégration
* Hugo Devaux: Responsable software
* Issa Abdelhafiz: Responsable software
* Mamour Sarr: Responsable hardware


![image](https://github.com/charfric/zombieAlerte/assets/131167268/99f67354-4a6b-4ab1-90fe-083f3215a94f)

Le diagramme de Gantt est un outil qui nous a permit de savoir quand et par qui les tâches étaient effectuées. 


![image](https://github.com/charfric/zombieAlerte/assets/131167268/bb358cb1-8307-4a8a-9511-236f46ea0c3f)

Le système est alimenté par une pile 9V.
Le module de transmission et l'écran OLED sont connectés au microcontroleur STM32 H7A3 par I2C et le module GPS par UART. 

## Module de transmission
***

Le module est équipé du Si4713-B30 de Silicon Labs, un émetteur qui fonctionne dans la gamme de fréquences de 76 MHz à 108 MHz. Nous l'avons également équipé d'une antenne.

## Module GPS
***

Fonctionne par triangulation 
Détection de 3 satellites 
Utilisation de l'écran LCD pour visualiser les coordonnées

## PCB et intégration
***
![image](https://github.com/charfric/zombieAlerte/assets/131167268/e4ee2714-3d4f-49ac-8e07-b9a54489b3b3)

Pour concevoir le PCB de notre projet, nous avons utilisé le logiciel Kicad. 

Pour l'écran, le module GPS et l'alimentation, nous avons placé 3 connecteurs. 

![image](https://github.com/charfric/zombieAlerte/assets/131167268/9ea12099-3afa-4211-b86a-64b5ce62e172)
 

écran Oled + GPS + transmetteur 


## Guide d'utilisation
***
1. Mettre l'alimentation et l'interrupteur sur ON 
2. Appuyer sur le bouton bleu de la STM32 (bouton reset)
3. Attendre quelques instants que la latitude et la longitude apparaissent sur l'écran (de préférence à l'extérieur)
4. Utiliser le micro brancher sur le module de transmission pour communiquer la position

## Conclusion
***
Même si nous avons pris du retard à cause de quelques difficultés avec le module radio et dans la conception du PCB, nous avons réussi à atteindre les objectifs que nous nous étions fixés, c'est-à-dire concevoir un système capable de transmettre une position par radio FM. 

Nous pouvons noter plusieurs axes d'améliorations comme par exemple utiliser du morse pour communiquer la positionou bien utiliser un amplificateur pour émettre sur une plus grande distance. 
