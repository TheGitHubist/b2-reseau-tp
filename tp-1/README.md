# I. Basics
---
```powershell
PS C:\Users\guill> ipconfig

Carte réseau sans fil Wi-Fi :
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.73.50
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0 ( ou 10.33.73.0/20 en CIDR )
   Passerelle par défaut. . . . . . . . . : 10.33.79.254
```
```powershell
PS C:\Users\guill> get-netadapter

Name                      InterfaceDescription                    ifIndex Status       MacAddress             LinkSpeed
----                      --------------------                    ------- ------       ----------             ---------
Wi-Fi                     Intel(R) Wi-Fi 6 AX201 160MHz                20 Up           28-6B-35-F2-3E-24       1.2 Gbps
```

```
Adresse du réseau LAN :> 10.33.79.0
Adresse Boradcast :> 10.33.79.255
Nombre d'addresses disponibles :> 4096
```

```powershell
PS C:\Users\guill> hostname
Killian
```

```powershell
PS C:\Users\guill> ipconfig /all

   Serveur DHCP . . . . . . . . . . . . . : 10.33.79.254
   Serveurs DNS. . .  . . . . . . . . . . : 8.8.8.8
                                            1.1.1.1
```

```
PS C:\Users\guill> netstat -rn

IPv4 Table de routage
===========================================================================
Itinéraires actifs :
Destination réseau    Masque réseau  Adr. passerelle   Adr. interface Métrique
          0.0.0.0          0.0.0.0     10.33.79.254      10.33.73.50     30
```

---
# Go Further
---

```powershell
# localhost name resolution is handled within DNS itself.
#	127.0.0.1       localhost
#	::1             localhost
1.1.1.1 b2.hello.vous

PS C:\Users\guill> ping b2.hello.vous

Envoi d’une requête 'ping' sur b2.hello.vous [1.1.1.1] avec 32 octets de données :
Réponse de 1.1.1.1 : octets=32 temps=15 ms TTL=55
Réponse de 1.1.1.1 : octets=32 temps=23 ms TTL=55
Réponse de 1.1.1.1 : octets=32 temps=46 ms TTL=55

Statistiques Ping pour 1.1.1.1:
    Paquets : envoyés = 3, reçus = 3, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 15ms, Maximum = 46ms, Moyenne = 28ms
```





```
dns lookup

Type	        Domain Name	                    IP Address	            TTL
A	            www.thinkerview.com	            104.21.73.104	        5 min

reverse dns lookup

Type	        IP Address	                    Domain Name	                          TTL
PTR	            143.90.88.12                    EAOcf-140p12.ppp15.odn.ne.jp	      24 hrs
```

```powershell
PS C:\Users\guill> tracert www.ynov.com

Détermination de l’itinéraire vers www.ynov.com [104.26.11.233]
avec un maximum de 30 sauts :

  1     3 ms     1 ms     1 ms  10.33.79.254
  2     4 ms     2 ms    21 ms  145.117.7.195.rev.sfr.net [195.7.117.145]
  3     2 ms     2 ms     2 ms  237.195.79.86.rev.sfr.net [86.79.195.237]
  4     4 ms     2 ms     3 ms  196.224.65.86.rev.sfr.net [86.65.224.196]
  5    16 ms    12 ms    10 ms  164.147.6.194.rev.sfr.net [194.6.147.164]
  6     *        *        *     Délai d’attente de la demande dépassé.
  7    15 ms    16 ms    15 ms  162.158.20.31
  8    15 ms    15 ms    16 ms  104.26.11.233
```

```powershell
   Passerelle par défaut. . . . . . . . . : 10.33.79.254
```

---
# Le requin
---