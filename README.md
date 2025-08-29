# 🚀 Claude Code Cheat Sheet

<div align="center">

## 🎯 Von Oliver Hees für die KI Heroes Community

[![KI Heroes Community](https://img.shields.io/badge/KI%20Heroes-Community-FF6B6B?style=for-the-badge)](https://www.skool.com/ki-heroes)
[![Website](https://img.shields.io/badge/Website-ki--heroes.net-4ECDC4?style=for-the-badge)](https://ki-heroes.net)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Official%20Guide-95E1D3?style=for-the-badge)](https://claude.ai/code)

**[🇩🇪 Deutsch](#deutsch) | [🇬🇧 English](#english)**

---

### 💡 **Das praxisorientierte Claude Code Referenzwerk für die KI Heroes Community**

</div>

---

## Deutsch

### 🎓 Willkommen bei KI Heroes!

Dies ist das **Claude Code Cheat Sheet** - speziell entwickelt für unsere KI Heroes Community. Hier findest du alle wichtigen Informationen und Best Practices zu Claude Code, basierend auf der offiziellen Anthropic Dokumentation.

### 🌟 Was bietet dieses Cheat Sheet?

- ✅ **Offizielle Features** - Nur verifizierte Funktionen aus der Anthropic Dokumentation
- ✅ **Praxisorientiert** - Echte Anwendungsbeispiele und Workflows
- ✅ **Sub-Agents erklärt** - Verstehe und nutze die verfügbaren Sub-Agents
- ✅ **Best Practices** - Bewährte Methoden aus der Community
- ✅ **Zweisprachig** - Komplett auf Deutsch und Englisch verfügbar

### 📚 Schnellstart

```bash
# Claude Code Installation (macOS/Linux/WSL)
curl -fsSL https://claude.ai/install.sh | bash

# Oder via NPM
npm install -g @anthropic-ai/claude-code

# Windows PowerShell
irm https://claude.ai/install.ps1 | iex

# Installation überprüfen
claude doctor
```

### 🤖 Verfügbare Sub-Agents

Claude Code bietet spezialisierte Sub-Agents für verschiedene Aufgaben:

| Sub-Agent | Zweck | Anwendungsbereich |
|-----------|-------|-------------------|
| **Code Reviewer** | Code-Qualität & Sicherheit | Überprüft Code auf Best Practices, Sicherheitslücken und Optimierungspotential |
| **Debugger** | Fehlerbehebung | Root-Cause-Analyse, systematische Fehlersuche |
| **Data Scientist** | Datenanalyse | SQL-Queries, BigQuery-Analysen, Datenverarbeitung |

### 🛠️ Core Features

#### **Code-Verständnis & Navigation**
- Neue Codebasen schnell verstehen
- Relevanten Code effizient finden
- Bugs systematisch beheben
- Code refaktorieren und optimieren

#### **Workflow-Tools**
- **Plan Mode** - Sichere Code-Analyse ohne direkte Änderungen
- **Extended Thinking** - Komplexe Problemlösung mit erweitertem Kontext
- **Git-Integration** - Nahtlose Versionskontrolle
- **Custom Commands** - Eigene Befehle definieren
- **Hooks** - Event-basierte Automatisierung

### 📋 Wichtige Befehle

```bash
# Claude Code starten
claude

# Installation verifizieren
claude doctor

# Updates installieren
claude update

# Auto-Updates deaktivieren
claude config set autoUpdates false --global
```

### 🔧 Sub-Agent Konfiguration

Sub-Agents können mit YAML-Frontmatter in Markdown-Dateien konfiguriert werden:

```yaml
---
name: mein-code-reviewer
type: code-reviewer
tools:
  - read
  - edit
  - bash
system_prompt: |
  Du bist ein Code-Review Spezialist.
  Fokussiere dich auf Sicherheit und Performance.
---
```

### 🚀 Deployment-Optionen

Claude Code unterstützt verschiedene Deployment-Szenarien:

- **Amazon Bedrock** - Enterprise AWS Integration
- **Google Vertex AI** - Google Cloud Platform
- **Corporate Proxy** - Unternehmensnetzwerke
- **LLM Gateway** - Custom API Endpoints
- **DevContainer** - Containerisierte Entwicklungsumgebungen

### 💻 Praktische Beispiele

#### Beispiel 1: Code Review mit Sub-Agent

```bash
# Code Review für ein Projekt
claude "Bitte überprüfe meinen Code mit dem Code Reviewer Sub-Agent"
```

#### Beispiel 2: Debugging Session

```bash
# Fehleranalyse starten
claude "Hilf mir diesen Bug zu finden mit dem Debugger Sub-Agent"
```

#### Beispiel 3: Datenanalyse

```bash
# SQL-Analyse mit Data Scientist
claude "Analysiere diese Datenbankabfrage mit dem Data Scientist Sub-Agent"
```

### 📊 System-Anforderungen

| Komponente | Minimum | Empfohlen |
|------------|---------|-----------|
| **OS** | macOS 10.15+, Ubuntu 20.04+, Windows 10+ | Aktuelle Versionen |
| **RAM** | 4GB | 8GB+ |
| **Node.js** | 18+ | Neueste LTS |
| **Internet** | Erforderlich | Stabile Verbindung |

### 🔐 Sicherheitsfeatures

- **Berechtigungsbasierte Architektur** - Granulare Zugriffskontrolle
- **Prompt Injection Protection** - Schutz vor Manipulation
- **Konfigurierbare Zugriffskontrolle** - Anpassbare Sicherheitsrichtlinien
- **Event-Logging** - Vollständige Audit-Trails

### 📈 Monitoring & Analytics

- Nutzungsmetriken verfolgen mit `/cost`
- Team-Analytics Dashboard
- Performance-Monitoring
- Kostenkontrolle und Budgetierung

### 🤝 Community & Support

- 🌐 **Website**: [ki-heroes.net](https://ki-heroes.net)
- 👥 **Community**: [Skool KI Heroes](https://www.skool.com/ki-heroes)
- 📚 **Offizielle Docs**: [docs.anthropic.com](https://docs.anthropic.com/en/docs/claude-code/overview)
- 🐛 **Feedback**: `/bug` Befehl in Claude Code

### 🎯 Best Practices

1. **Plan Mode nutzen** - Analysiere Code sicher bevor du Änderungen vornimmst
2. **Sub-Agents gezielt einsetzen** - Nutze spezialisierte Agents für spezifische Aufgaben
3. **Hooks konfigurieren** - Automatisiere wiederkehrende Aufgaben
4. **Kosten im Blick behalten** - Nutze `/cost` für Kostenkontrolle
5. **Regelmäßige Updates** - Halte Claude Code aktuell mit `claude update`

---

## English

### 🎓 Welcome to KI Heroes!

This is the **Claude Code Cheat Sheet** - specially developed for our KI Heroes Community. Here you'll find all important information and best practices for Claude Code, based on the official Anthropic documentation.

### 🌟 What does this Cheat Sheet offer?

- ✅ **Official Features** - Only verified functions from Anthropic documentation
- ✅ **Practice-oriented** - Real use cases and workflows
- ✅ **Sub-Agents explained** - Understand and use available Sub-Agents
- ✅ **Best Practices** - Proven methods from the community
- ✅ **Bilingual** - Complete in German and English

### 📚 Quick Start

```bash
# Claude Code Installation (macOS/Linux/WSL)
curl -fsSL https://claude.ai/install.sh | bash

# Or via NPM
npm install -g @anthropic-ai/claude-code

# Windows PowerShell
irm https://claude.ai/install.ps1 | iex

# Verify installation
claude doctor
```

### 🤖 Available Sub-Agents

Claude Code offers specialized Sub-Agents for various tasks:

| Sub-Agent | Purpose | Application Area |
|-----------|---------|------------------|
| **Code Reviewer** | Code Quality & Security | Reviews code for best practices, security vulnerabilities, and optimization potential |
| **Debugger** | Troubleshooting | Root-cause analysis, systematic bug finding |
| **Data Scientist** | Data Analysis | SQL queries, BigQuery analyses, data processing |

### 🛠️ Core Features

#### **Code Understanding & Navigation**
- Quickly understand new codebases
- Efficiently find relevant code
- Systematically fix bugs
- Refactor and optimize code

#### **Workflow Tools**
- **Plan Mode** - Safe code analysis without direct changes
- **Extended Thinking** - Complex problem solving with extended context
- **Git Integration** - Seamless version control
- **Custom Commands** - Define your own commands
- **Hooks** - Event-based automation

### 📋 Important Commands

```bash
# Start Claude Code
claude

# Verify installation
claude doctor

# Install updates
claude update

# Disable auto-updates
claude config set autoUpdates false --global
```

### 🔧 Sub-Agent Configuration

Sub-Agents can be configured with YAML frontmatter in Markdown files:

```yaml
---
name: my-code-reviewer
type: code-reviewer
tools:
  - read
  - edit
  - bash
system_prompt: |
  You are a code review specialist.
  Focus on security and performance.
---
```

### 🚀 Deployment Options

Claude Code supports various deployment scenarios:

- **Amazon Bedrock** - Enterprise AWS Integration
- **Google Vertex AI** - Google Cloud Platform
- **Corporate Proxy** - Enterprise networks
- **LLM Gateway** - Custom API endpoints
- **DevContainer** - Containerized development environments

### 💻 Practical Examples

#### Example 1: Code Review with Sub-Agent

```bash
# Code review for a project
claude "Please review my code with the Code Reviewer Sub-Agent"
```

#### Example 2: Debugging Session

```bash
# Start error analysis
claude "Help me find this bug with the Debugger Sub-Agent"
```

#### Example 3: Data Analysis

```bash
# SQL analysis with Data Scientist
claude "Analyze this database query with the Data Scientist Sub-Agent"
```

### 📊 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **OS** | macOS 10.15+, Ubuntu 20.04+, Windows 10+ | Latest versions |
| **RAM** | 4GB | 8GB+ |
| **Node.js** | 18+ | Latest LTS |
| **Internet** | Required | Stable connection |

### 🔐 Security Features

- **Permission-based Architecture** - Granular access control
- **Prompt Injection Protection** - Protection against manipulation
- **Configurable Access Control** - Customizable security policies
- **Event Logging** - Complete audit trails

### 📈 Monitoring & Analytics

- Track usage metrics with `/cost`
- Team analytics dashboard
- Performance monitoring
- Cost control and budgeting

### 🤝 Community & Support

- 🌐 **Website**: [ki-heroes.net](https://ki-heroes.net)
- 👥 **Community**: [Skool KI Heroes](https://www.skool.com/ki-heroes)
- 📚 **Official Docs**: [docs.anthropic.com](https://docs.anthropic.com/en/docs/claude-code/overview)
- 🐛 **Feedback**: `/bug` command in Claude Code

### 🎯 Best Practices

1. **Use Plan Mode** - Analyze code safely before making changes
2. **Deploy Sub-Agents strategically** - Use specialized agents for specific tasks
3. **Configure Hooks** - Automate recurring tasks
4. **Keep costs in check** - Use `/cost` for cost control
5. **Regular updates** - Keep Claude Code current with `claude update`

---

<div align="center">

### 💖 Created with passion by Oliver Hees for the KI Heroes Community

**[🏠 ki-heroes.net](https://ki-heroes.net) | [👥 Community](https://www.skool.com/ki-heroes)**

</div>