# Créer un mur vidéo

## Table des matières

- [Équipement requis](#équipement-requis)
- [Connexion de tout](#connexion-de-tout)
- [S'assurer que tout fonctionne correctement](#s'assurer-que-tout-fonctionne-correctement)
- [Étapes dans le compte](#étapes-dans-le-compte)
- [Quelques mots sur la compensation des bords](#quelques-mots-sur-la-compensation-des-bords)
- [Configurations en matrice (NxN), sans bords](#configurations-en-matrice-nxn-sans-bords)
- [Configurations en mosaïque (NxM), sans bords](#configurations-en-mosaïque-nxm-sans-bords)
- [Mesurer pour toutes les configurations, y compris les murs vidéo asymétriques, bords inclus](#mesurer-pour-toutes-les-configurations-y-compris-les-murs-vidéo-asymétriques-bords-inclus)
- [Dépannage](#dépannage)
    - [La lecture vidéo ne démarre pas sur le mur vidéo, mais je peux la voir fonctionner sur le lecteur "Maître".](#la-lecture-vidéo-ne-démarre-pas-sur-le-mur-vidéo-mais-je-peux-la-voir-fonctionner-sur-le-lecteur-maître)
    - [La lecture vidéo n'est pas fluide. Il y a des saccades et des glitches.](#la-lecture-vidéo-n'est-pas-fluide-il-y-a-des-saccades-et-des-glitches)
    - [La vidéo semble de mauvaise qualité.](#la-vidéo-semble-de-mauvaise-qualité)
    - [Les écrans du mur vidéo ne sont pas synchronisés à 100%.](#les-écrans-du-mur-vidéo-ne-sont-pas-synchronisés-à-100)
- [Configuration de l'unité émettrice LKV373A](#configuration-de-l'unité-émettrice-lkv373a)

**Important - LKV373A**
Le guide suivant utilise comme exemple un streamer IP vers HDMI qui est le Lenkeng LKV373A (uniquement l'émetteur). Ce matériel n'est plus disponible et sera bientôt en fin de vie. **Veuillez ne pas acheter le LKV373A V-4.0, il ne fonctionnera pas**. Vous pouvez continuer avec ce guide et remplacer le LKV373A par **tout autre streamer IP vers HDMI** que vous trouverez.

Vous pouvez créer une configuration de mur vidéo de signalisation numérique vraiment abordable en utilisant des lecteurs. Vous devez configurer manuellement chacun de vos écrans. Pour ce faire, pour des murs vidéo simples en matrice, comme 2x2 ou 3x3, c'est vraiment facile. Pour une configuration plus élaborée, vous devez faire les calculs (ou nous demander de l'aide ; nous serons ravis de vous aider). Mais vous pouvez créer des murs vidéo vraiment impressionnants.

## Équipement requis

Pour créer la configuration, vous aurez besoin de l'équipement suivant :
1. **Un lecteur pour chaque écran** qui fera partie du mur vidéo.
2. **Un streamer vidéo HDMI vers IP**. Nous recommandons le [Lenkeng LKV373A](https://www.lenkeng.com/p_detail/87/type/type1) (uniquement l'émetteur), qui coûte environ 35 $ sur eBay. D'autres appareils fonctionneront probablement aussi. Vérifiez les spécifications requises pour les streamers vidéo IP.
3. **Un routeur réseau** avec des ports LAN et WAN. Cela empêche le flux vidéo multicast d'inonder le reste de votre réseau local.
4. **Un commutateur réseau Ethernet** pour connecter tout ce qui précède. Tout commutateur simple fera l'affaire, mais il doit fournir au moins N+3 ports pour un mur vidéo N-écran.
5. **Un lecteur "maître"**, lisant le contenu pour le mur vidéo. Cela pourrait également être n'importe quel appareil avec une sortie HDMI, par exemple, un décodeur, un récepteur satellite, un lecteur DVD ou un autre lecteur multimédia.

Concernant les écrans du mur vidéo, nous recommandons d'utiliser des écrans similaires du même fournisseur. Différentes marques d'écrans peuvent avoir des niveaux de luminosité différents. Testez les écrans côte à côte avant de les monter pour voir si leurs niveaux de luminosité peuvent être ajustés.

## Connexion de tout

1. Assurez-vous que tout est débranché de l'alimentation.
2. Connectez le port WAN du routeur à votre réseau Internet local.
3. Connectez le port LAN du routeur au commutateur réseau du mur vidéo.
4. Connectez tous les lecteurs au commutateur réseau.
5. Connectez le port Ethernet du streamer IP au commutateur réseau.
6. Connectez l'entrée HDMI du streamer IP à la sortie HDMI du lecteur "maître" (ou de tout autre appareil HDMI que vous utilisez).
7. Branchez l'alimentation du routeur en premier et attendez 2 minutes pour qu'il démarre. Ensuite, allumez le commutateur Ethernet, le streamer IP et le reste des appareils.

Voici un diagramme avec un aperçu des connexions et des étapes :

## S'assurer que tout fonctionne correctement

Après avoir tout connecté comme ci-dessus, vous devez enregistrer votre lecteur si vous ne l'avez pas déjà fait.

Ensuite, nous devons nous assurer que les écrans ne font pas de surbalayage. Téléchargez cette image de carte de test (cliquez et sélectionnez l'icône "Télécharger" dans le coin supérieur droit) et téléchargez-la sur votre compte :
Mettez-la dans une mise en page et assignez cette mise en page à tous les écrans du mur vidéo. Ensuite, vérifiez soigneusement tous les coins des écrans pour tout surbalayage.
Voici ce que vous devriez normalement voir dans les 4 coins de chaque écran :
Et voici à quoi ressemble un écran faisant du surbalayage :
Le surbalayage interférera avec les alignements du mur vidéo, vous devez donc le supprimer. Utilisez le menu de la TV pour ajuster les paramètres d'image et changez les options généralement référencées comme "P.SIZE", "Aspect Ratio", "Format" ou similaire. Ces paramètres devraient avoir des options comme "16:9", "4:3", "Widescreen", "Pixel Scan", etc. Parcourez les options pour trouver celle qui élimine le surbalayage.
Ensuite, nous devons nous assurer que les lecteurs sont configurés avec la bonne orientation. Si un écran du mur vidéo est monté verticalement comme un portrait ou à l'envers, vous devez le définir dans la configuration du lecteur respectif dans votre compte. Les écrans devraient alors se reconfigurer et apparaître tournés après quelques minutes.

## Étapes dans le compte

Voici les étapes à suivre pour configurer un mur vidéo dans votre compte.

1. **Créer 1 entrée vidéo en streaming pour chaque écran.**
    1. Allez dans la section "Vidéos". Cliquez sur "Ajouter une vidéo".
    2. Dans la fenêtre contextuelle qui apparaît, sélectionnez "Flux vidéo".
    3. Dans le champ d'adresse du flux vidéo, vous devez ajouter l'adresse du flux multicast. Pour LKV373A, vous devez taper "udp://239.255.42.42:5004" (sans les guillemets). Pour d'autres streamers IP, **utilisez l'adresse multicast et le port appropriés**. Une fois terminé, cliquez sur "Créer".
    4. Saisissez un nom, par exemple "Flux TV 1".
    5. Désactivez l'option "Mise en mémoire tampon".
    6. Activez le bouton "Recadrer la vidéo".
    7. Remplissez le recadrage requis pour chaque écran pour afficher uniquement la partie requise du flux. Initialement, vous pouvez laisser les 4 champs à 0% pour tester. Lisez le reste du guide ci-dessous pour plus de détails.
    8. Cliquez sur "Enregistrer".
    9. Répétez ce processus de création de flux vidéo pour chaque écran de votre mur vidéo.

2. **Créer 1 mise en page pour chaque écran.**
    1. Allez dans la section "Mises en page" et cliquez sur "Ajouter une mise en page".
    2. Saisissez un nom, par exemple "Mise en page TV 1".
    3. Si votre écran est monté en portrait, cliquez sur l'icône "+" pour ajouter la mise en page portrait 16:9 et supprimez la mise en page paysage 16:9.
    4. Cliquez sur "Média". Dans la fenêtre contextuelle qui apparaît, sélectionnez le flux respectif que vous avez créé précédemment, par exemple "Flux TV 1", sélectionnez l'option d'ajustement comme "Étendre" et cliquez sur "OK".
    5. Redimensionnez le média ajouté dans l'éditeur de mise en page pour occuper toute la zone de l'écran.
    6. Cliquez sur "Enregistrer".
    7. Répétez ce processus de création de mise en page pour chaque écran de votre mur vidéo.

3. **Assignez les mises en page à chaque écran** en tant que mise en page par défaut. Assurez-vous de supprimer temporairement toute planification pour tester. Plus tard, vous pourrez faire de la planification si vous le souhaitez.

4. **Assignez du contenu au lecteur "maître"** en utilisant une mise en page contenant une vidéo. Assurez-vous que la vidéo a une piste audio. Cela est important pour éviter les problèmes lors des tests.

5. **Cliquez sur le bouton "Pousser vers les lecteurs".**

Il y a une petite limitation lors de l'utilisation de LKV. L'entrée de LKV doit avoir du son ; sinon, le lecteur ne peut pas lire le flux. C'est le comportement par défaut du matériel LKV.

Si le média assigné à votre lecteur maître **n'a pas de son**, par exemple une image, vous devez **mettre en sourdine TOUS** les lecteurs esclaves (à partir des paramètres de l'écran dans l'onglet Son/Affichage) pour surmonter la limitation de LKV.

Après cela, vous devriez avoir tous les écrans du mur vidéo lisant le contenu que vous avez assigné au lecteur "maître".
La lecture devrait être 100% synchronisée. Si ce n'est pas le cas, assurez-vous d'avoir les mêmes paramètres sur tous les écrans. Certaines unités TV ont un traitement d'image pour améliorer l'image, ce qui induit un délai pendant la lecture. Vous devriez soit désactiver cela sur tous les écrans (recommandé), soit l'activer sur toutes les TV (seulement si elles sont du même modèle et de la même taille).

## Quelques mots sur la compensation des bords

Les écrans ont des bords. C'est le cadre en plastique autour de l'écran. Vous pouvez configurer votre mur vidéo avec ou sans tenir compte des bords entre les écrans.
Voici la différence visuellement :
Vous décidez comment vous voulez que le contenu apparaisse, et cela vous donne la flexibilité de faire les deux.

## Configurations en matrice (NxN), sans bords

Les configurations simples pour les murs vidéo en matrice (2x2, 3x3) sont faciles, surtout si vous ne tenez pas compte de la compensation des bords. Par exemple, pour un mur vidéo 2x2, vous devez spécifier :
- Recadrage du flux pour le coin supérieur gauche : Haut : 0%, Bas : 50%, Gauche : 0%, Droite : 50%
- Recadrage du flux pour le coin supérieur droit : Haut : 0%, Bas : 50%, Gauche : 50%, Droite : 0%
- Recadrage du flux pour le coin inférieur gauche : Haut : 50%, Bas : 0%, Gauche : 0%, Droite : 50%
- Recadrage du flux pour le coin inférieur droit : Haut : 50%, Bas : 0%, Gauche : 50%, Droite : 0%

Voici un diagramme.
Voici la même chose pour un mur vidéo 3x3.
Pour tout mur vidéo NxN, divisez 100% par N et définissez chaque pourcentage de recadrage de flux en conséquence.

## Configurations en mosaïque (NxM), sans bords

Par "mosaïque", nous entendons des configurations en matrice qui ne sont pas NxN, par exemple une configuration en "ruban" 3x1 :
Les pourcentages sont calculés de la même manière que si le mur vidéo était une configuration NxN, y compris les écrans manquants. Vous devez placer votre contenu dans la bonne zone de l'éditeur de mise en page, car le reste ne sera pas affiché.

## Mesurer pour toutes les configurations, y compris les murs vidéo asymétriques, bords inclus

Vous pouvez configurer n'importe quel mur vidéo, même si les écrans sont montés en orientation paysage ou portrait. Vous pouvez donc créer des murs vidéo comme celui-ci :
Si vous voulez faire de la compensation des bords ou configurer un mur vidéo asymétrique, vous devez mesurer les distances réelles entre les zones visibles des écrans. Utilisez la carte de test ci-dessus et assurez-vous qu'elle couvre toute la zone des écrans. Donc, dans le cas général d'un mur vidéo asymétrique, vous devriez avoir quelque chose comme ceci pour faire les mesures.
Rappelez-vous : la carte de test doit couvrir toute la zone de l'écran. Apportez les modifications nécessaires pour obtenir un résultat similaire à celui ci-dessus.
La carte de test a une ligne blanche sur les bords de la zone visible de l'écran. Utilisez cela pour faire vos mesures.

Une note fondamentale : Assurez-vous que ces mesures sont aussi précises que possible, sinon vous risquez un mauvais alignement et devrez les répéter. Mesurez en millimètres, ou utilisez des 1/16 ou 1/32 de pouce. Vous devez être aussi précis que possible.

Pour chaque écran :
Mesurez la distance entre la ligne blanche du bord supérieur de l'écran le plus haut et la ligne blanche du bord supérieur de l'écran. Appelons cela **ÉCRAN_HAUT**.
Par exemple, la ligne blanche du bord supérieur de l'écran le plus haut (**TV3**) jusqu'à la ligne blanche du bord supérieur de chaque écran.
Mesurez la distance entre la ligne blanche du bord gauche de l'écran le plus à gauche et la ligne blanche du bord gauche de l'écran. Appelons cela **ÉCRAN_GAUCHE**.
Par exemple, la ligne blanche du bord gauche de l'écran le plus à gauche (**TV1**) jusqu'à la ligne blanche du bord gauche de chaque écran.
Mesurez la distance entre la ligne blanche du bord gauche de l'écran et la ligne blanche du bord droit. Appelons cela **ÉCRAN_LARGEUR**.
Mesurez la distance entre la ligne blanche du bord supérieur de l'écran et la ligne blanche du bord inférieur. Appelons cela **ÉCRAN_HAUTEUR**.

1. **[Téléchargez ou copiez cette feuille de calcul Google](https://docs.google.com/spreadsheets/d/1qUzama0Oi9M52wDo8lUVEDPuyItTrI1sMbUeIOssyAM/edit?usp=sharing).**
2. Entrez les chiffres ci-dessus, elle fera les calculs pour vous. Ensuite, passez à l'étape finale ci-dessous.
3. Allez dans votre portail de compte et faites ce qui suit pour chaque flux vidéo correspondant à chaque écran :
    1. Définissez le pourcentage de recadrage "Haut" comme calculé par la feuille de calcul.
    2. Définissez le pourcentage de recadrage "Gauche" comme calculé par la feuille de calcul.
    3. Définissez le pourcentage de recadrage "Bas" comme calculé par la feuille de calcul.
    4. Définissez le pourcentage de recadrage "Droit" comme calculé par la feuille de calcul.

Le résultat final serait quelque chose comme ceci :
Si vous avez besoin d'aide pour faire les calculs, contactez notre équipe de support et nous vous aiderons.
