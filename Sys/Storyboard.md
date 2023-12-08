# Storyboard zum DRC
Im kontext dieses Storyboards ist abzuklären, in welchem Kontext die Software verwendet wird und welche Personen als Kunden angesehne werden.  
Das DRC ist bestandteile einer Maschine welche von der *ruhlamat GmbH* hergestellt wird. 
Das DRC smmelt Statistickdaten und speichert diese langfristig. 
Hierzu muss das DRC Hauptsechlich mit der SPS der maschine komunizieren, da nur diese dazu fähig ist Statistick daten zu sammeln.  
Aus diesem grund gibt es folgende Kunden für das DRC:
* Bediner der Maschine/Endkunde
* SPS entwickler
* Inbetreibnehmer
* ruhlamat GmbH  

Der Inbetriebnehmer wird ebnfals als Kunde angesehn, da dieser ohne veränderung am DRC selbst das DRC an die Maschine anpassen soll.
## Board

|Bedinung                     |Kunfiguration                  |Fehlerverhalten                  |
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
|der Statistickdaten möglich  |                               |Inbetriebnahme erhoebar          |
|                             |                               |                                 |


|Drucken                      |
|:---------------------------:|
|Das DRC ermöglicht das       |
|Automatische drucken der     |
|erzeugten Statistick Daten   |
