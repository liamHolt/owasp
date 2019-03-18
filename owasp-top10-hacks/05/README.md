# 	Carrier

 Ein kurzes Tutorial für die Maschine "Carrier" von hackthebox.eu

 https://www.hackthebox.eu/home/machines/profile/155

 Die Maschine lehrt den Umgang mit Dirb (Suche von Unterverzeichnissen und Dateien), Simple Network Management Protocol Requests, Burp, Remote Code Execution Vulnerabilitys und Reverse Shells.  

Einschätzung:

![NMAP](Carrier/einschaetzung.png)
 
## Anleitung


 1. NMAP Scan 

    ![NMAP](Carrier/1-NmapScan.png)


 2. Besuch auf Port 80

    ![NMAP](Carrier/02-web.png)

 3. Dirb Scan Resultate (zum Scannen siehe Cheat Sheet)

    ![NMAP](Carrier/3-dirbResult.png)

 4. Beim Scannen der Verzeichnisse findet man das Verzeichnis "/doc".  

    ![NMAP](Carrier/4-docVerzeichnis.png)

 5. Das Verzeichnis liefert eine interessante Datei mit Fehlercodes. Unter anderem sind hier die Fehlercodes aus der Startseite aufgeführt.

    ![NMAP](Carrier/5-errorCodes.png)


 6. Port 161 gibt Hinweise auf SNMP Protokoll. Es wird im Internet nach einer Methode zum erstellen von Requests gesucht.

    ![NMAP](Carrier/6-snmpRecherche.png)

 7. Mit dem Tool snmpwalk (bei Kali vorinstalliert), lässt sich ein Request erstellen. Dieser liefert die Seriennummer des SNMP-Servers. Aus den Fehlercodes wissen wir, dass dies das Default Password für den Login Bereich ist. (Nutzername: admin, Passwort: NET_45JDX23)

    ![NMAP](Carrier/7-snmpWalkRequest.png)

 8. Im Admin Bereich unter dem Reiter "Diagnostics" kann der Status des Dienstes verifizieren. Die Antwort lässt vermuten, dass es sich dabei um Kommandozeilencode handelt. Der Request wird mit "Burp" abgefangen und analysiert.

    ![NMAP](Carrier/8-BurpVerifyRequestAbfangen.png)


 9. Request wird an Repeater gesendet (strg+R oder copy paste), damit er verändert und mehrfach ausgeführt werden kann.

    


 10. Dekodiert man den Wert hinter "check" mit Base64, erhält man "quagga". Die Vermutung, dass hier Code ausgeführt werden kann, verstärkt sich. Es wird ein Testbefehl angehängt um sicher zu gehen.

    ![NMAP](Carrier/12-befehlAnhaengen.png)


 11. Der Befehl wird getestet und Remote Code Execution Vulnerability festgestellt.

    ![NMAP](Carrier/13-befehlTesten.png)



 12. Es wird anschließend nach Code zum erstellen einer Reverse Shell gesucht.

    ![NMAP](Carrier/14-reverseShellErstellen.png)

 13. Der Befehl für die Shell wird eingefügt und mit Base64 kodiert.

    ![NMAP](Carrier/15-encodeBase64.png)

 14. Zum Schluss wird nur noch ein Listener erstellt (nc -nvlp 444), welcher die Reverse Shell empfängt. 

    ![NMAP](Carrier/16-requestSenden.png)

