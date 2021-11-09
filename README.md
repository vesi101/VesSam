#  1.	Labor Protokoll

Das Ziel dieser Übung war sich mit verschiedenen Softwares wie OpenHAB, Asterics, Tobii 4c und anderen auseinanderzusetzen und somit Hilfestellungen für  Menschen mit Behinderung zu ermöglichen.

## 1.1	Kurzer Überblick über diese obengenannten Softwares:

Open Home Automation Bus (openHAB) ist eine in Java entwickelte Softwarelösung, die Komponenten zur Gebäudeautomatisierung von den verschiedensten Anbietern hersteller- und protokollneutral in einer Plattform miteinander verbindet. openHAB wurde von Kai Kreuzer 2010 initiiert und hat viele Mitentwickler. (vgl. https://en.wikipedia.org/wiki/OpenHAB)

AsTeRICS ist ein kostenloser Open-Source-Baukasten für assistive Technologien (AT). Es ermöglicht die Schaffung flexibler Lösungen für Menschen mit Behinderungen unter Verwendung einer Vielzahl von Sensoren und Aktoren. 
(vgl. https://www.asterics.eu/)

Mit dem 4C von Tobii erweitert man den PC um einen voll funktionsfähigen Eye Tracker, um Spiele noch einfacher und intuitiver zu steuern.

FABI (Flexible Assistive Button Interface) ist eine Schnittstelle für den Anschluss von bis zu 9 externen Tastern (Buttons) oder selbstgemachten elektrischen Kontakten an einen Computer oder einem Smartphone. FABI ermöglicht die Steuerung des Mauszeigers und das Auslösen bestimmter Tasten durch das Drücken der Taster. Alle Funktionen können durch eine grafischer Konfigurationssoftware angepasst werden. Darüberhinaus kann FABI mit einem Drucksensor (sip/puff) erweitert werden. Ähnlich wie die FLipMouse bietet FABI mehrere Speicherplätze für verschiedene Konfigurationen, sodass AnwenderInnen diese bei Bedarf wechseln können. Das ermöglicht es, Computerspiele zu spielen, im Internet zu surfen, Emails zu schreiben und noch vieles mehr. (vgl. https://github.com/asterics/FABI)


# 2.	Kurzbeschreibung Klient:

Gerald hat eine starke körperliche Einschränkung und eine Hörbeeinträchtigung. Er ist auf Pflege angewiesen und kann Klänge wahrnehmen. Er würde gerne eine gewisse Autonomie zurückerlangen und seine Umgebung (z.B. Licht, Jalousien, Musik) steuern können. Darüberhinaus würde er gerne Klänge/Visuals erzeugen können und sich die Zeit mit Computerspielen vertreiben. Er möchte gerne im Internet surfen oder am Smartphone mit seinen Freunden kommunizieren können.


**Vorhandene Funktionen**

* 	rechter Arm leicht heben/senken (keine Handfunktion)

* 	große Zehe links 
* 	Kopf 
* 	Mund/Lippen
* 	Saugen/Pusten
* 	Augen
*  non-verbal


## 2.1. Aufgabenstellung: 
Aufgabe ist die Entwickung von individuellen Unterstützungstechniken für eine gewählte KlientInnenbeschreibung.

**Wunsch:**
 
* Steuerung Licht und Temperatur/Jalousien und Fernseher/Musikanlage 
Computer 

* Internet surfen
* E-Mail schreiben 
* Computerspiel spielen


SmartPhone bedienen 
*	SMS schreiben 
*	Anruf tätigen




# 3.	 Steuerung Licht und Temperatur/Jalousien 

Es gibt viele verschiedene Arten von Vergünstigungen für Menschen mit Behinderungen. Eine Vereinfachung wurde mit Asterics Grid mithilfe der Software openHAB durchgeführt. 

Verwendet wurden lokale openHAB Items des Smart-Living-Lab an der FH-Technikum Wien, welche zur Verfügung gestellt, welche ins Asterics Grid integriert wurden. Der Arbeitsbereich war die Küche in der man Gerald ermöglichen musste die Beleuchtung sowie Temperatur und Jalousien steuern zu können. 


## 3.1. Allgemeine Information zu Asterics Grid:

AsTeRICS Grid ist ein User-Interface, welches die smarte Steuerung in verschiedenen Bereichen ermöglicht. Man kann es nach jeglichen Nutzerbedürfnissen anpassen indem man einzelne Elemente im Grid erstellt. (vgl. https://www.asterics-foundation.org/projekte-2/asterics-ergo-grid-2/)

## 3.2. die Steuerung mithilfe von Asterics Grid und Openhab:

1. Neues Grid erstellt.
2. Licht-, Temperatur- (inklusive zusätzlichem Grid mit Solltemperaturen von 15, 20 und 25˚C) und Jalousien-Elemente wurden erstellt.
3. AsTeRICS Action wurde hinzugefügt.
4. In einem zusätzlichen Fenster wurde das ARE Projekt vom Smart-Living-Lab geöffnet und das ARE Modell wurde ins AsTeRICS Grid gedownloadet.
5. Als 'Komponente' openHAB.1_c ausgewählt.
6. Als 'Port' actionString ausgewählt.
7. Bei 'Daten' wurde der Teil der Küche und die jeweilige Operation (ON/OFF) hinzugefügt (openHAB des gewünschten Smart-Living-Lab Item)


**Allgemeines Grid:**
![Screen Shot 2021-11-09 at 10 55 58 AM](https://user-images.githubusercontent.com/93941670/140909680-89683cbb-486a-4d1a-a36f-59e165adb223.png)

**Extra Grid für Temperatur:**
![Screen Shot 2021-11-09 at 11 44 05 AM](https://user-images.githubusercontent.com/93941670/140910133-6d993801-2119-4aba-a1ef-15356e31c814.png)

**Asterics action für Smart Home mithilfe von openHAB**
![Screen Shot 2021-11-09 at 11 55 21 AM](https://user-images.githubusercontent.com/93941670/140911681-0d78dd2f-0b74-46bf-abad-4037db6c2de1.png)



# 4.	Computer
Ein Leben ohne Internet ist kaum mehr vorstellbar. Shoppen, Reisen und Kulturevents buchen, sich informieren, etc. Immer mehr alltägliche Handlungen finden über das Internet statt. Trotzdem ist das Internet nicht für alle auf gleicher Art und Weise zugänglich.
Personen mit Beeinträchtigung wollen auch ihre Zeit im Internet verbringen. Sie wollen vielleicht nicht vieles aber beispielsweise ein Mail schreiben zu können, Musik  zu hören oder etwas recherchieren. 

Da Gerald eine starke körperliche Einschränkung hat, wurde die Steuerung der Maus mit zwei Eingabegeräten, einerseits dem Eye–Tracker und andererseits dem Fabi (Flexible Assistive Button Interface) ermöglicht. 

## 4.1. Was ist der Eye – Tracker?
Ein Eyetracker ist ein Gerät, das mittels einer Kamera Augenbewegungen verfolgt und sie mithilfe einer Software in Bewegungen des Mauszeigers auf dem Computerbildschirm überträgt („Augensteuerung“).
In der Unterstützten Kommunikation (UK) ist der Eyetracker häufig bereits in den Computer integriert, und das Gerät ist bereits mit der entsprechenden Anwendungs-Software ausgestattet. (vgl. https://gaming.tobii.com/product/eye-tracker-5/)



Mit Click2Speak gibt es ein weiteres, freies und kostenloses Programm, die für die Benutzung mit einem Eyetracker optimiert wurde und welches auch im Zuge des Projekt in Verwendung genommen wurde. 



## 4.2. Was ist Click2Speak?



Click2Speak ist eine kostenlose Bildschirmtastatur, die für die Benutzung mit einer Augen- oder Kopfsteuerung konzipiert ist. Man kann damit komfortabel schreiben, ohne seine Arme verwenden zu müssen. Darüber hinaus verfügt das Programm über eine Vielzahl weiterer Funktionen zur allgemeinen Computersteuerung.
Hier gibt es der Link zum kostenlosen Downloaden. (https://www.click2speak.net/)

![click2speak](https://user-images.githubusercontent.com/93941670/140919961-298ad92c-da47-49ba-816d-c6ca891fdff5.jpeg)

**Schnellübersicht Hauptfenster Click2Speak** 
(siehe Screenshot im 'Photos' Ordner)	 

1. Alarmbutton 

2. Einstellungen 

3. Schnelleinstellungén für Größe und Position 
4. Sprachausgabezeile (7) ausblenden (zum Schreiben in Dokumente) 

5. Bereiche für Maus bzw. Windowssteuerung abtrennen 

6. Fenster verschieben

7. Texteingabezeile für TTS (Sprachausgabe) 

8. Wortvorschläge 

9. Bereich mit Windows-Funktionen 

10. Bereich mit Maus-/Klick-Funktioen

Die zusätzlichen Einstellungen im Click2Speak ermöglichte weitere Vereinfachungen wie beispielsweise das Dwell Clicking: 
Click2Speak benutzt das sogenannte Dwell-Clicking, hier mit Verweilzeit übersetzt, zum Klicken, beziehungsweise die Auswahl zu tätigen. Dabei muss der Nutzer den Mauszeiger eine bestimmte Zeit über einer Schaltfläche halten, wodurch das System automatisch einen Linksklick auslöst.
Durch die Verwendung vom Eye-Tracker mit Click2Speak wurde die Bedienung der Tastatur und der Maus vereinfachte, womit Gerald ein Mail schreiben oder im Internet surfen kann. 


## 4.3. Computerspiel Spielen:
Für die Unterhaltung wurde das Spiel 'Tap Tap Parking' gewählt.

![Screen Shot 2021-11-09 at 2 48 45 PM](https://user-images.githubusercontent.com/93941670/140935821-8077dbcd-598b-4ac7-bb8f-9b61d4d172d5.png)

kurze Beschreibung des Spieles: 

Bei diesem Spiel geht es um das richtige Parken des Autos bzw. der Autos in die Parklücke. Das Auto fährt mit hoher Geschwindigkeit und man muss mit einem Klick auf die Maus den richtigen Moment finden um die Parklücke zu erwischen. Im ersten Level macht man dies mit einem Auto, weitere Levels werden immer schwieriger.


Warum wurde dieses Spiel ausgesucht? 

Da der Patient eine schwere köperliche Einschränkung hat und nur seine rechte Hand sowie die linke Zehe bewegen kann, wurde ihm somit ermöglicht trotzdem Spaß am Computer haben zu können. 

Das Klicken der Maus wird mit Fabi kontrolliert und der Cursor wird mit dem Eye-Tracker gesteuert.



# 5.	SmartPhone bedienen 

**App:** Microsoft Your Phone

**Gerät:** Android


![yourphone](https://user-images.githubusercontent.com/93941670/140919596-d908633c-707b-4f93-a971-b6da27088f46.jpeg)

**Am Laptop einstellen:**

1. In Systemeinstellungen das Untermenü 'Telefon' öffnen. 
2. Handy hinzufügen.
3. 'Your Phone' App wird geöffnet und das Handy wird über Bluetooth mit dem Laptop verbunden. 


**Am Handy einstellen:**

1. Bluetooth einschalten.
2. 'Your Phone Companion' runterladen und öffnen (QR-Code vom Laptop scannen).
3. Handy wird automatisch verbunden.
4. App erlauben auf Nachrichten, Anrufe und alles was man verwenden möchte zuzugreifen. 

(vgl.https://support.microsoft.com/en-us/topic/your-phone-app-requirements-and-set-up-cd2a1ee7-75a7-66a6-9d4e-bf22e735f9e3)


# 6.	GoFitts

Mithilfe von dem FittsTask2D kann man das Pfaddiagramm von den unterschiedlichen Eingabemethoden testen. Es wurden also Eye-Tracker und Fabi getestet. 


**Hier sind die Resultate der FittsTask mit Fabi und Tobii.**

 **Tobii Ergebnis**
![Tobii](https://user-images.githubusercontent.com/93941670/140918635-b2882790-2ba6-499f-a0c6-60c3d56e818c.jpeg)

**Keyboard Ergebnis**
![keyboard](https://user-images.githubusercontent.com/93941670/140918889-d46bc782-44d5-40e8-8484-b6ae19c63e6f.jpeg)

**Fabi Ergebnis**
![fabi](https://user-images.githubusercontent.com/93941670/140919010-1d59cd22-310d-461a-9205-99d4b40e7d7f.jpeg)



























