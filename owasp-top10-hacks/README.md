# 	Anwendungsbeispiele für OWASP TOP 10    

“OWASP Top 10” ist eine Veröffentlichung des Open Web Application Security Project (OWASP). In ihr sind die 10 häufigsten Sicherheitsrisiken für Webanwendungen nach Priorität aufgelistet. Um das Konzept der Bedrohungen nachvollziehen und nachstellen zu können, sind im folgenden Anwendungsbeispiele für jede Art von Angriff der OWASP Top 10 zugeordnet.

Alle Beispiele sind bereits vollständig Dokumentiert worden. Bei Bedarf kann die Dokumentation auch als Hilfestellung herangezogen werden. 

https://www.hackingarticles.in/hack-the-box-[NameDerBox]-walkthrough/

Hinweise für den **Zugangscode** für HackTheBox findest du [hier](inviteCode/README.md).

## Penetrationtesting Cheat Sheet

In der Dokumentation wird teilweise vorausgesetzt, dass die Durchführung grundlegender Vorgänge klar ist (z.B. NMap Scan, erstellen von Reverse Shells...). Falls dies nicht der Fall ist, kann das Cheat Sheet verwendet werden. Dieses kann außerdem verwendet werden, um eine Hilfestellung beim Reconaissance-Angriff zu erhalten.

[Cheat Sheet](cheatSheet/README.md)

## OWASP Top 10 - 2017	

### 1 Injection
Injection-Schwachstellen, wie beispielsweise SQL-, OS- oder LDAP-Injection, treten auf, wenn nicht vertrauenswürdige Daten von einem Interpreter als Teil eines Kommandos oder einer Abfrage verarbeitet werden. Ein Angreifer kann Eingabedaten dann so manipulieren, dass er nicht vorgesehene Kommandos ausführen oder unautorisiert auf Daten zugreifen kann.

**Giddy**	https://www.hackthebox.eu/home/machines/profile/153

**Charon**	https://www.hackthebox.eu/home/machines/profile/42

[Dokumentation](01/README.md)

### 2 Fehler in der Authentifizierung
Anwendungsfunktionen, die im Zusammenhang mit Authentifizierung und Session-Management stehen, werden häufig fehlerhaft implementiert. Dies erlaubt es Angreifern, Passwörter oder Session-Token zu kompromittieren oder die entsprechenden Schwachstellen so auszunutzen, dass sie die Identität anderer Benutzer vorübergehend oder dauerhaft annehmen können.

**Lazy**         https://www.hackthebox.eu/home/machines/profile/18

[Dokumentation](02/README.md)


### 3 Verlust der Vertraulichkeit sensibler Daten	

Viele Anwendungen schützen sensible Daten, wie personenbezogene Informationen und Finanz oder Gesundheitsdaten, nicht ausreichend. Angreifer können diese Daten auslesen oder modifizieren und mit ihnen weitere Straftaten begehen (Kreditkartenbetrug, Identitätsdiebstahl etc.). Vertrauliche Daten können kompromittiert werden, wenn sie nicht durch Maßnahmen, wie Verschlüsselung gespeicherter Daten und verschlüsselte Datenübertragung, zusätzlich geschützt werden. Besondere Vorsicht ist beim Datenaustausch mit Browsern angeraten.

**Jerry**         https://www.hackthebox.eu/home/machines/profile/144

[Dokumentation](03/README.md)

### 4 XML External Entities (XXE) (in progress)

Viele veraltete oder schlecht konfigurierte XML Prozessoren berücksichtigen Referenzen auf externe Entitäten innerhalb von XML-Dokumenten. Dadurch können solche externen Entitäten dazu eingesetzt werden, um mittels URI Datei-Handlern interne Dateien oder File-Shares offenzulegen oder interne Port-Scans, Remote-Code-Executions oder Denial-of-Service Angriffe auszuführen.

**DevOops**         https://www.hackthebox.eu/home/machines/profile/140

[Dokumentation](04/README.md)


### 5 Fehler in der Zugriffskontrolle (Broke Access Control)

Häufig werden die Zugriffsrechte für authentifizierte Nutzer nicht korrekt um- bzw. durchgesetzt. Angreifer können entsprechende Schwachstellen ausnutzen, um auf Funktionen oder Daten zuzugreifen, für die sie keine Zugriffsberechtigung haben. Dies kann Zugriffe auf Accounts anderer Nutzer sowie auf vertrauliche Daten oder aber die Manipulation von Nutzerdaten, Zugriffsrechten etc. zur Folge haben.

**Carrier**         https://www.hackthebox.eu/home/machines/profile/155

[Dokumentation](05/README.md)


### 6 Sicherheitsrelevante Fehlkonfiguration 

Fehlkonfigurationen von Sicherheitseinstellungen sind das am häufigsten auftretende Problem. Ursachen sind unsichere Standardkonfigurationen, unvollständige oder ad-hoc durchgeführte Konfigurationen, ungeschützte Cloud-Speicher, fehlkonfigurierte HTTP-Header und Fehlerausgaben, die vertrauliche Daten enthalten. Betriebssysteme, Frameworks, Bibliotheken und Anwendungen müssen sicher konfiguriert werden und zeitnah Patches und Updates erhalten.

**Help**         https://www.hackthebox.eu/home/machines/profile/170

[Dokumentation](06/README.md)


### 7 Cross Site Scripting (XSS) (in progress)

XSS tritt auf, wenn Anwendungen nicht vertrauenswürdige Daten entgegennehmen und ohne Validierung oder Umkodierung an einen Webbrowser senden. XSS tritt auch auf, wenn eine Anwendung HTML- oder JavaScript-Code auf Basis von Nutzereingaben erzeugt. XSS erlaubt es einem Angreifer, Scriptcode im Browser eines Opfers auszuführen und so Benutzersitzungen zu übernehmen, Seiteninhalte verändert anzuzeigen oder den Benutzer auf bösartige Seiten umzuleiten.

**Holiday**         https://www.hackthebox.eu/home/machines/profile/22

**Nightmare** https://www.hackthebox.eu/home/machines/profile/122

[Dokumentation](07/README.md)

### 8 Unsichere Deserialisierung

Unsicher, weil unzureichend geprüfte Deserialisierungen können zu Remote-Code-ExecutionSchwachstellen führen. Aber auch wenn das nicht der Fall ist, können Deserialisierungsfehler Angriffsmuster wie Replay-Angriffe, Injections und Erschleichung erweiterter Zugriffsrechte ermöglichen.

**Stratosphere** https://www.hackthebox.eu/home/machines/profile/129

[Dokumentation](08/README.md)


### 9 Nutzung von Komponenten mit bekannten Schwachstellen	

Komponenten wie Bibliotheken, Frameworks etc. werden mit den Berechtigungen der zugehörigen Anwendung ausgeführt. Wird eine verwundbare Komponente ausgenutzt, kann ein solcher Angriff von Datenverlusten bis hin zu einer Übernahme des Systems führen. Applikationen und APIs, die Komponenten mit bekannten Schwachstellen einsetzen, können Schutzmaßnahmen unterlaufen und so Angriffe mit schwerwiegenden Auswirkungen verursachen. 

**Devel**         https://www.hackthebox.eu/home/machines/profile/3

**Lame** https://www.hackthebox.eu/home/machines/profile/1

**Legacy** https://www.hackthebox.eu/home/machines/profile/2

[Dokumentation](09/README.md)

### 10 Unzureichendes Logging & Monitoring

Unzureichendes Logging und Monitoring führt zusammen mit fehlender oder uneffektiver Reaktion auf Vorfälle zu andauernden oder wiederholten Angriffen. Auch können Angreifer dadurch in Netzwerken weiter vordringen und Daten entwenden, verändern oder zerstören. Viele Studien zeigen, dass die Zeit bis zur Aufdeckung eines Angriffs bei ca. 200 Tagen liegt sowie typischerweise durch Dritte entdeckt wird und nicht durch interne Überwachungs- und Kontrollmaßnahmen.

**Jerry (Bruteforce Methode)**         https://www.hackthebox.eu/home/machines/profile/144

**Nineveh**         https://www.hackthebox.eu/home/machines/profile/54

[Dokumentation](10/README.md)
