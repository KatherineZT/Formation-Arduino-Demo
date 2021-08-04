# Démonstration pour Formation "Programmation et Prototypage avec Arduino"

Méthodologie
- Trouver le matériel à utiliser
- S'assurer d'avoir les composants nécessaires pour joindre le matériel ensemble
- Chercher des fiches techniques, des librairies, des tutoriels (ou voir la présentation de la formation, en format PDF)
- Bâtir un fichier de code C++

### Situation
Nous voulons construire un robot qui sera capable de détecter des obstacles. Il sera doté d'un capteur de distance HC-SR04, et si un objet est détecté à proximité du robot, le robot doit arrêter. Les moteurs Tamiya du robot roulent à 40% de leur vitesse maximale tant et aussi longtemps que le robot ne détecte pas d'obstacle. Si le robot s'immobilise en face d'un obstacle, puis qu'on retire l'obstacle, le robot se remet à rouler.

Liste de matériel
- HC-SR04
- Twin-motor Tamiya gearbox (deux moteurs DC FA-130)
- Arduino Mega 2560

Matériel nécessaire en surplus
- 4 fils de jonction mâle-femelle
- Pont-en-H L298N

Justification de l'utilisation du L298N :
- voltage des moteurs : 1.5V recommandé (inférieur à 5V, mais le Arduino n'a qu'une sortie 5V et une sortie 3.3V)
- ampérage des moteurs : 2.1A (le Arduino aurait eu de la difficulté à la fournir, et le L298N est fait pour contrôler 2 moteurs DC)

#### Qu'est-ce qu'un pont-en-H (ou H-bridge)?
Un circuit simple qui permet de contrôler la direction et la vitesse d'un moteur.

### Pour faire rouler le code
Importez la librairie L298N pour Arduino dans le Arduino IDE, puis ouvrez le fichier `.ino`. Compilez le code pour vous assurer que la librairie est trouvée, puis programmez votre Arduino.

### Branchements
(insérer image ici)
