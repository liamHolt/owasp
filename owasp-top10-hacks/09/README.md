# 	Devel

 Ein kurzes Tutorial für die Maschine "Devel" von hackthebox.eu

 https://www.hackthebox.eu/home/machines/profile/170

 Die Maschine lehrt den Umgang mit Metasploit, FTP und Reverse Shells.
 
## Anleitung


 1. NMAP Scan 

    ![NMAP](DEVEL/1-NmapScan.png)


 2. Reverse Shell erstellen. aspx Dateien werden für gewöhnlich von Microsoft ausgeführt.

    ![NMAP](DEVEL/2-createReverseShell.png)

 3. Listener starten

    ![NMAP](DEVEL/3-createListener.png)

 4. Shell auf FTP Server deponieren

    ![NMAP](DEVEL/5-shellDeponieren.png)

 5. Über den Browser zur Shell navigieren und ReverseShell ausführen

    ![NMAP](DEVEL/6-shellAusfuehren.png)


 6. Mit Metasploit Shell erstellen und Systeminfo anzeigen

    ![NMAP](DEVEL/7-createShellFromMeterpreter.png)

 7. Um root Rechte zu erhalten, wird zum Schluss nach einem Exploit für Privilege Escalation gesucht und ausgeführt.

    ![NMAP](DEVEL/8-privilegeEscalation.png)

# 	Lame

 Ein kurzes Tutorial für die Maschine "Lame" von hackthebox.eu

 https://www.hackthebox.eu/home/machines/profile/1

 Die Maschine lehr den Umgang mit Searchsploit, OpenVas, Metasploit und Reverse Shells
 
## Anleitung


 1. NMAP Scan 

    ![NMAP](Lame/1-NMapScan.png)


 2. Openvas Scan. (Zum starten eines Scans: Scans-> TaskWizard(Lila Zauberstab) -> Ip-Adresse eingeben)

    ![NMAP](Lame/2-OpenVasResult.png)

 3. Suche nach Metasploit modul über searchsploit

    ![NMAP](Lame/3-Metasploit-ModulSuchen.png)

 4. Modul verwenden

    ![NMAP](Lame/4-MetasploitModulVerwenden.png)

 5. Mit "show options" die Einstellungen anzeigen. Anschließend RHOST (Remote-Host) und RPORT(Remote-Port) setzen und Skript ausführen mit "exploit".

    ![NMAP](Lame/5-shellMitMetasploit.png)

# 	Legacy

 Ein kurzes Tutorial für die Maschine "Legacy" von hackthebox.eu

 https://www.hackthebox.eu/home/machines/profile/2

 Die Maschine lehr den Umgang mit Searchsploit, OpenVas, Metasploit und Reverse Shells
 
## Anleitung


 1. NMAP Scan 

    ![NMAP](Legacy/1-NmapScan.png)


 2. Nach bekannten Schwachstellen für veraltete Windows Version suchen

    ![NMAP](Legacy/2-commonVulnerability.png)

 3. Metasploit Modul verwenden um Exploit auszuführen

    ![NMAP](Legacy/3-useMetasploitModule.png)

 4. Da es sich um eine Windows Maschine handelt, benötigt man DOS Befehle um über die Shell navigieren zu können. Die unten aufgeführten Befehle erleichtern den umgang mit der Shell.

    ![NMAP](Legacy/windowsBashCommands.png)



