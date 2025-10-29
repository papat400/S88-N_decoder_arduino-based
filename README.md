# English
## S88-N_decoder_arduino-based
Here is my version of the S88-N decoder. 
It uses an Arduino Nano and allows you to use it for block detection according to the Märklin principle or for potential-free electrical contacts. 16 inputs are available.

You can see typical connection examples in the **S88_bricolage.pdf** file.

* For block detection, optocouplers are used (see **IN_9** with **JP5 NOT CONNECTED**). Depending on the number of inputs used, you can choose the **LTV814, 824, or 844** models (1, 2 and 4 optocoupler per package, respectively).

* For electrical switch (ptoentiel-free) detection, you don't need optocouplers (see **S2**, with **JP6 connected**), except if you want to have a galvanic isolation (see **S1**). Without an optocoupler, it is necessary to solder a shunt by following the dotted lines on the PCB.

The arduino sketch is in the **S88_UNO.zip** archive. It comes from Locoduino at https://www.locoduino.org/spip.php?article138

Inputs/outputs used by the S88 bus on the Nano:
- S88 Clock: pin = 2
- S88 PS: pin = 3
- Data Input coming from the previous Arduino in the S88 chain: pin = 0
- Data output to go to the next Arduino in the S88 chain or to the control unit: pin = 1
- **There is no RESET input**
- The S88 bus inputs are set to INPUT_PULLUP

Digital inputs used for contacts:
- Inputs 4 to 11 for the 8-input option
- Inputs 4 to 13 + Outputs 0 to 5 (configured as digital inputs) for the 16-input option
- The digital inputs are set to INPUT_PULLUP

For this sketch, you'll need **UNO_S88** library, available in the **UNO_S88.zip** archive.

There are two versions of the PCB: one with screw terminals **S88_Nano_16R0C_2Layers**, the other with DuPont connectors **S88_Nano_16R0C_2Layers_DuPont**. Each person can choose whichever they prefer.
The PCBs were designed using Eagle 9.6.2 free.

---

# Français
## Décodeur S88-N basé sur Arduino
Voici ma version du décodeur S88-N.
Il utilise un Arduino Nano et permet, au choix, la détection de cantons selon le principe Märklin ou de contacts électriques libres de potentiel. 16 entrées sont disponibles.

Vous trouverez des exemples de branchement typiques dans le fichier **S88_bricolage.pdf**.

* Pour la détection de cantons, des optocoupleurs sont utilisés (voir **IN_9** avec **JP5 NON CONNECTÉ**). Selon le nombre d'entrées utilisées, vous pouvez choisir les modèles **LTV814, 824 ou 844** (1, 2 ou 4 optocoupleur par boîtier).

* Pour la détection de contact (libre de potentiel), les optocoupleurs ne sont pas nécessaires (voir **S2**, avec **JP6 connecté**), sauf si vous souhaitez une isolation galvanique (voir **S1**). Sans optocoupleur, il est nécessaire de souder un shunt en suivant les pointillés sur le PCB.

Le programme Arduino se trouve dans l'archive **S88_UNO.zip**. Il provient de Locoduino : https://www.locoduino.org/spip.php?article138

Entrées/sorties utilisées par le bus S88 :
- Clock S88 : pin = 2
- PS S88 : pin = 3
- Data Input venant de l'Arduino précédent dans la chaîne S88 : pin = 0
- Data output pour aller vers l'Arduino suivant dans la chaîne S88 ou vers la centrale : pin = 1
- **Il n'y a pas d'entrée RESET**
- Les entrées Bus S88 sont en INPUT_PULLUP 
        
Entrées TOR (Tout Ou Rien) utilisées pour les contacts :
- Entrées 4 à 11 pour l'option 8 entrées
- Entrée 4 à 13 + Sorties 0 à 5 (paramétrées en entrées TOR) pour l'option 16 entrées
- Les entrées TOR sont en INPUT_PULLUP

Pour ce programme, vous aurez besoin de la bibliothèque **UNO_S88**, disponible dans l'archive **UNO_S88.zip**.

Il y a deux versions de PCB : un avec des borniers à vis **S88_Nano_16R0C_2Layers**, l'autre avec des connecteurs DuPont **S88_Nano_16R0C_2Layers_DuPont**. A chacun de choisir ce qu'il préfère.
Les PCB ont été dessinés avec Eagle 9.6.2 free.
