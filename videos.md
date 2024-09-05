# Vidéos

## Table des matières

- [Formats pris en charge](#formats-pris-en-charge)
- [Ajouter une vidéo](#ajouter-une-vidéo)
- [Ajouter un fichier vidéo avec l'option glisser-déposer](#ajouter-un-fichier-vidéo-avec-loption-glisser-déposer)
- [Options avancées pour les vidéos](#options-avancées-pour-les-vidéos)
- [Gérer les fichiers vidéo](#gérer-les-fichiers-vidéo)
- [Paramètres de contrôle supplémentaires](#paramètres-de-contrôle-supplémentaires)

Dans la section Vidéos, vous pouvez télécharger et gérer une grande variété de formats vidéo. Les vidéos que vous téléchargez sont automatiquement converties en formats standard de l'industrie (H.264 avec audio AAC).

## Formats pris en charge

1. **Vidéos YouTube** sont prises en charge dès la sortie de la boîte, elles sont donc téléchargées dans la meilleure qualité possible (jusqu'à 1080p maintenant).
2. **Vidéos en streaming en direct** (YouTube, UStream ou flux HLS ou RTMP/RTSP personnalisés). Ceux-ci doivent être livrés par le flux en format H.264 pour garantir qu'ils seront lus sur les lecteurs.
3. **Fichiers PowerPoint** sont convertis en vidéos sur nos serveurs, conservant toutes les transitions et animations.

## Ajouter une vidéo

Pour ajouter un seul fichier vidéo, cliquez sur le bouton "Ajouter une vidéo/YouTube/PowerPoint" trouvé en bas de la liste des vidéos. Vous devez ensuite sélectionner le type de source vidéo. Vous pouvez choisir parmi les options suivantes :

- **Fichier vidéo** – Téléchargez une ou plusieurs vidéos depuis votre appareil, utilisez l'option Importer depuis une URL et entrez un lien vers un fichier vidéo. Le fichier sera copié sur votre compte.
- **Vidéo YouTube** – utilisez un lien vers une vidéo ou un flux YouTube que le lecteur téléchargera directement depuis YouTube et lira localement ou en streaming.
- **Vimeo** – utilisez un lien vers une vidéo ou un flux Vimeo, que le lecteur téléchargera directement depuis Vimeo et lira localement ou en streaming.
- **Fichier PPT** – Téléchargez des présentations PowerPoint depuis votre appareil. Les présentations sont converties en vidéos, conservant toutes les animations.
- **Flux vidéo** – utilisez un flux vidéo en direct depuis Internet ou une source locale, y compris UStream et les flux UDP/RTP/HLS.
- **Mur vidéo** – lisez nos instructions détaillées sur [comment configurer un mur vidéo](video-walls.md).
- **Entrée vidéo** – lisez nos instructions détaillées sur [comment configurer une entrée vidéo](how-to-setup-an-hdmi-video-feed-input-or-connect-a-usb-camera-video-input.md).
- **Vidéos gratuites** – recherchez des vidéos dans notre galerie vidéo en ligne et importez-les en quelques clics.

Après avoir fourni la source vidéo, vous devez également fournir les informations suivantes :

- saisir le **Nom** du fichier vidéo
- une **Description** optionnelle
- ajouter des **Tags** à la vidéo téléchargée
- cliquer sur **Enregistrer** pour enfin télécharger la vidéo

### Ignorer l'encodage vidéo
Lorsque vous téléchargez un fichier vidéo standard stocké localement sur votre PC, il y a une option pour télécharger le fichier exact pour la lecture et ignorer le processus d'encodage par défaut. Cette option est généralement recommandée uniquement pour les utilisateurs avancés, car la lecture du fichier vidéo original peut échouer. Activer cette option lors du téléchargement inhibera l'encodage, réduisant le temps nécessaire pour que la vidéo soit disponible et empêchant la création d'une vignette pour la vidéo.

## Ajouter un fichier vidéo avec l'option glisser-déposer

Vous avez la possibilité d'ajouter un fichier vidéo en faisant glisser le fichier spécifique ou les fichiers de votre PC directement dans votre bibliothèque vidéo, en sautant quelques étapes et en vous faisant gagner du temps supplémentaire.
L'option glisser-déposer est également disponible dans la vue en dossier.

## Options avancées pour les vidéos

Pour tous les types de sources vidéo, vous avez les options avancées suivantes :

- **Lire à partir de / Lire jusqu'à**
  - Dans les fonctionnalités avancées, vous pouvez définir les paramètres **Lire à partir de / Lire jusqu'à**. En d'autres termes, vous pouvez définir la date d'expiration, ce qui signifie que vous pouvez choisir la date et l'heure exactes auxquelles la vidéo sera affichée dans votre playlist/mise en page, ou vous pouvez la définir sur "Toujours" et "Pour toujours", et la vidéo n'expirera jamais.
- **Faire pivoter la vidéo**
  - Cette option vous permet de définir l'orientation correcte pour une vidéo. Cela concerne uniquement la vidéo spécifique. De cette façon, vous pouvez utiliser des vidéos qui ont été enregistrées avec la mauvaise orientation.
  - Donc, si vous avez une vidéo qui n'est pas affichée correctement, vous pouvez utiliser ce paramètre pour l'afficher correctement.
  - Gardez à l'esprit que ce paramètre n'affecte que la lecture et ne fait pas pivoter le fichier vidéo lui-même.
- **Recadrer la vidéo**
  - Cette option vous permet de définir les marges de recadrage pour une vidéo. Cela concerne uniquement la vidéo spécifique. Vous pouvez recadrer par pourcentage pour n'importe quel côté de la vidéo.
  - Par exemple, si vous définissez le recadrage "Droit" à 10%, 10% de la largeur de la vidéo sera recadrée pendant la lecture. Il en va de même pour tous les bords.
  - Gardez à l'esprit que ce paramètre n'affecte que la lecture et ne recadre pas le fichier vidéo lui-même.
- **Activer les sous-titres**
  - Tout d'abord, vous devez télécharger la vidéo sur votre compte, et la vidéo doit également avoir des sous-titres intégrés.
  - Les sous-titres intégrés sont stockés à l'intérieur du fichier vidéo (ou conteneur vidéo) en tant que flux – de la même manière que les flux vidéo et audio sont stockés à l'intérieur du fichier vidéo. Tous les formats de conteneurs vidéo ne peuvent pas avoir de sous-titres intégrés, et il y a des limitations quant aux formats de sous-titres pris en charge pour chaque format de conteneur vidéo.
  - Après cela, vous pouvez basculer le bouton "Activer les sous-titres" pour afficher les sous-titres sur votre écran.

### Remarque : Vidéos YouTube
Notez que les vidéos YouTube avec sous-titres ne peuvent pas être utilisées de cette manière. Vous devrez télécharger la vidéo YouTube et les sous-titres sur votre ordinateur, graver les sous-titres avec un programme relatif et les télécharger en tant que fichiers vidéo sur votre compte.

### Préparation des vidéos
Les sous-titres sont pris en charge uniquement pour les vidéos que vous téléchargez. Pour que cette solution fonctionne, vous devez vous assurer que les fichiers vidéo sont compatibles.
Vous devrez reconditionner le fichier vidéo et la piste de sous-titres en un seul fichier MKV. Assurez-vous que la piste de sous-titres est la première piste, car la vidéo ci-dessus ne lira que la première piste de sous-titres du fichier MKV. Vous avez deux options pour préparer le fichier MKV :

- Facile mais lent : Utilisez [Handbreak](https://handbrake.fr/), en ajoutant le fichier source vidéo et en ajoutant la piste de sous-titres.
- Difficile mais rapide : Si votre vidéo est déjà au format H.264, vous devez la reconditionner (pas la réencoder).
  - Utilisez FFmpeg comme ceci :
    ```
    ffmpeg -i video.mp4 -i subtitle.srt -c copy output.mkv
    ```
  - Après avoir préparé le fichier vidéo, vous aurez un seul fichier MKV, avec une piste vidéo encodée en H.264 et une piste de sous-titres.

### Télécharger des vidéos avec sous-titres

- Allez dans la section "Vidéos" et cliquez sur le bouton pour ajouter une nouvelle vidéo.
- Sélectionnez le fichier vidéo.
- Activez le bouton "Activer les sous-titres" et cliquez sur enregistrer.
- Assignez la vidéo à votre lecteur et poussez-la pour la lecture.
- Vous devriez maintenant pouvoir voir les sous-titres pour cette vidéo.

### Désactiver les sous-titres

- Pour désactiver les sous-titres, désactivez le bouton "Activer les sous-titres", enregistrez et poussez à nouveau.

## Gérer les fichiers vidéo

Dans la section Vidéos, vous pouvez voir une liste de tous les fichiers vidéo actuellement téléchargés dans votre compte. Les informations sur vos fichiers vidéo sont organisées dans les colonnes suivantes :

- le **Nom** de la vidéo ainsi qu'un **Aperçu** (vignette)
- le **Horodatage** (date et heure) de la dernière modification de la vidéo
- le **Espace de travail** (pour les comptes du plan **Entreprise**) auquel appartient la vidéo
- les **Tags** (pour les comptes des plans **Pro** et **Entreprise**) appliqués au fichier
- la colonne **Actions**

Si vous cliquez sur l'icône à trois points dans la colonne Actions, vous verrez une liste d'actions que vous pouvez appliquer à vos fichiers vidéo téléchargés.

- **Modifier**
  - Changez les détails d'une vidéo en cliquant sur le bouton "Modifier". Ici, vous pouvez également **remplacer** la vidéo réelle, et elle sera modifiée partout où elle est utilisée.
- **Dupliquer**
  - Créez une copie exacte du fichier vidéo avec un nouveau nom.
- **Déplacer**
  - Vous pouvez déplacer des vidéos vers des dossiers et/ou d'autres espaces de travail (pour les comptes du plan **Entreprise**).
- **Supprimer**
  - Supprimez le fichier vidéo.

## Paramètres de contrôle supplémentaires

- Dans le coin supérieur gauche, vous pouvez utiliser la boîte de recherche pour trier rapidement votre liste de vidéos. Vous pouvez rechercher en utilisant n'importe laquelle des quatre colonnes, c'est-à-dire par nom, date, espace de travail et tag.
- Vous pouvez sélectionner une ou plusieurs vidéos en cliquant sur la case carrée à gauche de leur vignette. Vous pouvez ensuite cliquer sur le bouton **Actions** en bas pour Modifier, Déplacer, Supprimer toutes les vidéos sélectionnées en une seule fois.
- Dans le coin supérieur droit, vous pouvez cliquer sur le bouton "Ajouter un dossier" pour créer un dossier qui peut être utilisé pour regrouper des fichiers multimédias (le dossier sera global parmi les images, vidéos, audios, documents, pages Web et widgets). Vous pouvez également changer la liste et actualiser la vue.
