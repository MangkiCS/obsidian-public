---
publish: true
title: Obsidian auf Android mit ChatGPT und Codex verbinden
created: 2026-08-18T12:41:08.627Z
modified: 2026-08-18T12:41:14.115Z
tags:
  - obsidian
  - chatgpt
  - codex
  - android
  - github
---

# Obsidian auf Android mit ChatGPT und Codex verbinden

Ich nutze Obsidian hauptsächlich auf Android. Dabei wollte ich meine Notizen nicht nur mit ChatGPT besprechen können, sondern der KI auch ermöglichen, größere Änderungen an meinem Vault vorzunehmen.

Eine direkte Verbindung zwischen ChatGPT und dem lokalen Obsidian-Vault auf Android ist dafür nicht ideal. GitHub kann aber als Brücke dienen.

## Mein Setup

Die Architektur sieht ungefähr so aus:

```text
Obsidian auf Android
        ↕
      GitSync
        ↕
 privates GitHub-Repository
        ↕
       Codex
```

Zusätzlich verwende ich Quartz für meine öffentlichen Notizen:

```text
Obsidian
   │
   ├── GitSync
   │      ↓
   │   privates Vault-Repository
   │      ↕
   │    Codex
   │
   └── Quartz Syncer
          ↓
      öffentliches Quartz-Repository
          ↓
      GitHub Pages
```

Damit bleiben mein privater Vault und meine öffentliche Website voneinander getrennt.

## Warum GitHub dazwischen?

Mein Obsidian-Vault liegt lokal auf meinem Android-Gerät.

GitSync synchronisiert diesen Vault mit einem privaten GitHub-Repository. Dadurch existiert eine Version meiner Markdown-Dateien, auf die andere Werkzeuge zugreifen können.

Das private Repository ist dabei meine eigentliche Wissensbasis.

Beispielsweise:

```text
obsidian-vault
├── Projects/
├── Notes/
├── Journal/
├── Resources/
├── Public/
└── assets/
```

Das Repository bleibt privat.

## ChatGPT oder Codex?

Für reines Lesen und Fragen zu meinen Notizen reicht ChatGPT vollkommen aus.

Zum Beispiel:

- „Fasse meine Notizen zu Solarthermie zusammen.“
- „Welche Projekte erwähnen Home Assistant?“
- „Welche offenen Aufgaben habe ich zum Thema Server?“
- „Erstelle aus meinen Notizen eine Übersicht.“

Wenn die KI allerdings selbst Änderungen am Vault vornehmen soll, wird Codex interessanter.

## Warum ich Codex dafür spannender finde

Codex arbeitet direkt mit einem Repository.

Dadurch kann ich Aufgaben formulieren wie:

> Ordne alle Notizen über meinen Homeserver unter einem gemeinsamen Ordner ein und aktualisiere die Wikilinks.

Oder:

> Erstelle aus meinen verstreuten Notizen zum Thema Solarthermie eine MOC-Datei.

Oder:

> Suche nach kaputten Markdown-Links und repariere sie.

Codex kann dabei mehrere Dateien gleichzeitig bearbeiten.

Danach landen die Änderungen wieder im Git-Repository.

GitSync zieht sie anschließend zurück auf mein Android-Gerät und Obsidian sieht die Änderungen.

## Der wichtige Unterschied

Ich möchte allerdings nicht, dass Codex direkt mein öffentliches Quartz-Repository verwaltet.

Deshalb verwende ich zwei getrennte Repositories.

### Privater Vault

```text
obsidian-vault
```

Eigenschaften:

- privat
- enthält meinen vollständigen Vault
- wird mit GitSync synchronisiert
- kann von Codex bearbeitet werden

### Öffentliche Website

```text
obsidian-public
```

Eigenschaften:

- öffentlich
- enthält nur veröffentlichte Notizen
- wird über Quartz Syncer befüllt
- wird mit Quartz gebaut
- wird über GitHub Pages veröffentlicht

Damit entscheide weiterhin ich selbst, welche Inhalte öffentlich werden.

## Veröffentlichen mit Quartz

Eine Notiz, die auf meiner Website erscheinen soll, markiere ich in Obsidian beispielsweise mit:

```yaml
---
publish: true
---
```

Quartz Syncer erkennt diese Datei anschließend im Publication Center.

Nach dem Veröffentlichen landet sie im `content`-Verzeichnis meines Quartz-Repositories.

Der Ablauf ist also:

```text
Private Notiz
    ↓
publish: true
    ↓
Quartz Syncer
    ↓
GitHub
    ↓
Quartz Build
    ↓
GitHub Pages
```

## Warum mir dieses Modell gefällt

Die einzelnen Werkzeuge haben jeweils eine klar definierte Aufgabe:

**Obsidian** ist mein Editor und meine Wissensdatenbank.

**GitSync** synchronisiert meinen vollständigen Vault.

**GitHub** ist die gemeinsame Schnittstelle zwischen meinen Geräten und KI-Werkzeugen.

**Codex** kann größere Änderungen an meinem Vault durchführen.

**Quartz Syncer** entscheidet, welche Notizen veröffentlicht werden.

**Quartz** verwandelt meine Markdown-Dateien in eine Website.

Dadurch muss ich meinen privaten Vault nicht direkt öffentlich zugänglich machen.

## Fazit

Für mich ist GitHub die entscheidende Verbindung zwischen Obsidian auf Android und KI-Werkzeugen.

Wenn ich nur mit meinen Notizen sprechen möchte, reicht ChatGPT.

Wenn ich möchte, dass eine KI tatsächlich an meinem Vault arbeitet, Dateien organisiert oder größere Änderungen durchführt, ist Codex deutlich interessanter.

Und durch die Trennung zwischen einem privaten Vault-Repository und einem öffentlichen Quartz-Repository behalte ich trotzdem die Kontrolle darüber, was privat bleibt und was im Internet erscheint.
