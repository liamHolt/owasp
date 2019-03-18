# 	Penetrationtesting Cheat Sheet

Wichtiges Repository: 

swisskyrepo/PayloadsAllTheThings

##	Reconaissance

### NMap Scans

Intensive Scan:

 ```bash
nmap -T4 -A -v <IP>
```

Intensive Scan + UDP

```bash
nmap -sS -sU -T4 -A -v <IP>
```

Intensive Scan + All TCP Ports
```bash
nmap -p 1-65535 -T4 -A -v 10.10.10.107
```

### Stego
 ```bash
steghide extract -sf <picture.png>
```

 ```bash
binwalk <picture.png>
```

 ```bash
strings <picture.png> |less
```


### Searchsploit

Mächtiges Tool zum Suchen von Schwachstellen

```bash
searchsploit "service oder os oder version..."
```

### Dirb(uster)

Tool zum aufspüren von Unterverzeichnissen und Dateien. Dirb sucht mit Bruteforce nach Einträgen aus Wörterbüchern. Geeignete Wörterbücher liegen bei Kali unter /usr/share/dirb/wordlists/ oder /usr/share/dirbuster/wordlists/. Das dirbuster Verzeichnis eignet sich eher für Verzeichnissuchen und das dirb Verzeichnis für Dateisuchen.

![DIRB](/06/Help/2-Dirb_configuration.png)

##	Exploitation

##	Post Exploitation

##	Sonstiges

