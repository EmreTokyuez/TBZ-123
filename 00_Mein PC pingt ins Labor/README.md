# Laborübung 01 Zwei VPCS pingen sich gegenseitig 
---
- Datum: 08.12.2022
- Name: Emre Tokyüz
- Link zur Aufgabenstellung[https://gitlab.com/ch-tbz-it/Stud/m129/-/tree/main/20_GNS3%20Einf%C3%BChrung#2-mein-pc-pingt-ins-labor]
---
## Cloud
---
- tap0 192.168.23.135
- - Eigener PC ist via OpenVPN (Layer2) mit tap0 verbunden.  
Picture

## Config R1
```
/system/identity set name=R1
/ip/address add address=192.168.24.1/24 interface=ether2
/ip/address add address=192.168.23.16/24 interface=ether1
```
## Config VPC1
---
```
set pcname PC1
# [IP] [MASKE] [GATEWAY]
ip 192.168.24.2 255.255.255.0 192.168.24.1


```

## Config pc 
---
```
sudo netstat -n 192.16wdwdaw

```
## Quellen
---
https://www.analysisman.com/2020/11/macos-staticroutes.html
https://www.howtogeek.com/howto/windows/adding-a-tcpip-route-to-the-windows-routing-table/

## Neue Lerninhalte
---
netstat command in macos -> transfer command von windows zu macos



## Reflexion
---




