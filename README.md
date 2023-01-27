Einfaches Beispiel für den IBM log4j Node vom IBM IAM 3 Support Pack (https://github.com/ot4i/node-for-log4j)

## Setup der Log4J2 Funktionen im Toolkit 
- bitte der offiziellen Dokumentation des IAM 3 Support Packs folgen. 

## Setup der Log4J2 Funktinalität in der Runtime (Integration Node / Integration Server) 
Folgende Schritte sind notwendig: 

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

