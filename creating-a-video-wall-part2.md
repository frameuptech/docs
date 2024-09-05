## Dépannage

### La lecture vidéo ne démarre pas sur le mur vidéo, mais je peux la voir fonctionner sur le lecteur "Maître".

Pour démarrer la lecture pour les autres lecteurs, vous avez besoin d'une vidéo avec une piste audio fonctionnant sur le lecteur "Maître". Nous travaillons sur cette restriction, qui sera supprimée dans les futures versions.

Le média assigné au lecteur maître n'a pas de son
Il y a une petite limitation lors de l'utilisation de LKV. L'entrée de LKV doit avoir du son ; sinon, le lecteur ne peut pas lire le flux. C'est le comportement par défaut du matériel LKV.

Si le média assigné à votre lecteur maître **n'a pas de son**, par exemple une image, vous devez **mettre en sourdine TOUS** les lecteurs esclaves (à partir des paramètres de l'écran dans l'onglet Son/Affichage) pour surmonter la limitation de LKV.

### La lecture vidéo n'est pas fluide. Il y a des saccades et des glitches.

Tout le système doit fonctionner à la même fréquence d'images et Hz. Vous devez faire ce qui suit :
1. Vérifiez la fréquence d'images du contenu vidéo que vous affichez. Elle doit être de 30 FPS (ou 60 FPS) ou de 25 FPS (ou 50 FPS).
2. Si vous avez un ensemble mixte de contenu (30/60 et 25/50), sélectionnez l'un des deux pour commencer un test et voir quel paramètre donne le meilleur résultat.
3. Si vous avez du contenu à 25/50 FPS, vous devez définir la résolution de sortie de tous les lecteurs (y compris le lecteur "Maître") à 25Hz (ou 50Hz).
4. Si vous avez du contenu à 30/60 FPS, vous devez définir la résolution de sortie de tous les lecteurs (y compris le lecteur "Maître") à 30Hz (ou 60Hz).
5. Dans le cas standard, vous devriez utiliser des résolutions 1080p ou 720p (selon vos écrans).
6. Évaluez et, si le résultat n'est pas satisfaisant, recommencez avec un paramètre différent.

### La vidéo semble de mauvaise qualité.

- Vérifiez la source vidéo originale sur votre PC et assurez-vous qu'elle est de meilleure qualité.
- Vérifiez que la source HDMI (dans la plupart des cas, le lecteur) fonctionne en résolution Full HD.
- Consultez le guide suivant sur la mise à jour du firmware du LKV373A pour avoir une résolution Full HD (1080p) au lieu de HD-Ready (720p).

### Les écrans du mur vidéo ne sont pas synchronisés à 100%.

- Vérifiez que les écrans n'ont pas de traitement d'image activé. De nombreuses marques ont des fonctionnalités avancées qui rendent l'image fluide et ont un excellent mouvement. Essayez de désactiver autant de fonctionnalités similaires que possible, réduisant la clarté de l'image, le mouvement fluide et d'autres fonctionnalités similaires. Assurez-vous de le faire sur toutes les TV.
- Si la TV a un mode "jeu" (utilisé pour les jeux de console), essayez de l'utiliser – cela devrait éliminer les décalages. Assurez-vous de le faire sur toutes les TV.
- Éteignez le LKV373A pendant 2 minutes, puis rallumez-le. Les lecteurs devraient redémarrer la lecture et devraient être synchronisés. Si le problème est corrigé au début et se reproduit, essayez d'utiliser un autre commutateur réseau. Le commutateur pourrait induire des retards.

## Configuration de l'unité émettrice LKV373A

Le LKV373A a un petit bug qui ne conserve pas la résolution Full HD pour le flux après un redémarrage. Si vous conservez le firmware d'origine, vous ne pouvez travailler qu'avec une résolution 1280x720.

Si vous voulez une résolution plus élevée, vous devez suivre la procédure suivante pour mettre à jour le firmware de l'appareil.

**AVERTISSEMENT : Assurez-vous** d'utiliser ce firmware uniquement sur le Lenkeng LKV373A **(il est indiqué V3.0 en bas)**. Flasher ce firmware sur un autre modèle pourrait le casser. C'est généralement une procédure risquée, alors ne le faites que si vous avez une unité de rechange à utiliser si cette procédure échoue.

1. Téléchargez le firmware en cliquant ici.
2. Extrayez le fichier ZIP dans un répertoire sur votre ordinateur.
3. Trouvez l'IP du Lenkeng LKV373A dans votre réseau.
4. Entrez l'IP de l'appareil dans votre navigateur. Une page devrait apparaître. Vérifiez que les versions du firmware affichées sont les suivantes par défaut :
    1. **Version : 4.0.0.0.20161031** – C'est le firmware du logiciel de gestion de l'appareil
    2. **Version de l'encodeur : 7.1.2.0.11.20161031** – C'est le firmware de la puce d'encodeur dans l'appareil
5. Vous devrez mettre à jour le firmware de l'appareil. Dans la section "Fichier à mettre à jour le firmware (*.PKG) :" cliquez sur choisir un fichier.
6. Parcourez le répertoire avec le contenu extrait du fichier ZIP et entrez dans le sous-répertoire "TX" (Émetteur).
7. Sélectionnez le fichier "IPTV_TX_PKG_v4_0_0_0_20160427.PKG".
8. Cliquez sur le bouton "Mettre à jour !" sur la page web. L'unité commencera à effectuer la mise à jour.
9. Un message disant "Mise à jour du firmware, veuillez patienter..." apparaîtra. Veuillez patienter.
10. Après 1 minute, un message apparaîtra disant "Veuillez redémarrer l'appareil".
11. Redémarrez l'appareil.
12. L'appareil devrait maintenant fonctionner en résolution Full HD (1728x1080, mais c'est anamorphique, donc ça fonctionne bien).

Après la mise à jour, vous pouvez également ouvrir le flux avec VLC sur votre PC en utilisant (presque) la même adresse (vous devez ajouter un @) :
udp://@239.255.42.42:5004

Dans VLC, vous pouvez vérifier la résolution du flux et confirmer qu'il diffuse en 1080p (pour une source HDMI 1080p).

De plus, l'appareil fournit maintenant plus de contrôles via son interface web. Pour réinitialiser les identifiants d'accès aux valeurs par défaut, vous devez utiliser Telnet (ou PuTTY) et telnet à l'IP de l'appareil sur le port 9999. À la connexion, vous verrez cette invite :

```
Trying 192.168.0.110...
Connected to 192.168.0.110.
Escape character is '^]'.
==============================
========IPTV TX Server========
==============================
input> factory_reset
Processing factory reset!
System will reboot after few seconds!
Connection closed by foreign host.
```

Vous pourrez alors accéder à l'interface web de l'appareil en utilisant les identifiants :

- **Nom d'utilisateur :** admin
- **Mot de passe :** 123456
