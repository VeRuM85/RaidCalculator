RAID-Rechner
Ein interaktives Tool zur Berechnung von Speicherkapazitäten für verschiedene RAID-Konfigurationen.
Funktionalität

Festplattenwahl: Auswahl zwischen HDD (20-1 TB) und SATA SSD (16-0.48 TB).
Festplatten-Slots: Bis zu 12 Festplatten können hinzugefügt werden.
Hot Spares: Konfigurierbare Anzahl an Ersatzfestplatten.
RAID-Typen: Unterstützt RAID 0, 1, 5, 6, 10 und JBOD.
Berechnung: Zeigt nutzbaren Speicher, Paritätsdaten, reservierten und ungenutzten Speicherplatz an.
Visualisierung: Balkendiagramme für Speicheraufteilung pro RAID-Typ.
Interaktivität: Tabs für HDD/SSD, Zurücksetzen-Funktion, Dropdown für zusätzliche RAID-Typen.

Dateistruktur

index.html: Hauptseite mit HTML, CSS und JavaScript.
HTML: Struktur für Tabs, Festplatten-Slots, Eingabefelder und Diagramme.
CSS: Styling für Layout, Tabs, Slots, Balkendiagramme und Buttons.
JavaScript: Logik für:
Initialisierung (init()): Event-Listener für Tabs, Buttons, Eingaben.
Festplattenanzeige (renderSizes(), renderSlots()): Dynamische Buttons und Slots.
Berechnung (computeData()): Speicheraufteilung für RAID-Typen.
Ergebnisdarstellung (renderResults(), renderChartRow()): Diagramme und Dropdown.
Zurücksetzen (clearResults()): Löscht Ergebnisse und setzt Eingaben zurück.





Nutzung

Wählen Sie HDD oder SATA SSD über die Tabs.
Klicken Sie auf Festplattengrößen, um Slots zu füllen (max. 12).
Geben Sie die Anzahl der Hot Spares ein.
Klicken Sie auf "Berechnen" für Speicheraufteilung.
Sehen Sie die besten RAID-Konfigurationen und wählen Sie weitere Typen im Dropdown.

Technische Details

Sprache: HTML, CSS, JavaScript.
Einheiten: Kapazitäten in TB, binäre Darstellung von 1 GB.
RAID-Berechnungen:
RAID 0: Volle Kapazität, kein Schutz.
RAID 1: Kleinste Festplatte als nutzbare Kapazität.
RAID 5: Kapazität minus eine Festplatte (Parität).
RAID 6: Kapazität minus zwei Festplatten (Parität).
RAID 10: Hälfte der Festplatten × kleinste Festplatte.
JBOD: Summierte Kapazität ohne Redundanz.


Reservierter Speicher: 1 % der Rohkapazität.

Hinweise

Ergebnisse basieren auf einer binären Darstellung von 1 GB.
Farbcodierung: Orange (reserviert), Grün (nutzbar), Blau (Parität), Grau (ungenutzt).
Responsive Design für verschiedene Bildschirmgrößen.
