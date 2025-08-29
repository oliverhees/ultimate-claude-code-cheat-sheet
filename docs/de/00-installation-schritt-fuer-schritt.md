# 🚀 Claude Code Installation - Schritt für Schritt

## 🎯 Von Oliver Hees für die KI Heroes Community

[![KI Heroes Community](https://img.shields.io/badge/KI%20Heroes-Community-FF6B6B?style=for-the-badge)](https://www.skool.com/ki-heroes)
[![Website](https://img.shields.io/badge/Website-ki--heroes.net-4ECDC4?style=for-the-badge)](https://ki-heroes.net)

---

## 📋 Inhaltsverzeichnis

1. [Voraussetzungen](#-voraussetzungen)
2. [Windows Installation](#-windows-installation)
3. [macOS Installation](#-macos-installation)
4. [Linux Installation](#-linux-installation)
5. [Erste Schritte nach der Installation](#-erste-schritte-nach-der-installation)
6. [Häufige Probleme & Lösungen](#-häufige-probleme--lösungen)
7. [Video-Tutorials](#-video-tutorials)

---

## ✅ Voraussetzungen

Bevor du mit der Installation beginnst, stelle sicher, dass du folgendes hast:

### Systemanforderungen
- **Betriebssystem**: Windows 10/11, macOS 10.15+, oder Linux (Ubuntu 20.04+)
- **RAM**: Mindestens 4GB (8GB empfohlen)
- **Speicherplatz**: Mindestens 500MB freier Speicher
- **Internet**: Stabile Internetverbindung

### Benötigte Accounts
- **Claude Account**: Registriere dich kostenlos auf [claude.ai](https://claude.ai)
- **API Key** (Optional): Für erweiterte Features

### Vorbereitung
```bash
# Überprüfe deine System-Version
# Windows (PowerShell)
Get-ComputerInfo | select WindowsProductName, WindowsVersion

# macOS/Linux
uname -a
```

---

## 🖥️ Windows Installation

### Methode 1: PowerShell (Empfohlen)

#### Schritt 1: PowerShell als Administrator öffnen
1. Drücke `Windows + X`
2. Wähle "Windows PowerShell (Administrator)"
3. Bestätige die Benutzerkontensteuerung mit "Ja"

#### Schritt 2: Installationsbefehl ausführen
```powershell
# Führe diesen Befehl aus:
irm https://install.anthropic.com/windows | iex

# Alternative, falls der erste nicht funktioniert:
Invoke-WebRequest -Uri https://install.anthropic.com/windows -UseBasicParsing | Invoke-Expression
```

#### Schritt 3: Installation überprüfen
```powershell
# Teste ob Claude Code installiert wurde
claude --version

# Erwartete Ausgabe: claude-code version X.X.X
```

### Methode 2: Manuelle Installation

#### Schritt 1: Installer herunterladen
1. Gehe zu [claude.ai/download](https://claude.ai/download)
2. Lade die Windows `.exe` Datei herunter
3. Speichere sie in deinem Downloads-Ordner

#### Schritt 2: Installation durchführen
1. Doppelklicke auf `claude-code-installer.exe`
2. Folge dem Installationsassistenten
3. Wähle Installationsverzeichnis (Standard: `C:\Program Files\Claude Code`)
4. Klicke auf "Installieren"

#### Schritt 3: PATH-Variable setzen
```powershell
# Füge Claude Code zu PATH hinzu
[Environment]::SetEnvironmentVariable("Path", $env:Path + ";C:\Program Files\Claude Code", [EnvironmentVariableTarget]::User)

# Neustart der PowerShell erforderlich!
```

### 🔧 Windows-spezifische Einstellungen

```powershell
# Aktiviere bessere Terminal-Farben
claude config set terminal.colors true

# Setze Standard-Editor (z.B. VS Code)
claude config set editor "code"

# Aktiviere Auto-Vervollständigung
claude completion install
```

---

## 🍎 macOS Installation

### Methode 1: Terminal (Empfohlen)

#### Schritt 1: Terminal öffnen
1. Drücke `Cmd + Space`
2. Tippe "Terminal"
3. Drücke Enter

#### Schritt 2: Installationsbefehl ausführen
```bash
# Hauptinstallation
curl -sL https://install.anthropic.com | sh

# Bei Berechtingungsfehler mit sudo:
curl -sL https://install.anthropic.com | sudo sh
```

#### Schritt 3: Shell-Konfiguration
```bash
# Für Zsh (Standard in macOS)
echo 'export PATH="$HOME/.claude/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

# Für Bash
echo 'export PATH="$HOME/.claude/bin:$PATH"' >> ~/.bash_profile
source ~/.bash_profile
```

### Methode 2: Homebrew

```bash
# Falls Homebrew nicht installiert ist:
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Claude Code via Homebrew installieren
brew tap anthropic/claude
brew install claude-code

# Update auf neueste Version
brew upgrade claude-code
```

### 🔧 macOS-spezifische Einstellungen

```bash
# Aktiviere macOS Keychain für API Keys
claude config set keychain.enabled true

# Setze VS Code als Standard-Editor
claude config set editor "code"

# Aktiviere Touch ID für sensible Operationen (wenn verfügbar)
claude config set security.touchid true
```

---

## 🐧 Linux Installation

### Ubuntu/Debian

#### Schritt 1: Terminal öffnen
```bash
# Öffne Terminal mit Ctrl + Alt + T
```

#### Schritt 2: Installation
```bash
# Basis-Installation
curl -sL https://install.anthropic.com | sh

# Mit sudo für system-weite Installation
curl -sL https://install.anthropic.com | sudo sh
```

#### Schritt 3: PATH konfigurieren
```bash
# Für Bash
echo 'export PATH="$HOME/.claude/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

# Für Zsh
echo 'export PATH="$HOME/.claude/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

### Fedora/RHEL

```bash
# Installation mit dnf
sudo dnf install -y curl
curl -sL https://install.anthropic.com | sh

# PATH setzen
echo 'export PATH="$HOME/.claude/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

### Arch Linux

```bash
# Via AUR (mit yay)
yay -S claude-code-bin

# Oder manuell
curl -sL https://install.anthropic.com | sh
```

### 🔧 Linux-spezifische Einstellungen

```bash
# Aktiviere Farbausgabe
claude config set terminal.colors true

# Setze bevorzugten Editor
claude config set editor "vim"  # oder "nano", "code", etc.

# Aktiviere Auto-Updates
claude config set updates.auto true
```

---

## 🎉 Erste Schritte nach der Installation

### 1. Installation testen
```bash
# Version überprüfen
claude --version

# Hilfe anzeigen
claude --help

# Erstes "Hallo Welt"
claude "Sage Hallo zu den KI Heroes!"
```

### 2. API Key konfigurieren (Optional)
```bash
# API Key setzen
claude auth login

# Folge den Anweisungen im Browser
# Der API Key wird sicher gespeichert
```

### 3. Erste Konfiguration
```bash
# Öffne Konfiguration
claude config

# Setze dein bevorzugtes Modell
claude config set model claude-3-opus  # oder claude-3-sonnet

# Aktiviere erweiterte Features
claude config set features.advanced true
```

### 4. Erstes Projekt
```bash
# Erstelle ein Test-Projekt
mkdir mein-erstes-claude-projekt
cd mein-erstes-claude-projekt

# Initialisiere Claude Code
claude init

# Stelle deine erste Frage
claude "Erkläre mir, was ich hier alles machen kann"
```

---

## 🔥 Häufige Probleme & Lösungen

### Problem 1: "claude: command not found"

**Lösung:**
```bash
# PATH neu laden
source ~/.bashrc  # oder ~/.zshrc

# PATH manuell setzen
export PATH="$HOME/.claude/bin:$PATH"

# Überprüfe Installation
ls -la ~/.claude/bin/
```

### Problem 2: Berechtingungsfehler

**Windows:**
```powershell
# Als Administrator ausführen
Start-Process powershell -Verb runAs
```

**macOS/Linux:**
```bash
# Mit sudo installieren
sudo curl -sL https://install.anthropic.com | sh

# Berechtigungen korrigieren
chmod +x ~/.claude/bin/claude
```

### Problem 3: Netzwerkfehler

```bash
# Proxy-Einstellungen (falls benötigt)
export HTTP_PROXY=http://proxy.server:port
export HTTPS_PROXY=http://proxy.server:port

# DNS-Cache leeren
# Windows
ipconfig /flushdns

# macOS
sudo dscacheutil -flushcache

# Linux
sudo systemd-resolve --flush-caches
```

### Problem 4: Antivirus blockiert Installation

**Lösung:**
1. Füge Claude Code zu den Ausnahmen hinzu
2. Deaktiviere temporär den Echtzeitschutz
3. Führe Installation erneut durch
4. Aktiviere Echtzeitschutz wieder

---

## 🎥 Video-Tutorials

### Für Anfänger
1. **[Installation auf Windows](https://www.skool.com/ki-heroes)** - 10 Min
2. **[Installation auf macOS](https://www.skool.com/ki-heroes)** - 8 Min
3. **[Installation auf Linux](https://www.skool.com/ki-heroes)** - 12 Min
4. **[Erste Schritte Tutorial](https://www.skool.com/ki-heroes)** - 15 Min

### Troubleshooting Videos
- **[Top 5 Installationsfehler lösen](https://www.skool.com/ki-heroes)**
- **[PATH-Probleme beheben](https://www.skool.com/ki-heroes)**
- **[API Key Setup](https://www.skool.com/ki-heroes)**

---

## ✅ Installation Checkliste

Verwende diese Checkliste, um sicherzustellen, dass alles funktioniert:

- [ ] Claude Code erfolgreich installiert
- [ ] `claude --version` funktioniert
- [ ] PATH-Variable korrekt gesetzt
- [ ] Erstes "Hallo Welt" ausgeführt
- [ ] API Key konfiguriert (optional)
- [ ] Editor-Integration eingerichtet
- [ ] Erstes Projekt erstellt
- [ ] Der KI Heroes Community beigetreten

---

## 🚀 Nächste Schritte

Herzlichen Glückwunsch! Du hast Claude Code erfolgreich installiert! 🎉

### Was nun?
1. **[Erste Schritte Guide](./01-erste-schritte.md)** - Lerne die Grundlagen
2. **[Basis-Befehle](./02-basis-befehle.md)** - Die wichtigsten Kommandos
3. **[Sub-Agents verstehen](./03-sub-agents-meistern.md)** - Der Game-Changer
4. **[Community beitreten](https://www.skool.com/ki-heroes)** - Hilfe und Austausch

---

## 💬 Hilfe & Support

Brauchst du Hilfe? Die KI Heroes Community ist für dich da!

- 📌 **[Community Forum](https://www.skool.com/ki-heroes)**
- 🌐 **[Website](https://ki-heroes.net)**
- 📹 **[Video Tutorials](https://www.skool.com/ki-heroes)**

---

<div align="center">

### 💖 Erstellt von Oliver Hees für die KI Heroes Community

**[🏠 ki-heroes.net](https://ki-heroes.net) | [👥 Community](https://www.skool.com/ki-heroes)**

</div>