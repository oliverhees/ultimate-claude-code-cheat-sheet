# 👶 Erste Schritte mit Claude Code

## 🎯 Von Oliver Hees für die KI Heroes Community

[![KI Heroes Community](https://img.shields.io/badge/KI%20Heroes-Community-FF6B6B?style=for-the-badge)](https://www.skool.com/ki-heroes)
[![Website](https://img.shields.io/badge/Website-ki--heroes.net-4ECDC4?style=for-the-badge)](https://ki-heroes.net)

---

## 🌟 Willkommen zu deiner Claude Code Reise!

Du hast Claude Code installiert? Perfekt! Jetzt zeige ich dir, wie du in nur 30 Minuten zum produktiven Claude Code Nutzer wirst.

> **💡 KI Heroes Tipp:** Arbeite diese Anleitung Schritt für Schritt durch. Jeder Befehl baut auf dem vorherigen auf!

---

## 📋 Was du in diesem Guide lernst

- ✅ Deinen ersten Claude Code Befehl ausführen
- ✅ Mit Projekten und Dateien arbeiten
- ✅ Die wichtigsten Befehle meistern
- ✅ Häufige Anfängerfehler vermeiden
- ✅ Deine Produktivität sofort steigern

---

## 🚀 Dein erster Claude Code Befehl

### Hallo Claude!

Öffne dein Terminal und tippe:

```bash
claude "Hallo Claude! Ich bin neu hier. Was kannst du alles?"
```

Claude wird dir antworten und dir seine Fähigkeiten erklären!

### Lass uns praktisch werden

```bash
# Frage Claude nach dem heutigen Datum
claude "Welcher Tag ist heute?"

# Lass dir einen Witz erzählen
claude "Erzähle mir einen Programmierer-Witz"

# Erkläre ein Konzept
claude "Erkläre mir in einfachen Worten, was eine API ist"
```

---

## 📁 Mit Projekten arbeiten

### Schritt 1: Projekt-Verzeichnis erstellen

```bash
# Erstelle ein neues Projekt
mkdir mein-erstes-projekt
cd mein-erstes-projekt

# Initialisiere ein neues Node.js Projekt
npm init -y
```

### Schritt 2: Claude Code aktivieren

```bash
# Claude über dein Projekt informieren
claude --add-dir . "Das ist mein erstes Projekt. Hilf mir dabei!"

# Oder spezifische Dateien hinzufügen
claude --add-file package.json "Erkläre mir diese Datei"
```

### Schritt 3: Code generieren lassen

```bash
# Erstelle eine einfache App
claude "Erstelle eine einfache Todo-Liste mit HTML und JavaScript"

# Claude erstellt die Dateien für dich!
```

---

## 🎯 Die 10 wichtigsten Befehle für Anfänger

### 1. Hilfe anzeigen
```bash
claude --help
# Zeigt alle verfügbaren Befehle
```

### 2. Mit Dateien arbeiten
```bash
# Datei zu Claude hinzufügen
claude --add-file datei.js "Erkläre diesen Code"

# Mehrere Dateien hinzufügen
claude --add-file file1.js file2.js "Vergleiche diese Dateien"
```

### 3. Mit Verzeichnissen arbeiten
```bash
# Ganzes Verzeichnis hinzufügen
claude --add-dir ./src "Analysiere meine Source-Dateien"

# Rekursiv alle Unterordner
claude --add-dir . --recursive "Verstehe mein ganzes Projekt"
```

### 4. Modell wechseln
```bash
# Zu Opus wechseln (stärkstes Modell)
claude --model opus "Komplexe Aufgabe hier"

# Zu Sonnet wechseln (schneller)
claude --model sonnet "Einfache Aufgabe hier"
```

### 5. Output formatieren
```bash
# Als JSON ausgeben
claude --output-format json "Liste 5 JavaScript Frameworks"

# Als Markdown ausgeben
claude --output-format markdown "Erstelle eine README"
```

### 6. Historie anzeigen
```bash
# Letzte Konversationen anzeigen
claude history

# Vorherige Konversation fortsetzen
claude --continue
```

### 7. Code Review
```bash
# Code reviewen lassen
claude --review "src/app.js" "Überprüfe meinen Code auf Fehler"
```

### 8. Tests generieren
```bash
# Tests für deinen Code erstellen
claude --test "src/calculator.js" "Erstelle Unit Tests"
```

### 9. Dokumentation erstellen
```bash
# Dokumentation generieren
claude --doc "src/" "Erstelle eine API Dokumentation"
```

### 10. Debug-Hilfe
```bash
# Bei Fehlern helfen lassen
claude --debug "error.log" "Hilf mir diesen Fehler zu lösen"
```

---

## 💻 Praktisches Beispiel: Deine erste Web-App

### Schritt 1: Projekt Setup

```bash
# Neues Verzeichnis erstellen
mkdir meine-erste-webapp
cd meine-erste-webapp

# Claude informieren
claude "Ich möchte eine einfache Wetter-App bauen. Lass uns anfangen!"
```

### Schritt 2: HTML erstellen

```bash
claude "Erstelle eine index.html für eine Wetter-App mit modernem Design"
```

### Schritt 3: Styling hinzufügen

```bash
claude "Füge CSS für ein schönes, responsives Design hinzu"
```

### Schritt 4: Funktionalität implementieren

```bash
claude "Implementiere JavaScript, um Wetterdaten von einer API abzurufen"
```

### Schritt 5: Testen

```bash
# Lokalen Server starten
claude "Wie kann ich meine App lokal testen?"

# Claude gibt dir Anweisungen!
```

---

## 🔍 Verstehe Claude's Antworten

### Claude's Ausgabe-Struktur

```markdown
# Claude antwortet normalerweise so:

1. **Erklärung** - Was er tun wird
2. **Code** - Der generierte Code
3. **Anweisungen** - Wie du den Code verwendest
4. **Tipps** - Zusätzliche Hinweise
```

### Code-Blöcke erkennen

```javascript
// Claude markiert Code immer so:
// ```sprache
// code hier
// ```

// Du kannst den Code direkt kopieren!
```

---

## ⚡ Produktivitäts-Tipps

### 1. Nutze Kontext
```bash
# Schlecht
claude "Schreibe eine Funktion"

# Gut
claude --add-file app.js "Schreibe eine Funktion, die zu meiner App passt"
```

### 2. Sei spezifisch
```bash
# Schlecht
claude "Mache es besser"

# Gut
claude "Optimiere die Performance meiner React-Komponente in app.js"
```

### 3. Nutze Claude iterativ
```bash
# Erste Version
claude "Erstelle eine Button-Komponente"

# Verbesserung
claude "Füge Hover-Effekte zum Button hinzu"

# Weitere Verbesserung
claude "Mache den Button barrierefrei"
```

---

## 🚫 Häufige Anfängerfehler vermeiden

### Fehler 1: Zu vage Anfragen
❌ **Falsch:** "Mache eine App"
✅ **Richtig:** "Erstelle eine Todo-App mit React und localStorage"

### Fehler 2: Keinen Kontext geben
❌ **Falsch:** "Fix den Bug"
✅ **Richtig:** "In Zeile 42 von app.js bekomme ich einen TypeError. Hier ist der Code..."

### Fehler 3: Zu viel auf einmal
❌ **Falsch:** "Baue mir Facebook"
✅ **Richtig:** "Erstelle eine Login-Seite mit E-Mail und Passwort"

### Fehler 4: Claude's Grenzen ignorieren
❌ **Falsch:** "Hacke diese Website"
✅ **Richtig:** "Erkläre mir Web-Security Best Practices"

---

## 🎮 Interaktive Übungen

### Übung 1: Hello World Variationen
```bash
# Aufgabe: Lasse Claude "Hello World" in 5 verschiedenen Sprachen schreiben
claude "Schreibe Hello World in Python, JavaScript, Java, Go und Rust"
```

### Übung 2: Code-Erklärung
```bash
# Erstelle eine Datei mystery.js mit diesem Code:
echo 'const x = [1,2,3].map(n => n * 2).filter(n => n > 2)' > mystery.js

# Lasse Claude erklären
claude --add-file mystery.js "Erkläre Schritt für Schritt, was dieser Code macht"
```

### Übung 3: Bug finden
```bash
# Erstelle buggy.js
echo 'function add(a, b) { return a + b }; console.log(add("5", 3))' > buggy.js

# Finde den Bug
claude --add-file buggy.js "Finde und erkläre den Bug in diesem Code"
```

---

## 📈 Dein Fortschritt

Nach diesem Guide kannst du:

- ✅ Claude Code für einfache Aufgaben nutzen
- ✅ Mit Dateien und Projekten arbeiten
- ✅ Die wichtigsten Befehle anwenden
- ✅ Häufige Fehler vermeiden
- ✅ Produktiv mit Claude arbeiten

---

## 🎯 Nächste Schritte

### Level Up!

1. **[Basis-Befehle meistern](./02-basis-befehle.md)** - Werde zum Claude Code Profi
2. **[Sub-Agents verstehen](./03-sub-agents-meistern.md)** - Die wahre Macht von Claude
3. **[Workflow-Patterns](./05-workflow-patterns.md)** - Automatisiere alles

### Community

Teile deine ersten Erfahrungen in der **[KI Heroes Community](https://www.skool.com/ki-heroes)**!

---

## 💡 Bonus-Tipps

### Claude als Lernpartner
```bash
# Lasse dir Konzepte erklären
claude "Erkläre mir Promises in JavaScript wie für ein 5-jähriges Kind"

# Code-Reviews für Lernen nutzen
claude --review mein-code.js "Zeige mir, wie ich diesen Code verbessern kann"
```

### Claude für Debugging
```bash
# Error Messages verstehen
claude "Was bedeutet dieser Fehler: [Error hier einfügen]"

# Lösungsvorschläge bekommen
claude "Wie behebe ich: Cannot read property of undefined"
```

---

<div align="center">

### 🎉 Herzlichen Glückwunsch!

Du hast die ersten Schritte gemeistert! Zeit für die nächste Stufe!

### 💖 Erstellt von Oliver Hees für die KI Heroes Community

**[🏠 ki-heroes.net](https://ki-heroes.net) | [👥 Community](https://www.skool.com/ki-heroes)**

</div>