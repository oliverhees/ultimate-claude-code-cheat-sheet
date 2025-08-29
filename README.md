# 🚀 Claude Code Cheat Sheet

<div align="center">

## 🎯 Von Oliver Hees für die KI Heroes Community

[![KI Heroes Community](https://img.shields.io/badge/KI%20Heroes-Community-FF6B6B?style=for-the-badge)](https://www.skool.com/ki-heroes)
[![Website](https://img.shields.io/badge/Website-ki--heroes.net-4ECDC4?style=for-the-badge)](https://ki-heroes.net)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Cheat%20Sheet-95E1D3?style=for-the-badge)](https://claude.ai)

**[🇩🇪 Deutsch](#deutsch) | [🇬🇧 English](#english)**

---

### 💡 **Das umfassende Claude Code Referenzwerk / The Comprehensive Claude Code Reference**

</div>

---

## Deutsch

## 📋 Inhaltsverzeichnis
- [🚀 Installation & Setup](#-installation--setup)
- [🎯 Grundlegende Befehle](#-grundlegende-befehle)
- [📝 Prompt-Techniken](#-prompt-techniken)
- [🔧 Konfiguration](#-konfiguration)
- [💻 Praktische Beispiele](#-praktische-beispiele)
- [🚀 Fortgeschrittene Features](#-fortgeschrittene-features)
- [🎯 Best Practices](#-best-practices)

### 🚀 Installation & Setup

#### Installation
```bash
# macOS/Linux
curl -sL https://install.anthropic.com | sh

# Windows (PowerShell als Administrator)
Invoke-WebRequest -Uri https://install.anthropic.com/windows -UseBasicParsing | Invoke-Expression

# Überprüfung
claude --version
```

#### Erste Schritte
```bash
# Claude REPL starten
claude

# Direkte Abfrage
claude -p "Erkläre mir Python in 3 Sätzen"

# Mit Verzeichnis-Kontext
claude --add-dir ./src "Analysiere diesen Code"
```

### 🎯 Grundlegende Befehle

#### Basis-Befehle
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `claude` | Startet interaktive Sitzung | `claude` |
| `claude -p` | Direkte Prompt-Ausführung | `claude -p "Hallo Welt"` |
| `claude --help` | Zeigt Hilfe | `claude --help` |
| `claude --version` | Zeigt Version | `claude --version` |

#### Kontext-Management
```bash
# Verzeichnis hinzufügen
claude --add-dir ./projekt

# Mehrere Verzeichnisse
claude --add-dir ./src ./tests ./docs

# Datei hinzufügen
claude --add-file README.md

# Mit Kontext arbeiten
claude --add-dir . "Erkläre die Projektstruktur"
```

#### Session-Management
```bash
# Session speichern
claude --save-session meine-session

# Session fortsetzen
claude --resume meine-session
# Oder kurz:
claude -r meine-session

# Session-Liste anzeigen
claude --list-sessions
```

### 📝 Prompt-Techniken

#### Pipe-Integration
```bash
# Git-Logs analysieren
git log --oneline -10 | claude -p "Fasse diese Commits zusammen"

# Fehler analysieren
cat error.log | claude -p "Finde die Ursache"

# JSON verarbeiten
curl api.example.com/data | claude -p "Extrahiere wichtige Metriken"
```

#### Ausgabe-Formate
```bash
# JSON-Format
claude -p "Liste 5 Python-Tipps" --output-format json

# Reiner Text
claude -p "Erkläre REST APIs" --output-format text

# Markdown (Standard)
claude -p "Erstelle eine README"
```

### 🔧 Konfiguration

#### Modell-Auswahl
```bash
# Claude Sonnet (schneller)
claude --model sonnet

# Claude Opus (leistungsstärker)
claude --model opus

# Haiku (schnellste Antworten)
claude --model haiku
```

#### Konfigurationsdatei
Erstelle `~/.claude/config.json`:
```json
{
  "default_model": "sonnet",
  "temperature": 0.7,
  "max_tokens": 4096,
  "output_format": "markdown",
  "auto_save": true
}
```

### 💻 Praktische Beispiele

#### Code-Review
```bash
# Einzelne Datei reviewen
claude --add-file app.py "Review diesen Code auf Best Practices"

# Projekt-Review
claude --add-dir ./src "Führe ein Security-Review durch"

# Diff analysieren
git diff | claude -p "Erkläre diese Änderungen"
```

#### Dokumentation generieren
```bash
# README erstellen
claude --add-dir . "Erstelle eine README.md für dieses Projekt"

# API-Dokumentation
claude --add-file api.py "Generiere OpenAPI Dokumentation"

# Inline-Kommentare
claude --add-file utils.js "Füge JSDoc Kommentare hinzu"
```

#### Debugging
```bash
# Fehler analysieren
claude --add-file error.log "Was verursacht diesen Fehler?"

# Stack Trace verstehen
python app.py 2>&1 | claude -p "Erkläre diesen Stack Trace"

# Performance-Analyse
claude --add-file profile.json "Identifiziere Performance-Bottlenecks"
```

### 🚀 Fortgeschrittene Features

#### Benutzerdefinierte Commands
Erstelle `.claude/commands/translate.md`:
```markdown
---
name: translate
description: Übersetzt Text
params:
  - text: Der zu übersetzende Text
  - target: Zielsprache
---

Übersetze den folgenden Text nach {{target}}:
{{text}}
```

Verwendung:
```bash
claude /translate --text "Hallo Welt" --target "Englisch"
```

#### Workflow-Automatisierung
```bash
# Git Commit Messages
git diff --staged | claude -p "Generiere eine Commit-Message"

# Code-Generation
claude -p "Erstelle einen REST API Endpoint für User-Management" > user_api.py

# Test-Generation
claude --add-file app.py "Schreibe Unit-Tests" > test_app.py
```

#### Batch-Verarbeitung
```bash
# Mehrere Dateien analysieren
for file in *.py; do
  echo "Analysiere $file"
  claude --add-file "$file" "Finde potenzielle Bugs" >> analysis.md
done

# Logs verarbeiten
find ./logs -name "*.log" -exec claude --add-file {} "Zusammenfassung" \; > summary.txt
```

### 🎯 Best Practices

#### 1. Kontext optimieren
```bash
# Gut: Spezifischer Kontext
claude --add-dir ./src/auth "Verbessere die Authentifizierung"

# Schlecht: Zu viel Kontext
claude --add-dir / "Finde Bugs"
```

#### 2. Klare Prompts
```bash
# Gut: Spezifisch und klar
claude -p "Erstelle eine Python-Funktion die Fibonacci-Zahlen bis n berechnet"

# Schlecht: Vage
claude -p "Mach Code"
```

#### 3. Session-Management nutzen
```bash
# Lange Arbeitssitzung speichern
claude --save-session projekt-refactoring

# Später fortsetzen
claude -r projekt-refactoring
```

#### 4. Output richtig nutzen
```bash
# Direkt in Datei speichern
claude -p "Erstelle Dockerfile für Node.js App" > Dockerfile

# JSON für Weiterverarbeitung
claude -p "Liste Dependencies" --output-format json | jq '.dependencies'
```

---

## English

## 📋 Table of Contents
- [🚀 Installation & Setup](#-installation--setup-1)
- [🎯 Basic Commands](#-basic-commands)
- [📝 Prompt Techniques](#-prompt-techniques)
- [🔧 Configuration](#-configuration)
- [💻 Practical Examples](#-practical-examples)
- [🚀 Advanced Features](#-advanced-features)
- [🎯 Best Practices](#-best-practices-1)

### 🚀 Installation & Setup

#### Installation
```bash
# macOS/Linux
curl -sL https://install.anthropic.com | sh

# Windows (PowerShell as Administrator)
Invoke-WebRequest -Uri https://install.anthropic.com/windows -UseBasicParsing | Invoke-Expression

# Verification
claude --version
```

#### Getting Started
```bash
# Start Claude REPL
claude

# Direct query
claude -p "Explain Python in 3 sentences"

# With directory context
claude --add-dir ./src "Analyze this code"
```

### 🎯 Basic Commands

#### Core Commands
| Command | Description | Example |
|---------|-------------|---------|
| `claude` | Starts interactive session | `claude` |
| `claude -p` | Direct prompt execution | `claude -p "Hello World"` |
| `claude --help` | Shows help | `claude --help` |
| `claude --version` | Shows version | `claude --version` |

#### Context Management
```bash
# Add directory
claude --add-dir ./project

# Multiple directories
claude --add-dir ./src ./tests ./docs

# Add file
claude --add-file README.md

# Work with context
claude --add-dir . "Explain the project structure"
```

#### Session Management
```bash
# Save session
claude --save-session my-session

# Resume session
claude --resume my-session
# Or short:
claude -r my-session

# List sessions
claude --list-sessions
```

### 📝 Prompt Techniques

#### Pipe Integration
```bash
# Analyze git logs
git log --oneline -10 | claude -p "Summarize these commits"

# Analyze errors
cat error.log | claude -p "Find the root cause"

# Process JSON
curl api.example.com/data | claude -p "Extract key metrics"
```

#### Output Formats
```bash
# JSON format
claude -p "List 5 Python tips" --output-format json

# Plain text
claude -p "Explain REST APIs" --output-format text

# Markdown (default)
claude -p "Create a README"
```

### 🔧 Configuration

#### Model Selection
```bash
# Claude Sonnet (faster)
claude --model sonnet

# Claude Opus (more powerful)
claude --model opus

# Haiku (fastest responses)
claude --model haiku
```

#### Configuration File
Create `~/.claude/config.json`:
```json
{
  "default_model": "sonnet",
  "temperature": 0.7,
  "max_tokens": 4096,
  "output_format": "markdown",
  "auto_save": true
}
```

### 💻 Practical Examples

#### Code Review
```bash
# Review single file
claude --add-file app.py "Review this code for best practices"

# Project review
claude --add-dir ./src "Perform a security review"

# Analyze diff
git diff | claude -p "Explain these changes"
```

#### Generate Documentation
```bash
# Create README
claude --add-dir . "Create a README.md for this project"

# API documentation
claude --add-file api.py "Generate OpenAPI documentation"

# Inline comments
claude --add-file utils.js "Add JSDoc comments"
```

#### Debugging
```bash
# Analyze errors
claude --add-file error.log "What's causing this error?"

# Understand stack trace
python app.py 2>&1 | claude -p "Explain this stack trace"

# Performance analysis
claude --add-file profile.json "Identify performance bottlenecks"
```

### 🚀 Advanced Features

#### Custom Commands
Create `.claude/commands/translate.md`:
```markdown
---
name: translate
description: Translates text
params:
  - text: Text to translate
  - target: Target language
---

Translate the following text to {{target}}:
{{text}}
```

Usage:
```bash
claude /translate --text "Hello World" --target "German"
```

#### Workflow Automation
```bash
# Git commit messages
git diff --staged | claude -p "Generate a commit message"

# Code generation
claude -p "Create a REST API endpoint for user management" > user_api.py

# Test generation
claude --add-file app.py "Write unit tests" > test_app.py
```

#### Batch Processing
```bash
# Analyze multiple files
for file in *.py; do
  echo "Analyzing $file"
  claude --add-file "$file" "Find potential bugs" >> analysis.md
done

# Process logs
find ./logs -name "*.log" -exec claude --add-file {} "Summarize" \; > summary.txt
```

### 🎯 Best Practices

#### 1. Optimize Context
```bash
# Good: Specific context
claude --add-dir ./src/auth "Improve authentication"

# Bad: Too much context
claude --add-dir / "Find bugs"
```

#### 2. Clear Prompts
```bash
# Good: Specific and clear
claude -p "Create a Python function that calculates Fibonacci numbers up to n"

# Bad: Vague
claude -p "Make code"
```

#### 3. Use Session Management
```bash
# Save long work session
claude --save-session project-refactoring

# Resume later
claude -r project-refactoring
```

#### 4. Use Output Properly
```bash
# Save directly to file
claude -p "Create Dockerfile for Node.js app" > Dockerfile

# JSON for further processing
claude -p "List dependencies" --output-format json | jq '.dependencies'
```

---

## 🔥 Schnellreferenz / Quick Reference

### Deutsch

#### Häufigste Befehle
```bash
# Installation
curl -sL https://install.anthropic.com | sh

# Start
claude

# Mit Kontext
claude --add-dir .

# Prompt ausführen
claude -p "Deine Frage"

# Session speichern/fortsetzen
claude --save-session name
claude -r name
```

#### Tastenkombinationen im REPL
- `Ctrl+C` - Aktuelle Eingabe abbrechen
- `Ctrl+D` - Session beenden
- `↑/↓` - Durch Historie navigieren
- `Tab` - Auto-Vervollständigung

### English

#### Most Common Commands
```bash
# Installation
curl -sL https://install.anthropic.com | sh

# Start
claude

# With context
claude --add-dir .

# Execute prompt
claude -p "Your question"

# Save/resume session
claude --save-session name
claude -r name
```

#### REPL Keyboard Shortcuts
- `Ctrl+C` - Cancel current input
- `Ctrl+D` - End session
- `↑/↓` - Navigate through history
- `Tab` - Auto-completion

---

## 🤝 Community & Support

### Deutsch
- 🌐 **Website**: [ki-heroes.net](https://ki-heroes.net)
- 👥 **Community**: [Skool KI Heroes](https://www.skool.com/ki-heroes)
- 📚 **Offizielle Docs**: [Anthropic Docs](https://docs.anthropic.com)
- 💬 **Discord**: Über die Community-Plattform

### English
- 🌐 **Website**: [ki-heroes.net](https://ki-heroes.net)
- 👥 **Community**: [Skool KI Heroes](https://www.skool.com/ki-heroes)
- 📚 **Official Docs**: [Anthropic Docs](https://docs.anthropic.com)
- 💬 **Discord**: Via community platform

---

<div align="center">

### 💖 Created with passion by Oliver Hees for the KI Heroes Community

**[🏠 ki-heroes.net](https://ki-heroes.net) | [👥 Community](https://www.skool.com/ki-heroes)**

</div>