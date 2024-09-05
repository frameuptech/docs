# Comment configurer une entrée vidéo HDMI ou connecter une caméra USB (Entrée vidéo)

## Table des matières

- [Introduction](#introduction)
- [Matériel recommandé](#matériel-recommandé)
- [Connexion du matériel](#connexion-du-matériel)
- [Configuration d'une entrée vidéo](#configuration-dune-entrée-vidéo)
- [Dépannage d'une entrée vidéo](#dépannage-dune-entrée-vidéo)

## Introduction

Le lecteur étend vos options disponibles pour afficher du contenu sur vos écrans. L'option "Entrée vidéo" vous permet de connecter n'importe quel appareil d'entrée vidéo USB à vos lecteurs pour afficher un flux vidéo sur vos écrans. L'utilisation typique est un **port HDMI-in** ; vous connectez une carte de capture HDMI USB et vous connectez via HDMI à votre récepteur décodeur (satellite, câble ou terrestre) pour afficher la vidéo en direct avec votre messagerie dans une mise en page cool. Cela fonctionne également avec des caméras USB typiques (n'importe quelle webcam) si vous souhaitez relayer un flux en direct local.

Lecteur basé sur **Raspberry Pi**
⚠️ Cette fonctionnalité est disponible **uniquement** pour les lecteurs basés sur Raspberry Pi. Cette fonctionnalité n'est pas disponible pour d'autres types de lecteurs et ne peut pas être utilisée du tout. Lisez plus à ce sujet.

## Matériel recommandé

[**Ici**](recommended-usb-devices.md) vous pouvez trouver des détails sur les cartes de capture HDMI USB que nous avons testées, qui peuvent être utilisées sur le lecteur comme un port HDMI-in.

## Connexion du matériel

Vous devez d'abord connecter la carte de capture HDMI USB (ou la webcam) directement au lecteur.
Vous pouvez utiliser n'importe lequel des quatre ports USB :

## Configuration d'une entrée vidéo

Pour utiliser l'entrée vidéo, procédez comme suit :

1. Allez dans la section "Vidéos" et cliquez sur le bouton "Ajouter une vidéo/YouTube/PowerPoint".
2. Parmi toutes les options qui apparaissent, sélectionnez "Entrée vidéo".
3. Dans le formulaire présenté, saisissez un nom et ajoutez tous les autres détails dont vous avez besoin, comme la description, les tags et la durée par défaut.
4. Par défaut, la **Résolution de capture** et les **FPS** sont automatiquement définis. Laissez ces paramètres par défaut lors de la première configuration.
5. Cliquez sur "Enregistrer" pour enregistrer et quitter la configuration.

Vous pouvez maintenant assigner ce flux d'entrée vidéo directement à votre lecteur pour vous assurer qu'il fonctionne comme prévu.

## Dépannage d'une entrée vidéo

1. **Je ne reçois aucune vidéo**
Certaines cartes de capture affichent un flux statique standard si rien n'est connecté à leur entrée, par exemple, un message d'erreur ou un écran coloré. Essayez de débrancher votre appareil HDMI (par exemple, votre décodeur) et voyez ce qui se passe. Si rien ne se passe, la carte de capture HDMI USB pourrait ne pas être correctement connectée ou ne pas fonctionner du tout.

2. **Je ne reçois aucun son**
Vérifiez que votre appareil HDMI (par exemple, votre décodeur) n'est pas en sourdine et que le volume est suffisamment élevé.

3. **Il y a un délai entre la vidéo d'entrée et son affichage à l'écran**
Un léger délai de moins d'une seconde est attendu. Un délai plus élevé peut être dû à la carte de capture HDMI spécifique que vous utilisez.
