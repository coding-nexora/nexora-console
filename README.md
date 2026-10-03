<div align="center">

# ◈ NEXORA

### Your Windows workspace for terminal, remote access and development.

**Eine moderne Windows-Konsole, die Terminal, SSH, Systemverwaltung  
und Developer Tools in einer Oberfläche vereint.**

<br>

![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?style=for-the-badge&logo=windows11&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-10-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Status](https://img.shields.io/badge/STATUS-IN%20DEVELOPMENT-F59E0B?style=for-the-badge)
![Version](https://img.shields.io/badge/VERSION-0.1.0-2DD4BF?style=for-the-badge)

<br>

**[Features](#-features) · [Remote](#-remote--ssh) · [Commands](#-nexora-commands) · [Roadmap](#-roadmap) · [Development](#-development)**

</div>

---

## ◈ Meet Nexora

**Nexora** ist eine moderne Terminal- und Entwicklungsumgebung für Windows.

Statt Terminal, SSH-Client, Systeminformationen und Entwicklerwerkzeuge
auf mehrere Programme zu verteilen, bringt Nexora diese Funktionen
in einer gemeinsamen Oberfläche zusammen.

Nexora ersetzt PowerShell und CMD dabei nicht.

Es baut auf den vorhandenen Windows-Werkzeugen auf und erweitert sie
um eine moderne Benutzeroberfläche, Remote-Verbindungen,
Serverprofile und zusätzliche Entwicklerfunktionen.

> **Ein Workspace. Deine Terminals. Deine Server. Deine Projekte.**

---

## ✦ Features

<table>
<tr>
<td width="50%">

### `>_` Modern Terminal

PowerShell und CMD direkt innerhalb von Nexora verwenden.

- mehrere Terminal-Tabs
- Command History
- Copy & Paste
- eigene Nexora Commands
- anpassbare Terminal-Einstellungen

</td>
<td width="50%">

### `◇` Remote & SSH

Linux- und andere SSH-Systeme direkt aus Nexora erreichen.

- SSH über Windows OpenSSH
- gespeicherte Serverprofile
- eigene Ports und Benutzer
- SSH-Key-Unterstützung geplant
- Verbindungen direkt im Terminal

</td>
</tr>

<tr>
<td width="50%">

### `▣` System

Wichtige Informationen über deinen Windows-PC auf einen Blick.

- CPU
- RAM
- Speicher
- Netzwerk
- Prozesse
- Ports

</td>
<td width="50%">

### `◆` Developer Tools

Nexora erkennt Entwicklungsprojekte und stellt passende Werkzeuge bereit.

- .NET
- Node.js
- Python
- Java
- Git

</td>
</tr>
</table>

---

# ◇ Remote. Direkt verbunden.

Nexora verfügt über einen integrierten **Remote Manager**.

Serverdaten können bequem über die Oberfläche eingetragen und
als Profile gespeichert werden.

<div align="center">

![Nexora Remote](docs/screenshots/remote.png)

</div>

### Eine Verbindung könnte beispielsweise so aussehen

```text
Name       Development
Server     server.example.com
Benutzer   deploy
Port       22
```

Nexora verwendet im Hintergrund den in Windows vorhandenen
**OpenSSH-Client**.

Die entsprechende Verbindung lautet:

```powershell
ssh deploy@server.example.com -p 22
```

Passwort-, Key- und Host-Abfragen bleiben innerhalb der
Terminal-Sitzung.

---

## ◇ Server Profiles

Häufig verwendete Server müssen nicht jedes Mal neu eingetragen werden.

Nexora kann Verbindungsprofile speichern:

```text
╭──────────────────────────────────────────────╮
│  ◇ Development                              │
│                                              │
│  deploy@server.example.com                   │
│  Port 22                                     │
│                                              │
│  ● Ready                                     │
│                                              │
│                 [ Connect → ]                │
╰──────────────────────────────────────────────╯
```

Geplant sind außerdem:

- Favoriten
- SSH Keys
- Verbindungsstatus
- zuletzt verwendete Server
- Profilbearbeitung
- schnelle Wiederverbindung

---

# `>_` Terminal

Das Terminal bildet das Herzstück von Nexora.

```text
╭─ NEXORA ────────────────────────────────────────────────╮
│                                                       │
│  PowerShell 7                          ● Running       │
│                                                       │
│  C:\Projects\Nexora                                   │
│                                                       │
│  ❯ dotnet run                                         │
│                                                       │
│  Building...                                          │
│  ✓ Build succeeded                                    │
│                                                       │
│  Nexora started successfully.                         │
│                                                       │
│  ❯ _                                                  │
│                                                       │
╰───────────────────────────────────────────────────────╯
```

Unterstützt werden sollen:

**PowerShell** · **PowerShell 7** · **CMD**

Jede Terminal-Sitzung läuft unabhängig in einem eigenen Tab.

---

# ◈ Nexora Commands

Neben normalen Shell-Befehlen erhält Nexora ein eigenes Command-System.

```powershell
nexora help
nexora version

nexora system
nexora processes
nexora network
nexora ports
nexora disk

nexora ssh
```

### Beispiel

```text
❯ nexora system

  ◈ NEXORA SYSTEM

  Operating System     Windows 11
  Architecture         x64
  Memory               32 GB
  Shell                PowerShell 7
  Nexora               0.1.0

  ✓ System information loaded.

❯
```

---

# ◆ Project Detection

Nexora soll automatisch erkennen, wenn sich das Terminal innerhalb
eines Entwicklungsprojekts befindet.

| Erkennung | Projekt |
|:---|:---|
| `package.json` | Node.js |
| `pyproject.toml` | Python |
| `requirements.txt` | Python |
| `*.csproj` | .NET |
| `pom.xml` | Java / Maven |
| `build.gradle` | Java / Gradle |
| `.git` | Git Repository |

Nach der Erkennung kann Nexora passende Aktionen anbieten:

```text
╭─ PROJECT ───────────────────────────────────╮
│                                            │
│  ◆ Nexora                                  │
│                                            │
│  Framework       .NET                      │
│  Git Branch      main                      │
│  Status          ✓ Ready                   │
│                                            │
│  [ ▶ Run ]   [ Git ]   [ Open Folder ]     │
│                                            │
╰────────────────────────────────────────────╯
```

---

# ▣ System Dashboard

Systeminformationen sollen direkt innerhalb von Nexora verfügbar sein.

```text
SYSTEM STATUS

CPU       ███████░░░░░░░░░░░░░   34%
Memory    ███████████░░░░░░░░░   52%
Disk      █████████████░░░░░░░   64%

Network

↓  24.8 MB/s
↑   4.2 MB/s

Uptime    2d 14h 32m
```

Alle angezeigten Werte sollen tatsächlich aus Windows ausgelesen werden.

---

# ⌘ Command Palette

Viele Nexora-Funktionen sollen ohne Navigation erreichbar sein.

```text
Ctrl + Shift + P
```

öffnet die Command Palette:

```text
╭──────────────────────────────────────────────╮
│  Search commands...                         │
├──────────────────────────────────────────────┤
│                                              │
│  >  New PowerShell Terminal                 │
│     New CMD Terminal                        │
│     Connect to Remote                       │
│     Open Project                            │
│     System Dashboard                        │
│     Settings                                │
│                                              │
╰──────────────────────────────────────────────╯
```

---

# ⌨ Keyboard Shortcuts

| Shortcut | Aktion |
|:---|:---|
| `Ctrl + Shift + T` | Neues Terminal |
| `Ctrl + W` | Aktuellen Tab schließen |
| `Ctrl + Shift + P` | Command Palette |
| `Ctrl + ,` | Einstellungen |
| `Ctrl + L` | Terminal leeren |
| `Ctrl + C` | Kopieren / Prozess abbrechen |
| `Ctrl + V` | Einfügen |

---

# 🔐 Security by Design

Remote-Verbindungen benötigen besondere Sorgfalt.

Nexora soll deshalb grundsätzlich:

- keine Passwörter im Quellcode speichern
- keine Zugangsdaten als Klartext in normalen Konfigurationsdateien ablegen
- SSH Keys unterstützen
- bekannte SSH Hosts respektieren
- Host-Fingerprint-Prüfungen nicht automatisch umgehen
- sensible Daten über geeignete Windows-Sicherheitsfunktionen speichern

---

# 🗺 Roadmap

### `v0.1` — Foundation

- [x] Nexora Grundoberfläche
- [x] Remote UI
- [ ] PowerShell Terminal
- [ ] CMD Terminal
- [ ] Terminal Tabs
- [ ] funktionierende SSH-Verbindungen
- [ ] Serverprofile
- [ ] Settings

### `v0.2` — Developer

- [ ] Nexora Commands
- [ ] System Dashboard
- [ ] Command Palette
- [ ] Project Detection
- [ ] Git Integration

### `v0.3` — Remote

- [ ] SSH Key Manager
- [ ] Server Dashboard
- [ ] Remote Status
- [ ] Favoriten
- [ ] Connection History

### `Future`

- [ ] Plugin System
- [ ] Themes
- [ ] Auto Update
- [ ] erweiterte Developer Tools
- [ ] zusätzliche Remote-Funktionen

---

# ⚙ Development

Nexora wird speziell für Windows entwickelt.

| | |
|:---|:---|
| **Language** | C# |
| **Framework** | .NET |
| **UI** | WinUI 3 |
| **Architecture** | MVVM |
| **Remote** | Windows OpenSSH |
| **Platform** | Windows 10 / 11 |

---

# 📂 Repository

Eine mögliche Projektstruktur:

```text
Nexora/
│
├── src/
│   ├── Nexora.App/
│   ├── Nexora.Core/
│   ├── Nexora.Terminal/
│   ├── Nexora.Remote/
│   └── Nexora.System/
│
├── tests/
│
├── docs/
│   ├── screenshots/
│   │   └── remote.png
│   └── architecture/
│
├── README.md
├── LICENSE
└── .gitignore
```

---

# 🚧 Development Status

> [!IMPORTANT]
> **Nexora befindet sich aktuell in Entwicklung.**
>
> Funktionen, Benutzeroberfläche und Architektur können sich bis zur
> ersten stabilen Version noch verändern.

Fehler und Verbesserungsvorschläge können über GitHub Issues gemeldet werden.

---

<div align="center">

<br>

# ◈

## NEXORA

### Terminal. Remote. Develop.

**Built for Windows. Designed for developers.**

<br>

`Windows` · `.NET` · `WinUI 3` · `OpenSSH`

</div>
