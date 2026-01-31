# BiblioBaby - TikTok Developer App Setup

## 📁 Was in diesem Ordner ist:

- `index.html` - BiblioBaby Landing Page
- `terms.html` - Terms of Service (AGB)
- `privacy.html` - Privacy Policy (Datenschutzerklärung)

## 🚀 SOFORT ONLINE STELLEN (2 Minuten):

### Methode 1: Netlify Drop (SCHNELLSTE - Empfohlen!)

1. Gehe zu: https://app.netlify.com/drop
2. Drag & Drop diesen **gesamten Ordner** (`/tmp/bibliobaby-legal`) auf die Seite
3. Fertig! Du bekommst sofort eine URL wie: `https://random-name.netlify.app`

**Deine URLs werden dann sein:**
- Terms: `https://random-name.netlify.app/terms.html`
- Privacy: `https://random-name.netlify.app/privacy.html`

### Methode 2: GitHub Pages (5 Minuten)

1. Erstelle neues GitHub Repository: `bibliobaby-legal`
2. Lade alle 3 Dateien hoch
3. Settings → Pages → Source: main branch
4. Fertig! URL: `https://dein-username.github.io/bibliobaby-legal/`

---

## 📝 TikTok Developer App - Alle Pflichtfelder:

### 1. **App Icon**
✅ BEREITS GENERIERT - Im Browser öffnen & herunterladen

### 2. **Terms of Service URL**
URL: `https://[deine-netlify-url].netlify.app/terms.html`

### 3. **Privacy Policy URL**
URL: `https://[deine-netlify-url].netlify.app/privacy.html`

### 4. **Platforms**
Auswahl:
- ✅ **Web** (auswählen)
- ✅ **Desktop** (auswählen)
- ❌ Android (nicht auswählen)
- ❌ iOS (nicht auswählen)

### 5. **App Review Explanation** (Copy & Paste dies unten)

```
BiblioBaby is a content creation platform that produces and publishes gentle, developmentally appropriate sensory videos for babies ages 0-3. Our platform automates the creation and publishing process to TikTok, YouTube, and Instagram.

Product: Content Posting API
Scope: video.upload

How it works:
1. Our system creates age-appropriate baby sensory content (animations, music)
2. The Content Posting API automatically publishes videos to our @bibliobaby TikTok channel
3. Content is scheduled 3x daily (7am, 12pm, 7pm) to provide consistent, calming content
4. All content is pre-reviewed for quality and appropriateness before upload
5. We do NOT collect user data - we only publish content to our own channel

Use Cases:
- Publishing gentle sensory videos for babies
- Scheduled content delivery for parents
- Educational content for early childhood development

Target Audience:
- Parents with babies ages 0-3
- Caregivers seeking appropriate sensory content
- Early childhood educators

We comply with TikTok Community Guidelines and all content is baby-safe, non-commercial, and educational.
```

### 6. **Demo Video** (Anleitung unten)

---

## 🎥 DEMO VIDEO ERSTELLEN:

### Quick & Easy Methode (Mac):

```bash
# 1. Öffne Terminal im LALA Engine Ordner
cd /Users/Asisi/Desktop/LALA_Engine

# 2. Starte Dashboard
poetry run lala dashboard

# 3. Öffne TikTok Kanal im Browser
# https://www.tiktok.com/@bibliobaby

# 4. Mach Screen Recording:
# Cmd + Shift + 5
# Wähle "Record Entire Screen"
# Klicke "Record"
```

### Was im Video zu zeigen ist (1-2 Minuten):

**Szene 1: Dashboard (30 Sek)**
- Dashboard öffnen: http://localhost:8000
- Zeige Video-Liste
- Scrolle durch Inhalte

**Szene 2: TikTok Kanal (30 Sek)**
- TikTok Profil öffnen
- Zeige vorhandene Videos

**Szene 3: Upload Script (30 Sek)**
- Terminal öffnen
- `poetry run python scripts/test_tiktok_upload.py`
- Zeige Upload-Bestätigung

**Szene 4: Ergebnis (30 Sek)**
- TikTok aktualisieren
- Zeige dass neues Video erschienen ist

### Video komprimieren (wenn >50MB):

```bash
# Mit ffmpeg
ffmpeg -i input.mov -vcodec h264 -acodec aac -crf 28 output.mp4
```

---

## ✅ CHECKLISTE:

- [x] App Icon generiert (mit DALL-E 3)
- [x] Terms of Service HTML erstellt
- [x] Privacy Policy HTML erstellt
- [x] Landing Page HTML erstellt
- [ ] Hosting setup (Netlify Drop oder GitHub Pages)
- [ ] TikTok App Formular ausfüllen
- [ ] Demo Video aufnehmen
- [ ] TikTok Developer App absenden

---

## 📧 EMAIL ADRESSEN (für die Formulare):

Du kannst diese temporären Email-Adressen verwenden:
- **legal@bibliobaby.com** - (Terms of Service)
- **privacy@bibliobaby.com** - (Privacy Policy)

*Hinweis: Diese müssen nicht existieren, nur im Formular angegeben werden*

---

## 🎨 BRAND ASSETS:

**Farben:**
- Coral: #FFA07A
- Mint: #98FB98
- Cream: #FFF8DC

**Taglines:**
- DE: "Wo kleine Entdecker blühen"
- EN: "Where Little Minds Bloom"

**Character:**
- Name: Bibbi
- Typ: Süßer Bär
- Stil: Minimalistisch, Pixar-Style

---

## 🚀 NÄCHSTE SCHRITTE NACH TIKTOK APPROVAL:

1. Client Key und Client Secret kopieren
2. In `.env` Datei eintragen:
   ```
   TIKTOK_CLIENT_KEY=dein_key
   TIKTOK_CLIENT_SECRET=dein_secret
   ```
3. OAuth Setup ausführen:
   ```bash
   poetry run python scripts/tiktok_oauth_setup.py
   ```

Viel Erfolg! 🎉
