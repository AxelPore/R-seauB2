# TP1B1 Réseau



## I. Récolte d'informations

```
PS C:\Users\axelp> ipconfig /all


Carte réseau sans fil Wi-Fi :

  
   DHCP activé. . . . . . . . . . . . . . : Oui
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.73.111(préféré)
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Passerelle par défaut. . . . . . . . . : 10.33.79.254
   Serveur DHCP . . . . . . . . . . . . . : 10.33.79.254
   Serveurs DNS. . .  . . . . . . . . . . : 8.8.8.8
                                       1.1.1.1
   NetBIOS sur Tcpip. . . . . . . . . . . : Activé




Carte Ethernet Ethernet :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :
   Description. . . . . . . . . . . . . . : Killer E3100G 2.5 Gigabit Ethernet Controller
   Adresse physique . . . . . . . . . . . : D8-BB-C1-B5-91-92
   DHCP activé. . . . . . . . . . . . . . : Oui
   Configuration automatique activée. . . : Oui
```


## II. Utiliser le réseau


```
PS C:\Users\axelp> ping 10.33.73.111

Envoi d’une requête 'Ping'  10.33.73.111 avec 32 octets de données :
Réponse de 10.33.73.111 : octets=32 temps<1ms TTL=128
Réponse de 10.33.73.111 : octets=32 temps<1ms TTL=128
Réponse de 10.33.73.111 : octets=32 temps<1ms TTL=128
Réponse de 10.33.73.111 : octets=32 temps<1ms TTL=128

Statistiques Ping pour 10.33.73.111:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 0ms, Maximum = 0ms, Moyenne = 0ms
```

```
PS C:\Users\axelp> ping 127.0.0.1

Envoi d’une requête 'Ping'  127.0.0.1 avec 32 octets de données :
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128

Statistiques Ping pour 127.0.0.1:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 0ms, Maximum = 0ms, Moyenne = 0ms
```