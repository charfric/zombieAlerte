# Alerter face à une menace zombie
## Tables des matières
1. [Introduction](#introduction)
2. [Module de transmission](#module-de-transmission)
3. [Module GPS](#module-gps)
4. [PCB et Intégration](#pcb-et-integration)
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

Le module est équipé du Si4713-B30 de Silicon Labs, un émetteur qui fonctionne dans la gamme de fréquences de 76 MHz à 108 MHz. Nous l'avons également équipé d'une antenne
![image](https://github.com/charfric/zombieAlerte/assets/131167268/9993d75a-634f-43ab-b8bc-04a138126301)

## Module GPS
***

![image](https://github.com/charfric/zombieAlerte/assets/131167268/ba7b957d-3ee0-41a8-8051-10d28480dd1a)

Fonctionne par triangulation 
Détection de 3 satellites 
Utilisation de l'écran LCD pour visualiser les coordonnées

## PCB et Intégration
***
![image](https://github.com/charfric/zombieAlerte/assets/131167268/e4ee2714-3d4f-49ac-8e07-b9a54489b3b3)
![image](https://github.com/charfric/zombieAlerte/assets/131167268/9ea12099-3afa-4211-b86a-64b5ce62e172)
 

écran Oled + GPS + transmetteur 

![image](https://github.com/charfric/zombieAlerte/assets/131167268/b2ab9a4a-b8d5-45fa-809a-c1bc75e7e64b)


## Conclusion
***
Maltré le retard que nous avons pris dans la conception du PCB et ... nous avons réussi a atteindre les objectifs que l'on s'étaient fixés, c'est-à-dire concevoir un système capable de transmettre une position par radio FM. 
