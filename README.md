# II2004 – Praktikum Eingebettete Systeme (PES)

Willkommen im Material-Repository zum **Praktikum Eingebettete Systeme (II2004)** an der THM.

Dieses Repository enthält die **Praktikumsanleitung, Aufgabenblätter, Datenblätter, Schaltpläne und ergänzende Literatur**, die ihr im Laufe des Praktikums benötigt.

> **Wichtig:** Organisatorische Informationen, Termine, Anwesenheitspflicht und Abgabefristen werden im **Moodle-Kurs** veröffentlicht. Im Zweifel ist Moodle für Termine und organisatorische Vorgaben maßgeblich.

## Schnellstart

1. **Moodle-Kurs lesen:**  
   https://moodle.thm.de/course/view.php?id=4988
2. **Dieses Repository lokal klonen** oder regelmäßig auf GitHub öffnen.
3. Mit der **Praktikumsanleitung** beginnen:  
   [Praktikumsanleitung-PES.pdf](./Praktikumsanleitung-PES.pdf)
4. Das aktuelle Aufgabenblatt unter [Aufgabenblaetter](./Aufgabenblaetter/) bearbeiten.
5. Benötigte Datenblätter und Schaltpläne unter [Resourcen](./Resourcen/) nachschlagen.
6. Ergänzende Hintergrundinformationen findet ihr unter [Begleitende_Literatur](./Begleitende_Literatur/).

## Repository-Struktur

```text
materialien_neu/
├── README.md
├── Praktikumsanleitung-PES.pdf
├── Aufgabenblaetter/
│   ├── abgabe1.pdf
│   ├── abgabe2.pdf
│   ├── abgabe3.pdf
│   ├── abgabe4.pdf
│   └── abgabe5.pdf
├── Resourcen/
│   ├── Board- und Erweiterungsboard-Schaltpläne
│   ├── STM32-Datenblatt und Reference Manual
│   ├── HAL-Dokumentation
│   └── Sensor-/Baustein-Datenblätter
└── Begleitende_Literatur/
    └── weiterführende Literatur
```

## Aufgabenblätter

Die fünf Aufgabenblätter findet ihr im Ordner [Aufgabenblaetter](./Aufgabenblaetter/).

| Abgabe | Thema |
|---|---|
| [Abgabe 1](./Aufgabenblaetter/abgabe1.pdf) | Einführung, GPIO und LCD |
| [Abgabe 2](./Aufgabenblaetter/abgabe2.pdf) | ADC und DMA |
| [Abgabe 3](./Aufgabenblaetter/abgabe3.pdf) | Timer und NVIC |
| [Abgabe 4](./Aufgabenblaetter/abgabe4.pdf) | Projekt 1 – Lüfterregelung |
| [Abgabe 5](./Aufgabenblaetter/abgabe5.pdf) | Projekt 2 – Wetterstation |

Lest zu jeder Abgabe **zuerst das vollständige Aufgabenblatt** und verwendet die Praktikumsanleitung sowie die Dokumente unter `Resourcen/` zum Nachschlagen.

## Wichtige technische Dokumente

Unter [Resourcen](./Resourcen/) liegen unter anderem:

### Entwicklungsplattform

- [STM32F429 Datasheet](./Resourcen/STM32F429-Datasheet.pdf)  
  Pinbelegung, elektrische Eigenschaften und Alternate Functions des Mikrocontrollers.
- [STM32F4 Reference Manual](./Resourcen/STM32F4-Reference-Manual.pdf)  
  Detaillierte Beschreibung der Peripherie und Register. Dies ist eine der wichtigsten Quellen für die praktische Arbeit.
- [Cortex-M4 Programming Manual](./Resourcen/STM32_Cortex-M4_MCUs_and_MPUs_programming_manual.pdf)  
  Informationen zum Cortex-M4-Kern.
- [STM32F429 Discovery Kit User Manual](./Resourcen/discovery-kit_user-manual.pdf)  
  Dokumentation des STM32F429 Discovery Boards.
- [Open429Z-D User Manual](./Resourcen/Open429Z-D-UserManual.pdf)  
  Dokumentation des im Praktikum verwendeten Erweiterungsboards.
- [Open429Z-D Schematic](./Resourcen/Open429Z-D-Schematic.pdf)  
  Schaltplan des Open429Z-D – besonders wichtig, wenn ihr herausfinden müsst, an welchen MCU-Pins eine Komponente angeschlossen ist.
- [CubeHAL Description](./Resourcen/CubeHAL-description.pdf)  
  Referenz zur STM32 HAL.

### Erweiterungsboards und Sensoren

- [8-Segment-Board – Schaltplan](./Resourcen/8-SEG-LED-Board-Schematic.pdf)
- [Analog Test Board – Schaltplan](./Resourcen/Analog-Test-Board-Schematic.pdf)
- [BME280 – Schaltplan](./Resourcen/BME280-Environmental-Sensor-Schematic.pdf)
- [BME280 – Datenblatt](./Resourcen/BME280_datenblatt.pdf)
- [L3GD20 – Datenblatt](./Resourcen/L3GD20_datenblatt.pdf)
- [WS2812B – Datenblatt](./Resourcen/WS2812B_Datasheet.pdf)
- [Understanding the I²C Bus](./Resourcen/Understanding_the_I2C_bus.pdf)

## Welche Quelle benutze ich wofür?

Als Faustregel:

| Fragestellung | Sinnvolle Quelle |
|---|---|
| Was ist in der Aufgabe gefordert? | aktuelles Aufgabenblatt |
| Wie soll der Code im Praktikum strukturiert sein? | Praktikumsanleitung |
| Welcher MCU-Pin ist mit einer Komponente verbunden? | Board-Schaltplan |
| Welche Alternate Function hat ein STM32-Pin? | STM32F429 Datasheet |
| Wie funktioniert ADC, DMA, Timer, GPIO, I²C usw. im Detail? | STM32F4 Reference Manual |
| Welche HAL-Funktion bzw. Struktur wird benötigt? | CubeHAL Description / HAL-Quellcode |
| Wie verhält sich ein Sensor oder externer Baustein? | jeweiliges Datenblatt |

**Tipp:** Gewöhnt euch daran, technische Aussagen mit der passenden Primärquelle zu überprüfen. Genau diese Fähigkeit – Datenblatt, Schaltplan und Reference Manual gezielt zu benutzen – ist ein wesentlicher Teil des Praktikums.

## Repository lokal verwenden

Wir verwenden in diesem Semester **GitHub (github.com)** und nicht die THM-GitLab-Instanz.

### Klonen mit Git

```bash
git clone https://github.com/thm-pes/materialien_neu.git
cd materialien_neu
```

Spätere Aktualisierungen holt ihr mit:

```bash
git pull
```

Alternativ könnt ihr das Repository über **EGit in STM32CubeIDE** klonen und aktualisieren.

> Dieses Repository dient der Bereitstellung der **gemeinsamen Kursmaterialien**. Eure eigenen Übungs- und Projektabgaben erfolgen in den dafür vorgesehenen bzw. euch zugewiesenen GitHub-Repositories. Beachtet dazu die Angaben im Moodle-Kurs.

## Arbeiten mit GitHub im Praktikum

Für das Praktikum benötigt ihr einen kostenlosen Account auf **https://github.com/**.

Die GitHub-Organisation des Praktikums findet ihr unter:

**https://github.com/orgs/thm-pes**

Achtet darauf, dass ihr euren GitHub-Benutzernamen kennt und Zugriff auf die euch zugewiesenen Repositories habt.

### Bei Abgaben beachten

Die verbindlichen Details stehen in Moodle. Grundsätzlich werden **Code und PDF-Dokumentation per GitHub-Tag** abgegeben. Achtet daher insbesondere darauf, dass

- alle relevanten Änderungen **committet** wurden,
- die Commits zu GitHub **gepusht** wurden,
- der geforderte **Tag auf dem richtigen Commit** liegt und
- der Tag ebenfalls zu GitHub **gepusht** wurde.

Kontrolliert eure Abgabe anschließend direkt auf github.com.

## Empfohlene Arbeitsweise

1. Aufgabenstellung vollständig lesen.
2. Problem in sinnvolle Software-Module zerlegen.
3. Benötigte Pinbelegungen im Schaltplan prüfen.
4. Peripherie im Datasheet/Reference Manual nachvollziehen.
5. Implementierung schrittweise entwickeln und testen.
6. Compiler-Warnungen beseitigen.
7. Code nachvollziehbar dokumentieren.
8. Änderungen regelmäßig committen und pushen.
9. Vor dem Fachgespräch sicherstellen, dass **jedes Teammitglied den Code erklären kann**.
10. Nach dem Fachgespräch die finale Version einschließlich Dokumentation fristgerecht taggen und pushen.

## Software

Für das Praktikum verwenden wir insbesondere:

- **STM32CubeIDE**
- **EGit** / Git-Integration der IDE
- **GitHub**

Installationshinweise und weitere organisatorische Informationen findet ihr im Moodle-Kurs.

## Kommunikation und Fragen

Organisatorische Informationen und Ankündigungen findet ihr in **Moodle**.

Für fachliche Fragen außerhalb der Praktikumszeiten steht außerdem der THM-Connect-Raum zur Verfügung:

**#praktikum-eingebettete-systeme**  
https://matrix.to/#/#praktikum-eingebettete-systeme:thm.de

Wenn ihr eine Frage zu eurem Code stellt, beschreibt möglichst:

- was ihr erreichen wollt,
- was ihr bereits ausprobiert habt,
- welches Verhalten ihr erwartet,
- welches Verhalten tatsächlich auftritt und
- welche Fehlermeldungen oder Messwerte ihr beobachtet.

So können euch Kommiliton:innen und Betreuende deutlich schneller helfen.

## Hinweise zu Aktualisierungen

Die Materialien können während des Semesters aktualisiert werden. Prüft daher regelmäßig:

```bash
git pull
```

bzw. synchronisiert das Repository über EGit.

---

**II2004 – Praktikum Eingebettete Systeme**  
Technische Hochschule Mittelhessen (THM)
