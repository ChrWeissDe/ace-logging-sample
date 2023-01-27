Einfaches Beispiel für den IBM log4j Node vom IBM IAM 3 Support Pack (https://github.com/ot4i/node-for-log4j)

Für die Installation vom Node innerhalb vom Toolkit bitte der offiziellen Dokumentation folgen. 

Für das Setup der Runtime (Integration Node / Integration Server) sind folgende Schritte notwendig

1.) Cleanup der folgenden Verzeichnisse - löschen aller IAM 3 relevanten Dateien (par, jars, log4j2 configs etc.) 
- <MQSI\shared-classes> - Beispiel C:\ProgramData\IBM\MQSI\shared-classes
- <ACE-INSTALL\server\classes> - Beispiel C:\Program Files\IBM\ACE\12.0.6.0\server\classes
- shared-classes Verzeichnis vom Integration Server 

2.) Entpacken der Log4jLoggingNode_v2.0.1.par Datei in ein temproräres Folder 
3.) Kopieren der folgenden Dateien aus dem Unterverzeichnis \lib in <MQSI\shared-classes> (Beispiel C:\ProgramData\IBM\MQSI\shared-classes) 
- jakarta-oro-2.0.8.jar 
- log4j-api-2.17.1.jar 
- log4j-core-2.17.1.jar 

4.) Erstellung einer neuen Log4jLoggingNode_v2.0.1.jar Datei 
- Erstellung einer neuen jar Datei (zip) innerhalb vom ausgepackten "classes Verzeichnis"; Inhalt der zip Datei: Verzeichnis org und META-INF 
- Bennenung der jar Datei: Log4jLoggingNode_v2.0.1.jar Datei  

5.) Kopieren der neuen Log4jLoggingNode_v2.0.1.jar Datei nach: 
<MQSI\shared-classes> - Beispiel C:\ProgramData\IBM\MQSI\shared-classes
<ACE-INSTALL\server\classes> - Beispiel C:\Program Files\IBM\ACE\12.0.6.0\server\classes




Aktuelle Limitierungen bei ACE 12.0.6 (bekannte Issues, an den von der IBM gearbeitet wird): 
- Log4JNode: 
  - keine Verwendung vom Debug Level möglich 
  - aktuell kann kein Pfad bei den log4jnodes für die log4j2 Properties Datei mitgegeben werden 
- ESQL Logging 
  - aktuell ClassNotFoundIssues; auch die Problemlösung von https://github.com/ot4i/node-for-log4j/issues/4 hat nicht funktioniert.  
