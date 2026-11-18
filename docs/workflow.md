# Aufgabe 2.3 / 2.4 – Werkzeuge und Workflow im Team

## Entscheidung (2.3)

| Zweck | Werkzeug | Warum |
|---|---|---|
| Gemeinsamer Code | **Git** mit **GitHub** (dieses Repository) | Versionsverwaltung, Branches, Code-Review über Pull Requests |
| Aufgabenverwaltung | **GitHub Issues** + **Meilensteine** | Jedes Arbeitspaket (AP1–AP17) ist ein Issue mit Verantwortlichem, Akzeptanzkriterien und Sprint-Meilenstein |
| Kanban-Board (wie Trello) | **GitHub Projects** (Spalten *Todo / In Arbeit / Review / Erledigt*) | Überblick, wer woran arbeitet; Grundlage für die Scrum-Meetings |
| Zeitplan | **GanttProject** ([`planung/Projektplan.gan`](../planung/Projektplan.gan)) | Gantt-Diagramm mit Meilensteinen (Aufgabe 2.2) |
| Architektur | **draw.io** ([`docs/architektur/Systemarchitektur.drawio`](architektur/Systemarchitektur.drawio)) | Schaubild aus Aufgabe 1.1 |
| Entwicklung | **STM32CubeIDE** | Vorgabe des Praktikums |

Git ist eines der vorgegebenen Tools; GitHub übernimmt die Rolle von GitLab (gleiche Funktionen: Repository, Issues, Merge/Pull Requests, Board).

## Arbeitsweise mit Git

1. `main` enthält immer einen **lauffähigen** Stand. Niemand committet direkt auf `main`.
2. Für jedes Issue einen eigenen Branch anlegen: `ap<Nr>-<kurzname>`, z. B. `ap3-taster-interrupt`.
3. Kleine, aussagekräftige Commits, z. B. `AP3: EXTI-Callback erzeugt StartEvent`.
4. Fertig → **Pull Request** gegen `main`, im Text `Closes #<Issue-Nr>` schreiben.
5. Mindestens **ein anderes Teammitglied** prüft den Pull Request (Code lesen, auf eigenem Board testen) und merged ihn.
6. Vor Arbeitsbeginn immer `git pull` auf `main` und den eigenen Branch aktualisieren (`git merge main`).
7. Konflikte in CubeMX-generierten Dateien vermeiden: Eigenen Code nur zwischen `/* USER CODE BEGIN */` und `/* USER CODE END */` schreiben; Änderungen an der `.ioc`-Datei vorher im Team absprechen.

## Ordnerstruktur

```
firmware/        STM32CubeIDE-Projekt (wird in AP1 angelegt)
docs/            Architektur, Arbeitspakete, Zeitplan, Präsentationen
planung/         GanttProject-Datei
```

## Scrum-Rhythmus

- **Sprint-Planning**: Issues des Sprints im Board in *Todo* ziehen und Verantwortliche zuweisen.
- **Kurzes Treffen 2× pro Woche** (z. B. nach der Sprechstunde): Was ist erledigt? Was als Nächstes? Wo hängt es? → Board aktualisieren.
- **Sprint-Ende**: Meilenstein prüfen, offene Issues in den nächsten Sprint verschieben.

## Einrichtung – Checkliste für jedes Teammitglied (2.4)

- [ ] Git installieren (`git --version` funktioniert) und Namen/E-Mail setzen:
      `git config --global user.name "Vorname Nachname"` und `git config --global user.email "..."`
- [ ] GitHub-Konto anlegen und vom Repo-Besitzer als Collaborator einladen lassen (Repo → *Settings → Collaborators*)
- [ ] Repository klonen: `git clone https://github.com/Mekin66/Projektpraktikum.git`
- [ ] STM32CubeIDE installiert, Projekt aus `firmware/` importieren und bauen (ab AP1)
- [ ] GanttProject installieren und `planung/Projektplan.gan` öffnen
- [ ] Testlauf: eigenen Branch `test-<name>` anlegen, eine Zeile in `docs/team.md` ergänzen, Pull Request erstellen, von jemand anderem mergen lassen
- [ ] Im Project-Board die eigenen Issues ansehen – jeder kennt seine nächste Aufgabe
