# Laborübung 5: SMB - Lokale Dateiablage auf einem NAS
Vollständige Aufgabenstellung findet man [hier](https://gitlab.com/alptbz/m123/-/blob/main/07_Datei%C3%BCbertragung/02_NAS.md)

## Offerte

Da ich zuhause auch ein NAS besitze, auf dem Unraid lauft wuerde ich auf aehnliche Hardware greifen und das NAS selber bauen. Folgende Teile wuerde ich bestellen:

| Name                                                                                                                                                                | Preis |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| [Intel Core i5-9500](https://www.digitec.ch/en/s1/product/intel-core-i5-9500-lga-1151-3-ghz-6-core-processors-11131511?supplier=406802)                             | 188.- |
| [Gigabyte Z390 M Gaming](https://www.digitec.ch/en/s1/product/gigabyte-z390-m-gaming-lga-1151-intel-z390-matx-motherboards-9871234?supplier=406802)                 | 130.- | kv |
| [Samsung 970 EVO 500GB](https://www.digitec.ch/en/s1/product/samsung-970-evo-500-gb-m2-2280-ssd-8351214?supplier=406802)                                            | 75.-  |
| [be quiet! Pure Power 11](https://www.digitec.ch/en/s1/product/be-quiet-pure-power-11-500-w-power-supply-pc-10034250?supplier=406802)                               | 69.-  |
| [Corsair Vengeance LPX 2x16GB](https://www.digitec.ch/en/s1/product/corsair-vengeance-lpx-2-x-16gb-3200-mhz-ddr4-ram-dimm-ram-5834370?supplier=406802)              | 115.- |
| [Fractal Node 804](https://www.digitec.ch/en/s1/product/fractal-node-804-mini-itx-matx-pc-case-2577009?supplier=406802)                                             | 115.- |
| [APC Back-UPS 750VA IEC](https://www.digitec.ch/en/s1/product/apc-back-ups-750va-iec-750-va-410-w-line-interactive-protection-class-5-ups-14044689?supplier=406802) | 104.– |
| [Lindy IEC power cable](https://www.digitec.ch/en/s1/product/lindy-iec-power-cable-2-m-power-cables-13911995?supplier=406802)                                       | 14.–  |
| [Furber T13 — C14](https://www.digitec.ch/en/s1/product/furber-t13-c14-030-m-power-cables-21562447?supplier=406802)                                                 | 11.-  |
| [2x WD Red Plus 4TB CMR](https://www.digitec.ch/en/s1/product/wd-red-plus-4-tb-35-cmr-hard-drives-14726161)                                                         | 206.- |
| 12 Stunden arbeit und Training                                                                                                                                      | 600.- |

Die Selektion der Hardware ist zum Teil viel, jedoch gibt es dem Unternehmen mehr Raum fuer die Zukunft und mehr Moeglichkeiten, die eigene Infrastruktur flexibel zu nutzen (CI/CD, eigenes Git, eigener Webserver). Eine Samsung SSD wurde auch einberechnet, um die 100MB/s Transferraten bei 3 Nutzern sicherzustellen, da die SSD als Cache-Drive benutzt wird. Die HDD's werden gespiegelt und deswegen werden 2 von denen gebraucht, damit wir eines verlieren koennen und trotzdem alle Daten besitzen. Auf ECC-RAM wurde verzichtet, da die Mehrkosten sich bei diesem Umfang nicht lohnen wuerden. Ein UPS wuerde einberechnet, damit das NAS bei einem Stromausfall genuegend Zeit hat sicher herunterzufahren und Datenkorruption somit verhindern kann.


## Vorbereitungen GNS3

- DNS Labor kopiert
- FreeNAS Geraet hinzugefuegt und mit dem Netzwerk verbunden.
  ![GNS3 Setup](images/gns3%20setup.png)
  Spaeter wird die Windows VM hinzugefuegt
## TrueNAS Core installation
- Per VNC auf den TrueNAS-PC  zugegriffen
- Installation ausgefuert wie in der Anleitung [hier](https://www.truenas.com/blog/how-to-install-truenas-core/
)
- Passwort zu "root" gesetzt sowie "Boot via BIOS" benutzt, da das UEFI nicht funktioniert hat (ist die VM veraltet? War stuck beim booten).
- Per

## TrueNAS Konfiguration
- Eingeloggt via VNC-Verbindung zu einem Ubuntu-Desktop
### Pool und Dataset

## Benutzer Setup
- Chef
  - Username: Chef
  - PW: Chef
- Buchhalter
  - Username: Buchhalter
  - PW: Buchhalter
- Entwickler
  - Username: Entwickler
  - PW: Entwickler


### SMB Shares
Berechtigungen fuer die Shares wurden wie in der Aufgabenstellung uebernommen:
![Berechtigungen](images/Berechtigungsmatrix.png)



### Ubuntu Desktop fuer den Entwickler
### Windows VM fuer die Buchhaltung

## Weiterführende Ressourcen 
https://www.truenas.com/blog/how-to-install-truenas-core/
https://www.truenas.com/docs/core/coretutorials/storage/pools/datasets/
https://www.truenas.com/docs/core/gettingstarted/storingdata/
https://www.truenas.com/docs/core/coretutorials/sharing/smb/smbshare/#create-local-user-accounts
## Neue Lerninhalte


## Reflexion
