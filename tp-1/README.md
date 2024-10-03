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
PS C:\Users\guill> arp -a

Interface : 10.33.73.50 --- 0x14
  Adresse Internet      Adresse physique      Type
  10.33.69.62           90-0f-0c-88-92-6f     dynamique
  10.33.79.254          7c-5a-1c-d3-d8-76     dynamique
```

---
# Go Further
---

