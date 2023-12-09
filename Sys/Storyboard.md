# Storyboard zum DRC
Im kontext dieses Storyboards ist abzuklären, in welchem Kontext die Software verwendet wird und welche Personen als Kunden angesehne werden.  
Das DRC ist bestandteile einer Maschine welche von der *ruhlamat GmbH* hergestellt wird. 
Das DRC smmelt Statistickdaten und speichert diese langfristig. 
Hierzu muss das DRC hauptsächlich mit der SPS der Maschine komunizieren, da nur diese dazu fähig ist Statistick daten zu sammeln.  
Aus diesem grund gibt es folgende Kunden für das DRC:
* Bediner der Maschine/Endkunde
* SPS entwickler
* Inbetriebnehmer
* ruhlamat GmbH  

Der Inbetriebnehmer wird ebnfals als Kunde angesehn, da dieser ohne veränderung am DRC selbst das DRC an die Maschine anpassen soll.
## Board

|Bedinung                     |Konfiguration                  |Fehlerverhalten                  |
|:---------------------------:|:-----------------------------:|:-------------------------------:|
|Durch eine Simple Graphische-|Der speicherort von Daten in   |Im fehlerfall wird ein           |
|Oberfläche kann eingestellt  |der SPS ist einfach einstellbar|eindeutiger fehlercode angegeben |
|werden ob Daten gesammlt     |                               |                                 |
|werden                       |                               |                                 |
|                             |                               |                                 |
|Die existenz des DRC ist im  |Der Speicherort der Gesamelten |Eine umfangreiche beschreibung   |
|Normalgebrauch des Maschine  |Daten ist einfach und schnell  |von Fehlercodes leigt for        |
|nicht zwingend erischtlich.  |             veränderbar       |                                 |
|Das Programm erscheint ein   |                               |                                 |
|bestandteil der Maschine zu  |                               |                                 |
|sein                         |                               |                                 |
|                             |                               |                                 |
|Durch eine Simple Graphische-|Eine anpassung an andere       |Der umfang an fehler             |
|Oberfläche ist das Drucken   |Maschine ist schnell möglich   |informationen ist in der         |
|der Statistickdaten möglich  |                               |Inbetriebnahme erhörbar          |
|                             |                               |                                 |
|Als Benenung für die         |Es ist möglich die Benenung der|Das DRC gibt Fehler im           |
|Speicherdatei ist jeglicher  |Daten in der Speicherdatei zu  |Druckprozess an                  |
|Name möglich                 |verändern                      ||
|                             |                               |                                 |
|                             |Die namens veränderung in der  ||
|                             |Speicherdatei ist Dynamisch    ||
|                             |möglich                        ||
|                             |                               |                                 |
  
  




|Drucken                      |Datei Speicherformate          |SPS-Kommunikation                |
|:---------------------------:|:-----------------------------:|:-------------------------------:|
|Das DRC ermöglicht das       |Die Daten sind in CSV Format   |Die kommunikation erfolgt        |
|Automatische drucken der     |Speicherbar                    |Bidirektional                    |
|erzeugten Statistick Daten   |                               ||
|                             |                               ||
|Es ist möglich die Daten     |                               |Die komunikation erfolgt in einr |
|nicht zu Drucken sondern     |                               |für die SPS verständlichen       |
|nur zu speichern             |                               |Codierung                        |
|                             |                               |                                 |
|Das DRC ist auch ohne        |||
|angebundene Druckersoftware  |                               ||
|Funktionsfähig               |||
|                             |                               |                                 |
