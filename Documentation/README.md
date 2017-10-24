# Dokumentation Assignment 3

Im Folgenden kurz die Zusammenfassung unserer Ergebnisse zum Assignment 3

## Statischer Aufbau

Anhand des Graphen unten, können folgene Teile geclustert werden:

* Catalina
* Catalina_tribes
* jasper
* el
* coyote
* jk
* org_apache

![Graph of tomcat components](architecture_summary.pdf)

### Dynamischer Aufbau

Um den Ablauf eines Request zu verstehen, habe wir erstmal bei verschiedenen Http Klassen einen Breakpoint gesetzt, bis einer bei einem Request angehalten wurde. Durch den Stacktrace und das weitere Debuggen von diesem Punkt hat sich folgender Verlauf ergeben:


| Klasse | Beschreibung |
| -------|:------------:|
| JIoEndpoint | Handle incoming TCP connections. |
| Http11Protocol| Abstract the protocol implementation, including threading, etc.|
| http11Processor|Process pipelined HTTP requests on the specified socket.|
| CoyoteAdapter | Implementation of a request processor which delegates the processing to a Coyote processor.|




