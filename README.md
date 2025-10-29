# S88-N_decoder_arduino-based
Here is my version of the S88-N decoder. 
It uses an Arduino Nano and allows you to use it for block detection according to the Märklin principle or for potential-free electrical contacts. 16 inputs are available.

You can see typical connection examples in the **S88_bricolage.pdf** file.
For block detection, optocouplers are used (see **IN_9** with **JP5 NOT CONNECTED**). Depending on the number of inputs used, you can choose the **LTV814, 824, or 844** models (1, 2 and 4 optocoupler per package, respectively).
For switch detection, you don't need optocouplers (see **S2**, with **JP6 connected**), except if you want to have a galvanic isolation (see **S1**). Without an optocoupler, it is necessary to solder a shunt by following the dotted lines on the PCB.

The arduino sketch is in the **S88_UNO.zip** archive. It comes from Locoduino at https://www.locoduino.org/spip.php?article138
For this sketch, you'll need **UNO_S88** library, available in the **UNO_S88.zip** archive.

===

Français
# Décodeur S88-N basé sur Arduino
Voici ma version du décodeur S88-N.
Il utilise un Arduino Nano et permet, au choix, la détection de cantons selon le principe Märklin ou de contacts électriques libres de potentiel. 16 entrées sont disponibles.

Vous trouverez des exemples de branchement typiques dans le fichier **S88_bricolage.pdf**.
Pour la détection de cantons, des optocoupleurs sont utilisés (voir **IN_9** avec **JP5 NON CONNECTÉ**). Selon le nombre d'entrées utilisées, vous pouvez choisir les modèles **LTV814, 824 ou 844** (1, 2 ou 4 optocoupleur par boîtier).
Pour la détection d'aiguillages, les optocoupleurs ne sont pas nécessaires (voir **S2**, avec **JP6 connecté**), sauf si vous souhaitez une isolation galvanique (voir **S1**). Sans optocoupleur, il est nécessaire de souder un shunt en suivant les pointillés sur le PCB.

Le programme Arduino se trouve dans l'archive **S88_UNO.zip**. Il provient de Locoduino : https://www.locoduino.org/spip.php?article138
Pour ce programme, vous aurez besoin de la bibliothèque **UNO_S88**, disponible dans l'archive **UNO_S88.zip**.
