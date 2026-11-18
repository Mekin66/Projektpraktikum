# Aufgabe 2.2 – Zeitplan (Gantt-Diagramm)

Die editierbare Version liegt als GanttProject-Datei unter [`planung/Projektplan.gan`](../planung/Projektplan.gan) (in GanttProject über *Projekt → Öffnen*). Das Diagramm unten wird von GitHub direkt angezeigt.

## Meilensteine

| Meilenstein | Datum | Ziel |
|---|---|---|
| M1 Inkrement 1 fertig | 13.12.2026 | Inkrement 1 erfüllt Product Backlog 1 (Ablauf mit Onboard-Peripherie, Abbruch, Cleanup, Ergebnis) |
| M2 Zwischenpräsentation (KW 51) | 14.12.2026 | Vorführung von Inkrement 1 vor dem Product Owner (genaues Datum in KW 51 eintragen) |
| M3 Inkrement 2 fertig | 24.01.2027 | Endprodukt erfüllt alle Mindestanforderungen (Zeitkonstante genau messen, Display-Führung, Fehlerbehandlung) |
| M4 Abschlusspräsentation (KW 5) | 25.01.2027 | Funktionsdemo und schriftliche Kurzanleitung (genaues Datum in KW 5 eintragen) |

## Gantt-Diagramm

```mermaid
gantt
  title Projektphase RC-Bauteiltester
  dateFormat YYYY-MM-DD
  axisFormat %d.%m.
  section Sprint 1
  AP1 Projektsetup & Repository :ap1, 2026-11-21, 2d
  AP2 Event-Framework (Event-Queue) :ap2, 2026-11-23, 6d
  AP3 Taster & Interrupt (EXTI) :ap3, 2026-11-23, 9d
  AP4 LED-Statusanzeige :ap4, 2026-11-23, 9d
  AP5 Display-Modul (LCD über I²C) :ap5, 2026-11-23, 13d
  AP6 Zustandsautomat (Idle/Betrieb/Cleanup/Ergebnis) :ap6, 2026-11-29, 8d
  AP7 Integration & Test Inkrement 1 :ap7, 2026-12-07, 5d
  AP8 Zwischenpräsentation vorbereiten :ap8, 2026-12-09, 5d
  Inkrement 1 fertig :milestone, m1, 2026-12-13, 0d
  Zwischenpräsentation (KW 51) :milestone, m2, 2026-12-14, 0d
  section Sprint 2
  AP9 Sprint-2-Planung & Projektplan aktualisieren :ap9, 2026-12-19, 2d
  AP10 Entprellung des Tasters :ap10, 2026-12-21, 8d
  AP11 RC-Glied aufbauen & beschalten :ap11, 2026-12-21, 9d
  AP12 Nutzerführung über Display (Pflicht) :ap12, 2026-12-21, 21d
  AP13 Messung (Sprung ausgeben, ADC-Messreihe) :ap13, 2026-12-30, 12d
  AP14 Berechnung der Zeitkonstante :ap14, 2026-12-30, 14d
  AP15 Fehlerbehandlung & Fehleingaben :ap15, 2027-01-11, 6d
  AP16 Integration & Systemtest Inkrement 2 :ap16, 2027-01-17, 5d
  AP17 Abschlusspräsentation & Kurzanleitung :ap17, 2027-01-18, 7d
  Inkrement 2 fertig :milestone, m3, 2027-01-24, 0d
  Abschlusspräsentation (KW 5) :milestone, m4, 2027-01-25, 0d
```

Zwischen 14.12. und 18.12.2026 findet die Zwischenpräsentation statt; die Feiertage sind im Zeitraum von AP10–AP14 mit Puffer eingeplant.
