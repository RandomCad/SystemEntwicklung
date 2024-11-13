# Storyboard zum DRC
Im Kontext dieses Storyboards ist abzuklären, in welchem Kontext die Software verwendet wird und welche Personen als Kunden angesehen werden.  
Das DRC ist Bestandteile einer Maschine welche von der *ruhlamat GmbH* hergestellt wird. 
Das DRC sammelt Statistikdaten und speichert diese langfristig. 
Hierzu muss das DRC hauptsächlich mit der SPS der Maschine kommunizieren, da nur diese dazu fähig ist Statistikdaten zu sammeln.  
Aus diesem Grund gibt es folgende Kunden für das DRC:
* Bediener der Maschine/Endkunde
* SPS Entwickler
* Inbetriebnehmer
* ruhlamat GmbH  

Der Inbetriebnehmer wird ebenfalls als Kunde angesehen, da dieser ohne Veränderung am DRC selbst das DRC an die Maschine anpassen soll.
## Board

|Bedingung                    |Konfiguration                 |Fehlerverhalten                  |
|:---------------------------:|:-----------------------------:|:-------------------------------:|
|Durch eine einfache graphische Oberfläche kann eingestellt werden, ob Daten gesammelt werden oder nicht. |Der Speicherort von Daten in der SPS ist einfach einstellbar.|Im Fehlerfall wird ein eindeutiger Fehlercode angegeben. |
|                             |                               |                                 |
|Die Existenz des DRC ist im Normalgebrauch der Maschine nicht zwingend erforderlich. |Der Speicherort der gesammelten Daten ist einfach und schnell veränderbar.|Eine umfangreiche Beschreibung von Fehlercodes liegt vor.|
|Das Programm erscheint ein Bestandteil der Maschine zu sein. |                               |                                 |
|                             |                               |                                 |
|Durch eine einfache graphische Oberfläche ist das Drucken der Statistikdaten möglich. |Eine Anpassung an andere Maschinen ist schnell möglich.|Der Umfang an Fehlerinformationen ist in der Inbetriebnahme hörbar.|
|Als Benennung für die Speicherdatei ist jeglicher Name möglich. |Es ist möglich, die Benennung der Daten in der Speicherdatei zu verändern. |Das DRC gibt Fehler im Druckprozess an.|
|                             |                               |                                 |
|                             |Die Namensveränderung in der Speicherdatei ist dynamisch möglich. |                                 |

|Drucken                      |Datei Speicherformate          |SPS-Kommunikation                |
|:---------------------------:|:-----------------------------:|:-------------------------------:|
|Das DRC ermöglicht das automatische Drucken der erzeugten Statistikdaten. |Die Daten sind im CSV-Format speicherbar.|Die Kommunikation erfolgt bidirektional.|
|Es ist möglich, die Daten nicht zu drucken, sondern nur zu speichern. |                               |Die Kommunikation erfolgt in einer für die SPS verständlichen Codierung.|
|Das DRC ist auch ohne angebundene Druckersoftware funktionsfähig. |                               |                                 |

