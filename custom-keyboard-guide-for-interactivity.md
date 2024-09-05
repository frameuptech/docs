# Guide du Clavier Personnalisé pour l'Interactivité

## Table des matières
- Introduction
- Trouver les codes des touches pour votre appareil
- Personnalisation des raccourcis clavier pour les actions interactives

### Introduction
Si votre écran utilise un clavier pour une application interactive, vous pouvez vouloir remplacer ou étendre les raccourcis clavier pour les actions interactives. Cela peut être facilement fait en utilisant les Directives Avancées du Lecteur. Les claviers existent sous de nombreuses formes et saveurs, donc les remplacements de touches doivent être déclarés sous forme de code de touche.

### Trouver les codes des touches pour votre appareil
Pour trouver les codes des touches pour le clavier de votre choix, vous devez d'abord le connecter au lecteur, puis `ssh` vers le même lecteur. Ensuite, le code de touche pour toute touche spécifique peut être récupéré en utilisant l'utilitaire `evtest`.
L'exécution de `evtest` vous présentera initialement un choix de périphériques d'entrée :
    $ evtest
    Aucun périphérique spécifié, tentative de balayage de tout /dev/input/event*
    Périphériques disponibles :
    /dev/input/event0 : Clavier Filaire Dell KB216
    /dev/input/event1 : Contrôle Système du Clavier Filaire Dell KB216
    /dev/input/event2 : Contrôle Consommateur du Clavier Filaire Dell KB216
    Sélectionnez le numéro d'événement du périphérique [0-2] : 0
    La version du pilote d'entrée est 1.0.1
    L'ID du périphérique d'entrée : bus 0x3 fournisseur 0x413c produit 0x2113 version 0x111
    Nom du périphérique d'entrée : "Clavier Filaire Dell KB216"
Après sélection, le périphérique d'entrée, qui dans notre cas est le périphérique `0`, l'utilitaire affiche quelques informations de base sur le clavier et attend une entrée.
    Sélectionnez le numéro d'événement du périphérique [0-2] : 0
    La version du pilote d'entrée est 1.0.1
    L'ID du périphérique d'entrée : bus 0x3 fournisseur 0x413c produit 0x2113 version 0x111
    Nom du périphérique d'entrée : "Clavier Filaire Dell KB216"
    Événements pris en charge : 
    Type d'événement 0 (EV_SYN) 
    Type d'événement 1 (EV_KEY) 
    Code d'événement 1 (KEY_ESC)
    Code d'événement 2 (KEY_1) 
    Code d'événement 3 (KEY_2) 
    Code d'événement 4 (KEY_3) 
    (plus de codes d'événements...) 
    Propriétés :
    Test en cours ... (interrompre pour quitter)
En appuyant sur n'importe quelle touche souhaitée, le programme répond avec des informations détaillées sur l'événement, y compris le code de la touche. Par exemple, en appuyant sur la touche `espace`, la réponse suivante est obtenue :
    Événement : heure 1694082009.896384, type 4 (EV_MSC), code 4 (MSC_SCAN), valeur 7002c
    Événement : heure 1694082009.896384, type 1 (EV_KEY), code 57 (KEY_SPACE), valeur 1
    Événement : heure 1694082009.896384, -------------- SYN_REPORT ------------
L'événement `EV_KEY` contient les informations souhaitées, car la touche `KEY_SPACE` correspond au code de touche `57`.

### Personnalisation des raccourcis clavier pour les actions interactives
Actuellement, les actions prises en charge pour être personnalisées sont `enter` et `exit`, qui par défaut sont `espace` et `esc` respectivement.
Vous pouvez configurer cela sous les Directives Avancées du Lecteur (Configuration de l'écran → Avancé → Personnalisation → Directives Avancées du Lecteur) en utilisant une directive de ce type :
    custom_keyboard_configuration={"enter": [30, 31], "exit": [37, 38]}
Dans cet exemple, les touches `enter` implémentent l'action A(30) et S(31), et les touches `exit` implémentent l'action K(37), L(38).
