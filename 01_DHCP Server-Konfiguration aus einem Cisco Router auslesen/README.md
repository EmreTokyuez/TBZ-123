# Laborübung 1: DHCP Server-Konfiguration aus einem Cisco Router auslesen

Vollständige Aufgabenstellung: 

## Erledigte Vorbereitungen
 - Thema eingelesen (Dokumente auf Teams)
 - GNS3 Projekt importiert

## 2. Router starten, einloggen und konfigurierte IP-Adressen auslesen

 - Welche IP-Adresse ist auf dem *Interface* *GigabitEthernet0/0* und *GigabitEthernet0/1* konfiguriert?
   - 192.168.122.90/24
 - Ist das *Interface* *GigabitEthernet0/2* aktiv? Welchen Status hat es?
   - administratively down,  down
 - Wo ist das *Interface* *GigabitEthernet0/1* in der Netzwerkgrafik zu finden?
![Interface ist da](images/Switch.png)

## 3. Konfiguration anzeigen
 - Mit welchem Befehl (wie lautet die Zeile) wurde der Name des Routers konfiguriert?
  ```
  hostname R1
  ```
   
 - Wie lautet das Passwort für den *remote access* mit TELNET?
  ```
  cisco
  ```

## 4. DHCP Konfiguration
- Welche IP-Adresse wird dem ersten DHCP-Client vergeben, der einen DHCP request macht?
```
 Current index 
 192.168.10.64
```

## 5. DHCP Lease
 Link zur Pcap-Datei: 

- Welche IP Adresse wir dem Client zugeteilt?
  192.168.10.65
- Nach welcher Zeit müssen die Clients den DHCP lease erneuern?
  86400s -> 1 day
- Welche Option Nummer hat die Option "Router"?
  Option (3)
- Welche Option Nummer hat die Option "Domain Name Server"
  Option (6)
## 6. VPCS

```
show ip
```

```
dhcp
```

```
ping 192.168.10.1
```

```
ping google.ch
```


```
ping 8.8.8.8
```
## 7. PCs konfigurieren
## 8. Cisco CLI Befehl herausfinden - DHCP bindings
## 9. Ubuntu Desktop Guest
# Weiterführende Ressourcen 
- Dokumente auf Teams ueber DHCP
## Neue Lerninhalte
Das war für mich neu: 
 - Cisco CLI Befehle

## Reflexion
Mithilfe der Übung habe ich nun das Gefühl eine grobe Übersicht über GNS3 zu haben. Der [Kompetenz](../01_Kompetenzmatrix/README.md) *D1G: Ich kann einfache statische Routingtabellen umsetzen.* bin ich nun definitiv einen Schritt näher gekommen. 
Ich fand die Übung sehr einfach und hatte keine grosse Mühe. 

