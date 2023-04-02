
Le but de ce papier est de faire le point sur les solutions techniques existantes pour obtenir une passerelle entre le réseau GSM et Internet, ce qu'on appelerait en anglais un sms-gateway

L'utilité de créer une telle jonction est multiple

Offre la possibilité de faire de la domotique et de contrôler par exemple des objets connectés en envoyant des commandes par sms

Obtenir des informations sur son téléphone pratiquement n'importe où sans avoir besoin d'utiliser les données mobiles ou bien être connecté à un réseau wifi, on peut demander par exemple via un webscrapper la météo ou bien encore faire une requête auprès de chatGPT

Être notifié d'un événement qui s'est produit, comme une alerte sur une caméra IP suite à une détection de mouvement sans qu'on soit à proximité

Possibilité de commununiquer sur d'autres plateformes de discussion en utilisant leur API dédié

Pouvoir envoyer de multiples sms programmés à l'avance depuis son ordinateur pour avertir ou informer les destinataires

Et bien d'autres cas d'usage

------------


#####Service d'envoi de sms en ligne

On trouve généralement dans sur internet des sites proposant principalement la possibilité d'envoyer en masse des sms, mais plus rarement celle d'en recevoir, et encore moins d'avoir le choix d'envoyer et d'en recevoir sur son téléphone par le biais de son ordinateur

<p align="center"><img src="http://i.imgur.com/sqgvTpf.png"  width="300px"/></p>

Ces sites proposes souvent des abonnements sous forme de pack avec un quota limité de sms, le prix étant dégressif par rapport au nombre potentiel de sms que vous envoyer

|  <div style="width:300px"> Avantages </div>| <div style="width:300px"> Inconvénients </div>  |
| - |  -|
| - Solution déjà toute prête<br> - Gain de temps non négligeable|  - Communication non bidirectionnelle<br> - Prix souvent prohibitif par rapport au prix de revient d'un envoi de sms<br> - Vous n'êtes pas maître des données que vous envoyé|
<br>
#####Logiciels de synchronisation sms

|  <div style="width:300px"> Avantages </div>| <div style="width:300px"> Inconvénients </div>  |
| - |  -|
|  - Mise en place rapide sur les différentes plateformes disponibles <br>- Les SMS sont répliqués sur tous vos appareils|- Impossible d'utiliser les sms en dehors du cadre d'une discussion<br>- Offre payante assez onéreuse<br>- SMS disponibles que sur les appareils sur lequel on a installé le programme<br>- Les données ne vous appartiennent pas| 


<br>
#####Les modems ou dongle gsm/4g/5g

|  <div style="width:300px"> Avantages </div>| <div style="width:300px"> Inconvénients </div>  |
| - |  -|
|  - Possibilité d'avoir internet <br>- Facilité de l'installation|- Carte sim non utilisable pour l'appel<br>- Prix de l'appareil| 


<br>
#####API HTTP

https://github.com/NdoleStudio/httpsms


|  <div style="width:300px"> Avantages </div>| <div style="width:300px"> Inconvénients </div>  |
| - |  -|
| Mise en place assez rapide<br> -Open source<br> -Gratuit jusqu'à 200 envois/réceptions sms<br> -Intégration aisée dans d'autres projets|  -Reste toutefois une solution payante <br> - Nous n'avez pas la main sur les données stockées <br> -Utilisation du cloud Google|

<br>
#####API HTTP dédié

https://raspisms.fr/

|  <div style="width:300px"> Avantages </div>| <div style="width:300px"> Inconvénients </div>  |
| - |  -|
| - Entièrement gratuit et pas de limitations si vous hébergez vous même le serveur<br> - Nombreuses fonctionnalités telle que l'utilisation des webhook<br> - Vous contrôlez entièrement les données qui transitent au serveur|  - Solution assez lourde (certaines fonctions non utilisées par exemple)<br> - Ne peut s'installer que sur Linux à l'heure actuelle<br> - Nécessite une machine dédiée|






