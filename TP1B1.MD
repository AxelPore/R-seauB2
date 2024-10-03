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

```
PS C:\Users\axelp> ping 10.33.79.254

Envoi d’une requête 'Ping'  10.33.79.254 avec 32 octets de données :
Délai d’attente de la demande dépassé.
Délai d’attente de la demande dépassé.
Délai d’attente de la demande dépassé.
Délai d’attente de la demande dépassé.

Statistiques Ping pour 10.33.79.254:
    Paquets : envoyés = 4, reçus = 0, perdus = 4 (perte 100%),
```

```
PS C:\Users\axelp> ping 10.33.72.177

Envoi d’une requête 'Ping'  10.33.72.177 avec 32 octets de données :
Réponse de 10.33.72.177 : octets=32 temps=5 ms TTL=128
Réponse de 10.33.72.177 : octets=32 temps=14 ms TTL=128
Réponse de 10.33.72.177 : octets=32 temps=4 ms TTL=128
Réponse de 10.33.72.177 : octets=32 temps=5 ms TTL=128

Statistiques Ping pour 10.33.72.177:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 4ms, Maximum = 14ms, Moyenne = 7ms
```

```
PS C:\Users\axelp> ping www.thinkerview.com

Envoi d’une requête 'ping' sur www.thinkerview.com [188.114.96.7] avec 32 octets de données :
Réponse de 188.114.96.7 : octets=32 temps=15 ms TTL=55
Réponse de 188.114.96.7 : octets=32 temps=15 ms TTL=55
Réponse de 188.114.96.7 : octets=32 temps=14 ms TTL=55
Réponse de 188.114.96.7 : octets=32 temps=20 ms TTL=55

Statistiques Ping pour 188.114.96.7:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 14ms, Maximum = 20ms, Moyenne = 16ms
```

```
PS C:\Users\axelp> nslookup www.thinkerview.com
Serveur :   dns.google
Address:  8.8.8.8

Réponse ne faisant pas autorité :
Nom :    www.thinkerview.com
Addresses:  2a06:98c1:3121::7
          2a06:98c1:3120::7
          188.114.96.7
          188.114.97.7
```

```
PS C:\Users\axelp> nslookup www.wikileaks.org
Serveur :   dns.google
Address:  8.8.8.8

Réponse ne faisant pas autorité :
Nom :    wikileaks.org
Addresses:  51.159.197.136
          80.81.248.21
Aliases:  www.wikileaks.org
```

```
PS C:\Users\axelp> nslookup www.torproject.org
Serveur :   dns.google
Address:  8.8.8.8

Réponse ne faisant pas autorité :
Nom :    www.torproject.org
Addresses:  2a01:4f8:fff0:4f:266:37ff:feae:3bbc
          2620:7:6002:0:466:39ff:fe32:e3dd
          2a01:4f9:c010:19eb::1
          2620:7:6002:0:466:39ff:fe7f:1826
          2a01:4f8:fff0:4f:266:37ff:fe2c:5d19
          204.8.99.146
          95.216.163.36
          204.8.99.144
          116.202.120.166
          116.202.120.165
```
## IV. Network scanning et adresses IP

```
PS C:\Users\axelp> nmap.exe -sn -PR 10.33.64.0/20

Nmap scan report for 10.33.66.78
Host is up (0.17s latency).
MAC Address: E4:B3:18:48:36:68 (Intel Corporate)
Nmap scan report for 10.33.67.113
Host is up (0.098s latency).
MAC Address: D2:91:DE:DF:9A:6E (Unknown)
Nmap scan report for 10.33.68.203
Host is up (0.84s latency).
MAC Address: AA:E3:0B:A8:53:8A (Unknown)
Nmap scan report for 10.33.68.210
Host is up (0.27s latency).
MAC Address: 52:96:20:27:E8:9D (Unknown)
```

```
Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Description. . . . . . . . . . . . . . : Killer(R) Wi-Fi 6E AX1675i 160MHz Wireless Network Adapter (211NGW)
   Adresse physique . . . . . . . . . . . : F0-57-A6-D2-8A-02
   DHCP activé. . . . . . . . . . . . . . : Non
   Configuration automatique activée. . . : Oui
   Adresse IPv6 de liaison locale. . . . .: fe80::216:31f9:f43c:db6b%14(préféré)
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.64.26(préféré)
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Passerelle par défaut. . . . . . . . . : 10.33.79.254
   IAID DHCPv6 . . . . . . . . . . . : 149968806
   DUID de client DHCPv6. . . . . . . . : 00-01-00-01-2D-47-E3-99-F0-57-A6-D2-8A-02
   Serveurs DNS. . .  . . . . . . . . . . : 8.8.8.8
                                       1.1.1.1
   NetBIOS sur Tcpip. . . . . . . . . . . : Activé
```



