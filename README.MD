
Le but de ce papier est de faire le point sur les solutions techniques existantes pour obtenir une passerelle entre le réseau GSM et Internet, ce qu'on appelerait en anglais un sms-gateway

L'utilité de créer une telle jonction est multiple

- Offre la possibilité de faire de la domotique et de contrôler par exemple des objets connectés en envoyant des commandes par sms

- Obtenir des informations sur son téléphone pratiquement n'importe où sans avoir besoin d'utiliser les données mobiles ou bien être connecté à un réseau wifi, on peut demander par exemple via un webscrapper la météo ou bien encore faire une requête auprès de chatGPT

- Être notifié d'un événement qui s'est produit, comme une alerte sur une caméra IP suite à une détection de mouvement sans qu'on soit à proximité

- Possibilité de commununiquer sur d'autres plateformes de discussion en utilisant leur API dédié

- Pouvoir envoyer de multiples sms programmés à l'avance depuis son ordinateur pour avertir ou informer les destinataires

Et bien d'autres cas d'usage

------------


#### Service d'envoi de sms en ligne

On trouve généralement dans sur internet des sites proposant principalement la possibilité d'envoyer en masse des sms, mais plus rarement celle d'en recevoir, et encore moins d'avoir le choix d'envoyer et d'en recevoir sur son téléphone par le biais de son ordinateur

<p align="center"><img src="http://i.imgur.com/sqgvTpf.png"  width="300px"/></p>

Ces sites proposes souvent des abonnements sous forme de pack avec un quota limité de sms, le prix étant dégressif par rapport au nombre potentiel de sms que vous envoyer

|  Avantages| Inconvénients|
| - |  -|
|- Solution déjà toute prête<br> - Gain de temps non négligeable<br><img width=450/>|  - Communication non bidirectionnelle<br> - Coût important par rapport au prix de revient d'un envoi de sms<br> - Vous n'êtes pas maître des données que vous envoyé<br><img width=450/>|


#### Logiciels de synchronisation sms
mysms, pulse,  pushbullet sont des applications qui vous permettent de répliquer les sms sur votre ordinateur, et également d'envoyer des sms depuis votre pc

|  Avantages| Inconvénients|
| - |  -|
|- Mise en place rapide sur les différentes plateformes disponibles <br>- Les SMS sont répliqués sur tous vos appareils<br><img width=450/>|- Impossible d'utiliser les sms en dehors du cadre d'une discussion<br>- Offre payante assez onéreuse<br>- SMS disponibles que sur les appareils sur lequel on a installé le programme<br>- Les données ne vous appartiennent pas<br><img width=450/>| 


#### Les modems ou dongle gsm/4g/5g
Pour un usage plutôt nomade, l'intérêt principal d'un tel appareil étant d'avoir internet, on peut toutefois intercepter les sms via petit script qui tourne en permanence sur la machine. Il se peut que certains modèles ne soient pas compatible avec la lecture et/ou l'envoi de sms 

| Avantages | Inconvénients|
| - | -|
|- Possibilité d'avoir internet <br>- Facilité de l'installation<br><img width=450/>|- Carte sim non utilisable pour l'appel<br>- Prix de l'appareil<br><img width=450/>| 


#### API HTTP

https://github.com/NdoleStudio/httpsms

Projet open source, l'API peut s'intégrer facilement à d'autres projets, le service fonctionne de la façon suivante : 
- Installation d'une application côté client qui permet de gérer localement les sms (envoi de requête au serveur en cas de nouveau sms reçu, et expédition de messages si le serveur en fait la demande)
- Mise en place d'un serveur qui va créer la liaison avec Internet lorsqu'il reçoit des informations du client

|  Avantages|Inconvénients|
| - |  -|
|- Mise en place assez rapide<br>- Open source<br>- Gratuit jusqu'à 200 envois/réceptions sms<br>- Intégration aisée dans d'autres projets<br><img width=450/>|- Reste toutefois une solution payante <br>- Nous n'avez pas la main sur les données stockées <br>- Utilisation du cloud Google<br><img width=450/>|


#### API HTTP dédié
https://raspisms.fr/

Même principe que ci-dessus, à la différence que le serveur peut être une machine que vous possédez et dont vous en faites de l'auto-hébergement 

|Avantages|Inconvénients|
| - |  -|
|- Entièrement gratuit et pas de limitations si vous hébergez vous même le serveur<br>- Nombreuses fonctionnalités telle que l'utilisation des webhook<br> - Vous contrôlez entièrement les données qui transitent au serveur<br><img width=450/>|- Solution assez lourde (certaines fonctions non utilisées par exemple)<br>- Partie serveur ne peut s'installer que sur Linux à l'heure actuelle<br> - Nécessite une machine dédiée<br><img width=450/>|


#### API HTTP dédié multiplateforme

Même principe que ci-dessus mais cette fois-ci le côté serveur peut être installé sur n'importe quelle machine avec Python dessus

J'utilise deux projets déjà existants

La partie client reprend le travail de ce repo https://github.com/juancresc/SMSHub

La partie serveur est une modification de cette version de ce script : https://gist.github.com/hawkins/36b7d781d8fa5277d4cb29b6906abe57

Les deux parties réunies nous donnent le nouveau repo que j'ai crée : https://github.com/Hyperyon/sms




