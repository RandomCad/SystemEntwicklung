# Microservice Architectur für eine Vertigungsanlage  
Im falle einer vertigungs anlage muss ein Komplexer Produktionsablauf durchgeführt werden. Die folgenden betrachtungen erfolgen dabei auf basis eines Hypotetischen konzeptes für eine Passpersonaliesierungsmaschine.  
## Aufgabe der Maschine  
Aufgabe einer Passpersonaliesierungsmaschine im folgenden Personaliesierungsmaschine benant ist es einen Vertiges Pass dokument weiter zu Personaliesieren.  
Ein Dokument (Pass) wird im geschlossenen zustand auf der einen Seite in die Maschine eingeführt und soll auf der anderen seite voll Personalieseirt in einem Geschlossenen Zustand ausgespendet werden. Die einführung und auspendung erfolgt in vertikalen _kontianern_.  
## Aufbau der Maschine  
Die Maschine soll aus mehreren stationen bestehen, welche unterschiedliche aufgaben erfüllen. Für unsere betrachtung sind alle Actoren und Sensoren der Maschine relvant. Die Actoren können durch die Softwar zu einer Bewegung gebracht werden, wärend Snsoren werte an die Software Lievern können. Ein bauteil kann sowohl aus einem Actor als auch aus einem Sensor bestehen.  
Grundsetzlich muss die Bewegung der Maschine gesteuert werden. Typischerweise wird hierfür eine oder in Komplexen maschinen auch mehrer SPS'n verwendet um die Werte der SEnsoren auszulehsen und die Actoren entsprechend zu bewegen. Es gibt demnach eine Zentralle rechenkomponente und einen Monolitischen aufbau des Programmes.  
Um eine steuerung für eine solche Maschine in form von Microserfices umzusetzen muss dieses Hauptprogramm in mehrere Bestandteile aufgeteilt werden. Dabei können folgende Schritte genommen werden:  
1. Jede **Station** erhält ein eigenens Programm. Dieses gibt die zu befolgenden Abrebeitschritte in dieser station an. Da jede station ein eigenes Programm erhält wäre es möglich dies auf dedizierten chips für jede Station einzelnd auszuführen.  
2. Jede **Baugruppe** in einer station erhält eine eigenen programierung. Eine Baugruppe ist grundsetzlich ein Zusammenschluss von mehreren bestandteilen der Maschine. In gewisser weise wird jede Station in weitere Substationen unterteilt. Diese erhalten ihre eigenen Programierung und im bestenfalle auch eigene Rechenchips.
3. Jeder **Actor** und **Sensor** erhält eine eigenes Programm und dedizierte Hardwäre. Dies ist nicht dringend untypisch. Dabei besitzen insbesondere größere motoren rechtheufig dedizierte Hardare, auf welchen dedizierte Software zur steuerung läuft. Es ist aber untypisch dies für jeden einzelnen senso und Zylinder umzusetzen.
## Betrachtung der Ansätze
Im grundkonzept ohne Microserfic wird spezialisierte Hardware und software zur steurung verwendet. Diese hardawre ist vergleichsweise teuer aber für diese anwendung gedacht.  
### Microservic auf ebene von Stationen
Die umsetzung der Steuerung auf stationsebene ist grundsetzlich nicht unüblich und wird insbesondere dann verwendet, wenn die Komplexität der einzelnen Stationen recht hoch ist. In diesem falle erscheint die aufteilung des REchenaufwandes sinnvoll. Eine einzelne SPS könnte die gesamte Maschine warsccheinlich schlecht steuern. Gleichzeitig wird hierbei der Sinn eines Microservices nicht erreicht, da jede Station so komplex ist, dass sie eine eigens Monolitysche software benötigt.  
Im falle unserer Passmaschine sind einzelne Stationen eigentlich nicht so komplex, dass diese nicht von einem Zentralen gerät gestuert werden können. Die aufteilung der Rechenarbeit auf die Einezlen Stationen ist demnach nicht nötig und es findet eine vereinfachung der Programmteile stat.  
Es wäre sinnvoll eine Aufteilung des Programmes in einzelne Module für die einzelnen Stationen umzusetzen. Dies solten aber immer noch auf einem Gerät ausgeführt werden. Dies liegt hauptsechlich daran, dass die Programme der einzelne Stationen immernoch besondere Harxware benötigen und es aus Ekonomischer sich sinnvoller ist eine SPS gut auszulasten als viele wenig ausgelastet SPS zu haben. Außerdem geschtaltet sich die Komunikation zwischen den Stationen einfacher. Dies ist insbesnodere für Echtzeit kreitereien wichtig, auf welche später weiter eigegeange werden soll.  
Es ist demanch sinnvoll eine Microserficartige softwararchitectur auf ebene von Stationen für eine solche Maschine umzusetzen.
### Microservic auf ebene von Baugruppen
Soll auf eben von Baugruppen eine Microservic Architectur umgesetzt werden muss folgendes beachtet werden:  
1. Jede baugruppe solte ein eigense verarbeitungs gerät erhalten. Es wird darauf gehofft, dass die Verarbeitung der Aufgaben einzelner Baugruppen so einfach ist, das hierfür nur wenig rechenkapazität benötigt wird.  
2. Die Baugruppen müssen miteinander verbunden werden.
3. Ein komunikationsstandart zwischen den Baugruppen muss entwickelt werden  
Aufgabe eines Baugruppen rechners ist die Verareitung aller singale der Sensoren, welche zur baugruppe gehören, sowie die Steuerung aller Actoren der Baugruppe. Dabei muss jede Baugruppe anforderungen von anderen Baugruppen befolgen, welche eine Bewegung von der Baugruppe fordern, sowie die verarbeiteten signale der Sensoren weitergeben, wenn diese von anderen Baugruppen benötigt werden.  
Ein Probelem der Abklärung von zuständigkeiten entsteht. Wer darf wem sagen, was dieser tuhen soll. 

Tatsechlich werden die einzlnen statione selbst in einem Monolitartigen Programm unabhängig von einander Programiert. 



die Beweglichen teile der Maschine relevant. Alle statischen können nbeinflusst werden und sind damit aus softwarsicht  irrelevant
>Jede station kann als erster Microservic verwendet werden  
Dabei erhält jede station einen eigenen Controler, welcher den ablauf an dieser station durchführt. 
