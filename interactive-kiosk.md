# Kiosque Interactif

## Table des matières
- Introduction
- Création d'une Application de Kiosque Interactif
- Paramètres de l'Application
- Indicateur Interactif
- Options Avancées uniquement pour Raspberry Pi
- Informations Supplémentaires

### Introduction
Le Kiosque Interactif permet à votre contenu d'être affiché comme un économiseur d'écran, et du contenu supplémentaire sera affiché après une interaction avec l'écran, soit par un toucher, soit par un clic de clavier. Après une période d'inactivité sélectionnée, l'écran revient au contenu de l'économiseur d'écran.

### Création d'une Application de Kiosque Interactif
Le Kiosque Interactif se trouve dans la catégorie Générale de votre galerie d'applications. Cliquez simplement dessus, puis sélectionnez "Utiliser l'Application" pour commencer la configuration.

### Paramètres de l'Application
**Nom & Description :** Un **Nom** est requis pour l'application et une **Description** optionnelle pour celle-ci.
**Contenu de Lecture :** Choisissez le contenu qui servira d'économiseur d'écran pour votre kiosque.
> **Limitation du lecteur Raspberry Pi**
> 
> Les playlists contenant des dispositions ne sont pas prises en charge comme contenu de lecture.
**Contenu d'Interaction :** Choisissez le contenu qui sera affiché lors de l'interaction de l'utilisateur.
> Les playlists ne sont pas prises en charge comme contenu d'interaction.
**Délai d'inactivité :** Définissez la durée d'inactivité, après laquelle le kiosque reviendra à l'affichage du contenu de l'économiseur d'écran.
> Certains médias comme les vidéos, les audios, les documents et les PDF, et les applications telles que Google Slide ont leur propre durée de lecture ou de visualisation définie. Lorsque vous utilisez ces éléments comme contenu d'interaction, le kiosque restera en contenu interactif **pendant toute la durée du média**, ce qui **outrepasse le délai d'inactivité**. Essentiellement, le temps pendant lequel les utilisateurs peuvent interagir avec le contenu est déterminé par la durée du média lui-même.
**Bouton de fermeture :** Le bouton de fermeture est toujours en haut de votre contenu d'interaction. En appuyant dessus, les utilisateurs peuvent passer du contenu d'interaction au contenu de lecture. Dans ce paramètre, vous pouvez choisir la couleur qui convient le mieux à votre contenu d'interaction.

### Indicateur Interactif
- **Basculer l'Indicateur Interactif :** Activer ce basculeur activera l'Indicateur Interactif, une invite visuelle pour encourager l'interaction de l'utilisateur avec le kiosque.
- **Indicateur :** Dans ce champ, vous pouvez sélectionner l'Indicateur Interactif de votre choix.
    - 💡_L'Indicateur Interactif clignotera à un rythme prédéfini._
- **Couleur de l'Indicateur :** Sélectionnez la couleur de l'Indicateur Interactif pour correspondre à vos préférences de conception ou aux directives de votre marque.
- **Taille de l'Indicateur :** Ajustez la taille de l'Indicateur Interactif, les tailles étant des pourcentages de votre écran, pour garantir qu'il soit suffisamment visible.
- **Emplacement de l'Indicateur :** Sélectionnez l'emplacement souhaité pour l'Indicateur Interactif sur votre écran pour garantir sa visibilité et sa commodité pour l'interaction de l'utilisateur.

### Options Avancées uniquement pour Raspberry Pi
- Collez l'URL exacte de votre navigateur, par exemple, ‘_https://example.com/forms/success_‘. En atteignant cette URL, les utilisateurs seront redirigés vers le contenu de lecture.
    - Un exemple pratique serait l'URL d'une page de ‘Merci’ après avoir soumis un formulaire.
- Fonctions du clavier : Connectez un clavier pour accéder aux fonctions de touches suivantes :
    - **Entrée :** Passer du contenu de lecture au contenu d'interaction.
    - **Échap :** Passer du contenu d'interaction au contenu de lecture.
> **Disposition du clavier**
> 
> Vous pouvez configurer ces fonctions de touches pour correspondre à la disposition de votre clavier. Pour obtenir des conseils sur la modification de ces touches, veuillez consulter notre guide du clavier.

### Informations Supplémentaires
- Le **Kiosque Interactif doit avoir une connexion Internet** pour afficher des pages web et d'autres médias en ligne.
    - Avec une connexion Internet à faible vitesse, les utilisateurs peuvent rencontrer des décalages intermittents lors de la transition entre le contenu de lecture et le contenu d'interaction.
- Un Kiosque Interactif peut être directement attribué à un écran ou à un horaire ; **l'ajouter à une playlist ou à une disposition n'est pas possible.**
- Si un utilisateur a activé **l'alerte météo NWS** :
    - Les alertes seront visibles dans le kiosque.
    - Les alertes apparaissent au-dessus du contenu de lecture et du contenu interactif.
- **Horaires de volume** :
    - Remplacent le contenu du Kiosque Interactif.
- **Alertes d'urgence** :
    - Remplacent le contenu du Kiosque Interactif.
