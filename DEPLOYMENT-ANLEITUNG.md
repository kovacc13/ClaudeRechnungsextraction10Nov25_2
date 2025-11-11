# 🚀 EINFACHE DEPLOYMENT ANLEITUNG

## ✅ WICHTIG: Richtige Datei-Struktur

Die ZIP-Datei enthält bereits die **richtige Struktur**:

```
rechnung-extraktor-RICHTIG/
├── api/
│   └── extract.js          ← Backend (MUSS in "api" Ordner!)
├── index.html              ← Hauptseite
├── package.json            ← NPM Config
├── vercel.json             ← Vercel Config
└── README.md               ← Diese Anleitung
```

---

## 📋 SCHRITT-FÜR-SCHRITT ANLEITUNG

### **Schritt 1: ZIP entpacken**
1. Rechtsklick auf `rechnung-extraktor-RICHTIG.zip`
2. "Entpacken" oder "Extract All"
3. Du bekommst einen Ordner `rechnung-extraktor-RICHTIG`

---

### **Schritt 2: Zu Vercel gehen**
1. Öffne: https://vercel.com
2. Klicke **"Sign Up"** (oder Login falls du schon registriert bist)
3. Registriere dich mit:
   - GitHub (empfohlen)
   - Google
   - Email

---

### **Schritt 3: Neues Projekt erstellen**
1. Klicke auf **"Add New"** (oben rechts)
2. Wähle **"Project"**
3. Klicke **"Continue with GitHub"** ODER
4. Scrolle runter und klicke **"Browse"** (für direkten Upload)

---

### **Schritt 4A: MIT GitHub (empfohlen)**

**4.1 GitHub Repository erstellen:**
1. Gehe zu https://github.com/new
2. Name: `rechnung-extraktor`
3. Klicke "Create repository"

**4.2 Dateien hochladen:**
1. Klicke "uploading an existing file"
2. Ziehe ALLE Dateien aus dem entpackten Ordner rein:
   - Den ganzen `api` Ordner (wichtig!)
   - `index.html`
   - `package.json`
   - `vercel.json`
   - `README.md`
3. Klicke "Commit changes"

**4.3 Mit Vercel verbinden:**
1. Zurück zu Vercel
2. Wähle dein GitHub Repository
3. Klicke "Deploy"
4. **Warte 1-2 Minuten**

---

### **Schritt 4B: OHNE GitHub (direkter Upload)**

1. Bei Vercel: Klicke "Browse"
2. Wähle den **GANZEN entpackten Ordner** aus
3. Klicke "Upload"
4. Klicke "Deploy"
5. **Warte 1-2 Minuten**

---

### **Schritt 5: Fertig! 🎉**

Du bekommst eine URL wie:
```
https://rechnung-extraktor-abc123.vercel.app
```

**Diese URL sofort testen:**
1. Öffne die URL
2. Gib deinen Claude API Key ein (von https://console.anthropic.com)
3. Lade eine Test-PDF hoch
4. Klicke "Rechnung extrahieren"

---

## 🔍 VERCEL DASHBOARD CHECKEN

Nach dem Deploy, prüfe in Vercel:

1. **Functions Tab:**
   - Sollte zeigen: `api/extract.js` ✅
   - Falls NICHT: Dateien falsch hochgeladen

2. **Logs Tab:**
   - Bei Fehler: Hier siehst du was schief läuft

---

## ⚠️ HÄUFIGE FEHLER & LÖSUNGEN

### Problem: "Failed to fetch"
**Ursache:** Backend-Datei nicht im `api/` Ordner
**Lösung:**
1. Lösche das Projekt in Vercel
2. Erstelle neues Projekt
3. Stelle sicher, dass `extract.js` in einem Ordner namens `api` ist

### Problem: "API Key funktioniert nicht"
**Lösung:**
1. Gehe zu https://console.anthropic.com
2. Erstelle neuen API Key
3. Key muss mit `sk-ant-` beginnen
4. Kopiere den GANZEN Key

### Problem: "Module not found: @anthropic-ai/sdk"
**Lösung:**
1. Prüfe ob `package.json` hochgeladen ist
2. Vercel installiert automatisch beim Deploy
3. Warte 2-3 Minuten nach Deploy

---

## 💰 KOSTEN

- **Vercel Hosting:** KOSTENLOS ✅
- **Claude API:** Erste $5 gratis = 125 Rechnungen
- **Danach:** ~€0.04 pro Rechnung

---

## 🎯 NACH DEM DEPLOY

### Eigene Domain verbinden (optional)
1. Domain kaufen (z.B. bei Namecheap)
2. In Vercel: Settings → Domains
3. Domain hinzufügen
4. DNS wie angezeigt konfigurieren

Beispiel: `rechnung.deine-firma.at`

---

## 📞 SUPPORT

Falls es nicht klappt:
1. Screenshot vom Vercel Dashboard machen
2. Screenshot vom Fehler machen
3. Claude fragen und Screenshots zeigen

---

## ✅ CHECKLISTE BEIM DEPLOY

- [ ] ZIP entpackt
- [ ] `api/` Ordner existiert
- [ ] `api/extract.js` darin
- [ ] Alle 5 Dateien hochgeladen
- [ ] Vercel zeigt "Deploy successful"
- [ ] URL funktioniert
- [ ] API Key eingegeben
- [ ] Test-PDF funktioniert

**Wenn alle Häkchen gesetzt: 🎉 FERTIG!**
