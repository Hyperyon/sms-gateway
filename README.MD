
Le but de ce papier est de faire le point sur les solutions techniques existantes pour obtenir une passerelle entre le réseau GSM et Internet, ce qu'on appelerait en anglais un sms-gateway

L'utilité de créer une telle jonction est multiple

Offre la possibilité de faire de la domotique et de contrôler par exemple des objets connectés en envoyant des commandes par sms

Obtenir des informations sur son téléphone pratiquement n'importe où sans avoir besoin d'utiliser les données mobiles ou bien être connecté à un réseau wifi, on peut demander par exemple via un webscrapper la météo ou bien encore faire une requête auprès de chatGPT

Être notifié d'un événement qui s'est produit, comme une alerte sur une caméra IP suite à une détection de mouvement sans qu'on soit à proximité

Possibilité de commununiquer sur d'autres plateformes de discussion en utilisant leur API dédié

Pouvoir envoyer de multiples sms programmés à l'avance depuis son ordinateur pour avertir ou informer les destinataires

Et bien d'autres cas d'usage

On trouve généralement dans sur internet des sites proposant principalement la possibilité d'envoyer en masse des sms, mais plus rarement celle d'en recevoir, et encore moins d'avoir le choix d'envoyer et d'en recevoir sur son téléphone par le biais de son ordinateur

![Image](http://i.imgur.com/sqgvTpf.png)

Ces sites proposes souvent des abonnements sous forme de pack avec un quota limité de sms, le prix étant dégressif par rapport au nombre potentiel de sms que vous envoyer

Inconvénients : 
communication non bidirectionnelle
le prix souvent prohibitif par rapport au prix de revient d'un envoi de sms
vous n'êtes pas maître des données que vous envoyer

Avantage :
Solution déjà toute prête, gain de temps non négligeable


Logiciels de synchronisation sms
Inconvénients :
Vous n'avez pas la possibilité d'utiliser les sms en dehors du cadre d'une discussion
Ofrre payante assez onéreuse
SMS disponibles que sur les appareils sur lequel on a installé le programme, ou disponible que sur leur site dédié
Données stockées sur un serveur distant qui n'est pas le vôtre

Avantage :
Mise en place rapide sur les différentes plateformes disponible
Les SMS sont répliqués sur tous vos appareils


Les modems ou dongle gsm/4g/5g

Avantage : 
Possibilité d'avoir internet
Facilité de l'installation

Inconviénent :
La carte SIM n'est pas utilisable pour recevoir des appels par exemple
Prix de l'appareil

API HTTP

https://github.com/NdoleStudio/httpsms

Avantage :
Mise en place assez rapide
Open source
Gratuit jusqu'à 200 envois/recéptions sms
Intégration aisée dans d'autres projets

Inconvénient :
Reste toutefois une solution payante
Nous n'avez pas la main sur les données stockées
Utilisation du cloud Google


https://raspisms.fr/

Avantages :
Entièrement gratuit et pas de limitations si vous hébergez vous même le serveur
Nombreuses fonctionnalités telle que l'utilisation des webhook
Vous contrôlez entièrement les données qui transitent au serveur

Inconvénients :
Solution assez lourde
Ne peut s'installer que sur Linux à l'heure actuelle
Nécessite une machine dédiée
