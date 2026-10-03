<div align="center">

<img src="assets/nexora-logo.png" width="130" alt="Nexora Logo">

# NEXORA

### DEVELOPER WORKSPACE

**Terminal · SSH · System · Projekte · Tools**

Eine moderne Developer-Konsole für Windows.

<br>

![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-20242A?style=for-the-badge&logo=windows11&logoColor=white)
![Release](https://img.shields.io/badge/Release-Beta-4DD9C5?style=for-the-badge)
![Version](https://img.shields.io/badge/Version-0.1.0-20242A?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-4DD9C5?style=for-the-badge)

<br>

**[Übersicht](#-was-ist-nexora) · [Terminal](#-terminal) · [SSH](#-ssh--remote) · [System](#-system-monitoring) · [Beta](#-beta)**

</div>

---

## ◈ Was ist Nexora?

**Nexora** ist ein moderner Developer Workspace für Windows, der alltägliche
Entwicklungs- und Administrationswerkzeuge in einer gemeinsamen Anwendung
vereint.

Terminal öffnen. Server über SSH verwalten. Systemressourcen überwachen.
Projekte organisieren. Tools ausführen.

Alles, ohne ständig zwischen verschiedenen Anwendungen wechseln zu müssen.

> **Nexora bringt deinen Workspace an einen Ort.**

---

## ✦ Ein Workspace. Mehr Möglichkeiten.

<table>
<tr>
<td width="33%" valign="top">

### `>_` Terminal

PowerShell und CMD direkt innerhalb von Nexora – mit Tabs und mehreren
parallelen Sitzungen.

</td>
<td width="33%" valign="top">

### `◇` SSH

Verbinde dich über SSH mit deinen Servern und speichere häufig verwendete
Verbindungen als Profile.

</td>
<td width="33%" valign="top">

### `▣` System

Überwache CPU, RAM, Speicher und weitere Systeminformationen direkt
innerhalb deines Workspace.

</td>
</tr>

<tr>
<td width="33%" valign="top">

### `◆` Projekte

Organisiere deine Entwicklungsprojekte und öffne sie direkt aus Nexora.

</td>
<td width="33%" valign="top">

### `⌘` Tools

Häufig benötigte Developer- und Systemwerkzeuge sind zentral erreichbar.

</td>
<td width="33%" valign="top">

### `⚙` Workspace

Passe Nexora und deinen Workflow über die integrierten Einstellungen an.

</td>
</tr>
</table>

---

# `>_` Terminal

## Deine Konsole. Neu gedacht.

Nexora integriert deine Windows-Shell direkt in den Developer Workspace.

<div align="center">

<img src="assets/screenshots/terminal.png" width="100%" alt="Nexora Terminal">

</div>

### Terminal Features

- PowerShell
- CMD
- mehrere Terminal-Tabs
- parallele Sessions
- Command History
- Copy & Paste
- Arbeitsverzeichnis
- Prozessinformationen
- Statusanzeige

In der unteren Statusleiste zeigt Nexora zusätzlich wichtige Informationen
über die aktuelle Sitzung und dein System.

```text
CMD  ·  Verbunden  ·  PID 22296

Node v24.21.0  ·  CPU 67%  ·  RAM 70%  ·  Disk 46%  ·  Nexora 0.1.0
```

---

# ◇ SSH & Remote

## Deine Server. Direkt verbunden.

Nexora besitzt einen integrierten SSH-Bereich für Remote-Verbindungen.

Server können mit Host, Benutzer und Port eingerichtet und als Profile
gespeichert werden.

```text
Development

Host       server.example.com
User       deploy
Port       22

                     [ Verbinden → ]
```

Nexora verwendet dafür den **Windows OpenSSH Client**.

Eine Verbindung entspricht beispielsweise:

```powershell
ssh deploy@server.example.com -p 22
```

Damit bleiben SSH-Passwort-, Schlüssel- und Host-Abfragen innerhalb
der Terminal-Sitzung.

---

# ▣ System Monitoring

## Alles im Blick.

Nexora zeigt wichtige Systeminformationen live direkt im Workspace an.

<div align="center">

<img src="assets/screenshots/system.png" width="100%" alt="Nexora System Monitoring">

</div>

Die Werte werden regelmäßig aktualisiert.

### Systeminformationen

| Information | Beschreibung |
|:--|:--|
| **CPU** | Aktuelle Prozessorauslastung |
| **RAM** | Aktuelle Arbeitsspeicherauslastung |
| **Disk** | Speicherbelegung |
| **System** | Windows-Version und Architektur |
| **CPU Info** | Anzahl logischer Prozessoren |
| **Storage** | Freier und gesamter Speicher |

Über **„Prozesse im Terminal anzeigen“** können laufende Prozesse direkt
über das Nexora Terminal untersucht werden.

---

# ◆ Projekte

Nexora besitzt einen eigenen Bereich für Entwicklungsprojekte.

Dadurch können Projekte zentral verwaltet und direkt mit dem Terminal
und den integrierten Developer Tools verwendet werden.

Der Workspace ist auf typische Entwicklungsumgebungen wie beispielsweise
Node.js, .NET, Java, Python und Git ausgelegt.

---

# ⌘ Befehle

Über **Befehle** in der oberen Navigationsleiste können Funktionen
schnell aufgerufen werden.

Nexora ist dadurch nicht ausschließlich über die Seitenleiste bedienbar,
sondern bietet einen schnellen Workflow für häufig verwendete Aktionen.

---

# ✦ Live Status

Die Nexora Statusleiste liefert jederzeit einen schnellen Überblick:

```text
Node v24.21.0
CPU 30%
RAM 70%
Disk 46%
Nexora 0.1.0
```

Dadurch bleiben wichtige Informationen sichtbar, ohne den eigentlichen
Workspace zu überladen.

---

# 🎨 Nexora Design

Nexora verwendet eine bewusst reduzierte Benutzeroberfläche.

Das Design basiert auf:

- dunklem Developer-Workspace
- Türkis als Nexora-Akzentfarbe
- klarer Seitenleiste
- minimalistischen Icons
- dezenten Rahmen
- großen Arbeitsflächen
- reduzierten Statusanzeigen
- konsistenter Typografie

Das Ziel ist eine Oberfläche, die auch bei längerer Arbeit übersichtlich
und angenehm bleibt.

---

# 🔐 Sicherheit

Gerade bei Remote-Verbindungen behandelt Nexora sensible Daten bewusst.

Nexora setzt unter anderem auf:

- Windows OpenSSH
- keine fest eingebauten Passwörter
- keine Zugangsdaten im Quellcode
- SSH Host Verification
- Unterstützung bestehender SSH-Sicherheitsmechanismen

---

# ⚙ Technologie

| | |
|:--|:--|
| **Platform** | Windows |
| **Language** | C# |
| **Framework** | .NET |
| **Interface** | Windows Desktop |
| **Remote** | Windows OpenSSH |
| **Version** | 0.1.0 |
| **Release Channel** | Beta |

---

# 🧪 Beta

> [!IMPORTANT]
> ### Nexora befindet sich aktuell in der Beta.
>
> Nexora ist bereits funktionsfähig und kann verwendet werden.
> Da es sich noch um eine Beta-Version handelt, können Fehler auftreten
> und einzelne Funktionen oder Teile der Benutzeroberfläche noch verändert
> oder erweitert werden.

Bug Reports und Verbesserungsvorschläge sind ausdrücklich willkommen.

---

# 🐛 Bugs & Feedback

Du hast einen Fehler gefunden oder eine Idee für Nexora?

Erstelle ein **GitHub Issue** mit möglichst folgenden Informationen:

- Nexora-Version
- Windows-Version
- Beschreibung des Problems
- Schritte zum Reproduzieren
- Screenshot oder Fehlermeldung, falls vorhanden

---

# 🗺 Roadmap

Nexora wird auch nach der Beta kontinuierlich weiterentwickelt.

Geplant sind unter anderem:

- [ ] weitere Terminal-Funktionen
- [ ] erweiterte SSH-Verwaltung
- [ ] zusätzliche Developer Tools
- [ ] mehr Projektfunktionen
- [ ] Performance-Optimierungen
- [ ] weitere Anpassungsmöglichkeiten
- [ ] zusätzliche Nexora Commands
- [ ] Plugin-System

---

<div align="center">

<br>

<img src="assets/nexora-logo.png" width="80" alt="Nexora">

## NEXORA

### DEVELOPER WORKSPACE

**Terminal. Remote. System. Develop.**

<br>

`Windows` · `Terminal` · `SSH` · `System` · `Development`

<br>

**Nexora 0.1.0 Beta**

</div>
