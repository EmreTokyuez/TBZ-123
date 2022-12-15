# Laborübung 1: DHCP Server-Konfiguration aus einem Cisco Router auslesen

Vollständige Aufgabenstellung findet man [hier]()

## Erledigte Vorbereitungen
 - Thema eingelesen (Dokumente auf Teams)
- GNS3 Projekt importiert, Cisco Router  ausgetauscht fuer Mikrotik CHR Router
- Passwort 'admin' gesetzt 

## Grundkonfiguration Microtik Router R1
- Anzahl Netzwerkadapter auf 4 gesetzt
```
/system identity set name=R1
/ip address add address=192.168.10.1/24 interface=ether2 network=192.168.10.0
/ip dns set allow-remote-requests=yes
/ip firewall nat add action=masquerade chain=srcnat out-interface=ether1
```
## R1 Hostname, IP Einstellungen
## R1 DHCP-Setup
## Weiterführende Ressourcen 
- Dokumente auf Teams ueber DHCP
## Neue Lerninhalte

## Reflexion

