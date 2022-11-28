Einfaches Beispiel für den IBM log4j Node vom IBM IAM 3 Support Pack (https://github.com/ot4i/node-for-log4j)

Schritte: 

1) Installation des log4j Node Server Client und Server Komponenten 
   - server: par Datei in /server/jplugin ablegen 
   - Toolkit: Installation des Features in Eclipse 
2) log4J2 Properties Datei in shared-classes ablegen (Beispiel Windows: C:\ProgramData\IBM\MQSI\shared-classes)
3) Anwendung auf Server deployen  


Aktuelle Limitierungen bei ACE 12.0.6 (bekannte Issues, an den von der IBM gearbeitet wird): 
- Log4JNode: 
  - keine Verwendung vom Debug Level möglich 
  - aktuell kann kein Pfad bei den log4jnodes für die log4j2 Properties Datei mitgegeben werden 
- ESQL Logging 
  - aktuell ClassNotFoundIssues; auch die Problemlösung von https://github.com/ot4i/node-for-log4j/issues/4 hat nicht funktioniert.  
