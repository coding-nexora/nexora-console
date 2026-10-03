<div align="center">

# ◈ Nexora

### Terminal. Remote. Develop.

**Eine moderne Windows-Konsole für Entwickler, Serveradministratoren und Power-User.**

PowerShell · CMD · SSH · Server Management · Developer Tools

![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-blue)
![.NET](https://img.shields.io/badge/.NET-10-purple)
![Status](https://img.shields.io/badge/Status-In%20Development-orange)
![Version](https://img.shields.io/badge/Version-0.1.0-green)

</div>

---

## ◈ Was ist Nexora?

**Nexora** ist eine moderne Terminal-, Developer- und Servermanagement-Anwendung
für Windows.

Das Ziel von Nexora ist nicht, PowerShell oder CMD komplett zu ersetzen.
Stattdessen verbindet Nexora bestehende Windows-Shells mit einer modernen
Benutzeroberfläche und zusätzlichen Werkzeugen.

Mit Nexora kannst du beispielsweise:

- PowerShell und CMD verwenden
- mehrere Terminal-Sitzungen gleichzeitig öffnen
- Linux-Server über SSH verwalten
- Serverprofile speichern
- Systeminformationen überwachen
- Entwicklungsprojekte erkennen
- eigene `nexora`-Befehle verwenden
- häufig verwendete Entwicklerwerkzeuge zentral verwalten

---

# 🖥️ Nexora Console

Die Nexora Console bildet das Herzstück der Anwendung.

Beispiel:

```text
┌───────────────────────────────────────────────────────────────┐
│ ◈ NEXORA                                      ─   □   ×      │
├────────────┬──────────────────────────────────────────────────┤
│            │ PowerShell ×    CMD ×    +                      │
│ ◈ Home     ├──────────────────────────────────────────────────┤
│ > Terminal │                                                  │
│ ◇ Remote   │ PowerShell 7                     ● Running       │
│ ▣ System   │                                                  │
│ ⬡ Projects │ C:\Users\User\Projects\Nexora                   │
│ ⚙ Settings │                                                  │
│            │ ❯ dotnet run                                    │
│            │                                                  │
│            │ Building Nexora...                               │
│            │ ✓ Build succeeded                               │
│            │                                                  │
│            │ ❯ _                                             │
│            │                                                  │
├────────────┴──────────────────────────────────────────────────┤
│ main │ .NET │ CPU 12% │ RAM 38% │ Nexora 0.1.0              │
└───────────────────────────────────────────────────────────────┘
```

---

# 🌐 Remote / SSH

Nexora besitzt einen integrierten Remote-Bereich für SSH-Verbindungen.

Anstatt jedes Mal einen vollständigen SSH-Befehl einzugeben, können
Server als Profile gespeichert werden.

Beispiel:

```text
┌─────────────────────────────────────────────────────────────┐
│ REMOTE                                                      │
│                                                             │
│ Deine Server. Direkt verbunden.                             │
│                                                             │
│ Name                                                        │
│ [ Development Server                                  ]     │
│                                                             │
│ Server                                   Port               │
│ [ server.example.com                ]    [ 22 ]             │
│                                                             │
│ Benutzer                                                    │
│ [ deploy                                              ]     │
│                                                             │
│                 [ Profil speichern ] [ ◇ Verbinden → ]      │
└─────────────────────────────────────────────────────────────┘
```

Nexora verwendet dafür den **Windows OpenSSH Client**.

Intern entspricht eine Verbindung beispielsweise:

```powershell
ssh deploy@server.example.com -p 22
```

Passwort- und Sicherheitsabfragen bleiben direkt innerhalb der
Terminal-Sitzung.

---

# 💾 Gespeicherte Server

Server können als Profile gespeichert werden.

```text
GESPEICHERTE SERVER

┌────────────────────────────────────────┐
│ ◇ Development                          │
│                                        │
│ deploy@server.example.com              │
│ Port 22                                │
│                                        │
│ ● Bereit                               │
│                                        │
│ [ Verbinden ]              [ ••• ]     │
└────────────────────────────────────────┘

┌────────────────────────────────────────┐
│ ◇ Production                           │
│                                        │
│ root@production.example.com            │
│ Port 22                                │
│                                        │
│ ● Bereit                               │
│                                        │
│ [ Verbinden ]              [ ••• ]     │
└────────────────────────────────────────┘
```

Dadurch kann eine häufig verwendete SSH-Verbindung mit wenigen Klicks
gestartet werden.

---

# ⚡ Eigene Nexora Commands

Neben normalen PowerShell- und CMD-Befehlen soll Nexora eigene Befehle
bereitstellen.

Beispiele:

```powershell
nexora help
nexora version
nexora system
nexora network
nexora ports
nexora processes
nexora disk
nexora ssh
```

Beispiel:

```text
❯ nexora system

◈ NEXORA SYSTEM

Operating System    Windows 11
Architecture        x64
Processor           AMD64
Memory              32 GB
Nexora               0.1.0

✓ System information loaded.
```

---

# 📊 System Dashboard

Nexora soll wichtige Systeminformationen direkt anzeigen können.

```text
SYSTEM

CPU
████████░░░░░░░░░░░░  38%

MEMORY
████████████░░░░░░░░  57%

DISK
██████████████░░░░░░  68%

Network
↓ 24.8 MB/s
↑ 4.2 MB/s

Uptime
2d 14h 32m
```

Geplant sind Informationen über:

- CPU
- Arbeitsspeicher
- Laufwerke
- Netzwerk
- Windows-Version
- Systemlaufzeit
- laufende Prozesse
- verwendete Ports

---

# 📁 Developer Projects

Nexora soll Entwicklungsprojekte automatisch erkennen.

Unterstützt werden sollen unter anderem:

| Datei | Erkanntes Projekt |
|---|---|
| `package.json` | Node.js |
| `pyproject.toml` | Python |
| `requirements.txt` | Python |
| `.csproj` | .NET |
| `pom.xml` | Java / Maven |
| `build.gradle` | Java / Gradle |
| `.git` | Git Repository |

Beispiel:

```text
╭─ PROJECT DETECTED ──────────────────────────╮
│                                            │
│  ◈ Nexora                                  │
│                                            │
│  Type          .NET                        │
│  Git           main                        │
│  Status        ✓ Ready                     │
│                                            │
│  [ ▶ Run ] [ Git ] [ Open Folder ]         │
│                                            │
╰────────────────────────────────────────────╯
```

---

# 🔍 Command Palette

Mit:

```text
Ctrl + Shift + P
```

soll die Nexora Command Palette geöffnet werden.

```text
╭──────────────────────────────────────────────╮
│ 🔍 What do you want to do?                  │
├──────────────────────────────────────────────┤
│ > New PowerShell Terminal                    │
│   New CMD Terminal                           │
│   Connect to SSH Server                      │
│   Open Project                               │
│   Show System Dashboard                      │
│   Open Settings                              │
╰──────────────────────────────────────────────╯
```

---

# ⌨️ Shortcuts

| Shortcut | Funktion |
|---|---|
| `Ctrl + Shift + T` | Neues Terminal |
| `Ctrl + W` | Tab schließen |
| `Ctrl + Shift + P` | Command Palette |
| `Ctrl + ,` | Einstellungen |
| `Ctrl + L` | Terminal leeren |
| `Ctrl + C` | Kopieren / Prozess abbrechen |
| `Ctrl + V` | Einfügen |

---

# 🎨 Design

Nexora verwendet eine moderne, minimalistische Benutzeroberfläche.

Designziele:

- Dark Mode
- Light Mode
- Windows-11-inspiriertes Design
- dezente Transparenz
- Nexora-Akzentfarbe
- flüssige Animationen
- klare Typografie
- möglichst wenig visuelle Ablenkung

Die Oberfläche soll modern wirken, ohne die Bedienung eines klassischen
Terminals unnötig kompliziert zu machen.

---

# 🔐 Sicherheit

Sicherheit ist insbesondere bei Remote-Verbindungen wichtig.

Nexora soll deshalb:

- keine Passwörter im Quellcode speichern
- keine Passwörter in normalen JSON-Konfigurationen speichern
- SSH-Schlüssel unterstützen
- sensible Daten über sichere Windows-Schnittstellen speichern
- SSH-Host-Fingerprints nicht automatisch umgehen
- keine unbekannten SSH-Hosts ungefragt akzeptieren

---

# 🗺️ Roadmap

### Nexora 0.1

- [x] Grundlegendes Nexora Interface
- [x] Remote-Seite
- [ ] PowerShell Terminal
- [ ] CMD Terminal
- [ ] Terminal Tabs
- [ ] SSH-Verbindungen
- [ ] Serverprofile
- [ ] Settings

### Nexora 0.2

- [ ] System Dashboard
- [ ] Nexora Commands
- [ ] Command Palette
- [ ] Projekt-Erkennung
- [ ] Git Integration

### Nexora 0.3

- [ ] SSH Key Manager
- [ ] Server Dashboard
- [ ] Plugin-System
- [ ] Themes
- [ ] Auto Update

---

# 🛠️ Technologie

Nexora wird für Windows entwickelt.

Geplanter Stack:

```text
Language       C#
Framework      .NET
UI             WinUI 3
Platform       Windows 10 / Windows 11
Remote         Windows OpenSSH
Architecture   MVVM
```

---

# 📸 Screenshots

> Nexora befindet sich aktuell in Entwicklung.

### Remote Manager

![Nexora Remote Manager](docs/screenshots/remote.png)

Weitere Screenshots folgen mit zukünftigen Versionen.

---

# 🚧 Projektstatus

> **Nexora befindet sich derzeit in aktiver Entwicklung.**

Funktionen, Benutzeroberfläche und Architektur können sich während
der Entwicklung noch verändern.

Die aktuelle Version sollte daher noch nicht als vollständig
produktionsreif betrachtet werden.

---

<div align="center">

## ◈ NEXORA

**Terminal. Remote. Develop.**

Made for Windows.

</div>
