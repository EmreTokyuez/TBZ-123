# Laborübung 3: DNS Server - PiHole

Vollständige Aufgabenstellung findet man [hier](https://gitlab.com/alptbz/m123/-/blob/main/06_DNS/01_DNS%20Server.md)

## Erledigte Vorbereitungen
- Thema eingelesen (Dokumente auf Teams)
- GNS3 Projekt importiert
- Passwort 'admin' gesetzt 
- Konfiguration importiert
- Lizenz aktiviert
- PC1 gestartet
![Netzwerk in GNS3](images/netzwerk.png)
## 1. Ping Anfrage
In PC1
```
ping tbz.ch
```
Services die laufen, weil dies klappt:
- DHCP -> Damit wir uns mit dem Router im Netzwerk verbinden koennen und Anfragen schicken und erhalten koennen.
- DNS-Server -> Damit wir von  tbz.ch die IPv4 Adresse kriegen und mithilfe dieser uns verbinden koennen. 

## 2. DNS Query sniffen

### Fragen

- Welcher Host ist der DNS Server?
- Wie lange ist die Antwort (DNS Query Response) gültig?
- Was macht der Router mit der erhaltenen DNS Query?
- Ist die DNS Anfrage signiert? Könnte diese Anfrage gefälscht werden? 

## 3. PiHole aufsetzen


### Statische IP Adresse konfigurieren
### Pi-hole installieren

### Korrekter DNS Server im DHCP Server eintragen

### Fragen
- Wie teilt der Client dem Server mit, dass er DNSSEC verwenden möchte?
- Wie unterscheidet sich eine Query Response mit DNSSEC gegenüber einer ohne?

## 4. Pi-hole Ad und Telemetry blockierende Funktionen ausprobieren

## Weiterführende Ressourcen 

## Neue Lerninhalte

## Reflexion

