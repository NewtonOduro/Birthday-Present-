# 🌹 Nana Akua Birthday Website

> *A romantic, fully self-contained birthday surprise built with love by Newton*

---

## 📖 About This Project

This is a beautiful, interactive birthday website created as a personal surprise gift for **Nana Akua** from **Newton**. It is a single HTML file that runs entirely in any web browser — no internet connection required after download, no server setup needed, no installation.

The website features a blue elegant theme, animated truck wallpaper slideshow, embedded photos, a birthday song, love poetry with voice reading, and much more — all packed into one file.

---

## ✨ Features

### 🎆 Fireworks Animation
Colourful blue fireworks burst across the screen automatically when the page first loads, setting a celebratory mood right away.

### 🚛 Truck Wallpaper Slideshow (Hero Section)
The very first screen Nana Akua sees features a full-screen rotating slideshow of truck wallpapers including:
- Ram 1500
- Ford F-150
- Chevy Silverado
- GMC Sierra
- Toyota Tundra

Slides rotate every 5 seconds with smooth fade transitions. Clickable dot indicators allow manual navigation between trucks. The truck name is displayed in the corner of the hero.

### 📷 Photo Gallery
Four large portrait-friendly photo slots displaying Nana Akua's photos at their full natural size. The layout uses a 2-column grid with the first photo spanning the full width. All 4 of Nana Akua's photos are embedded directly into the website.

### 🎵 Music Player — Céline Dion: The Power of Love
The birthday song **"The Power of Love"** by Céline Dion is embedded directly into the website. A native browser audio player is shown with full controls — play, pause, seek, and volume. The song requires no upload or internet connection.

### 🎂 Interactive Birthday Cake
An animated SVG birthday cake with three flickering candle flames. Clicking the cake blows out the candles with a smooth animation, sends a wish to the stars, and triggers a burst of fireworks.

### 💌 Letter from Newton
A beautifully styled personal love letter from Newton to Nana Akua, formatted like a real handwritten letter with elegant typography inside a decorative card.

### 🎤 Love Poetry with Voice Reading
A three-stanza poem written specially for Nana Akua. A "Listen to the poem" button reads the poem aloud using the browser's built-in text-to-speech engine. The button toggles to stop reading at any time.

### 🎁 Surprise Reveal Button
A glowing button hides a secret message for Nana Akua. Pressing it reveals the hidden message with a smooth animation and a burst of fireworks. Pressing again hides it.

### ⏳ Countdown Timer
A live ticking countdown showing exactly how many **days, hours, minutes and seconds** remain until Nana Akua's next birthday. Updates every second in real time.

### 📝 Guestbook — Birthday Wishes
Friends and family can type their name and a birthday wish for Nana Akua. Each wish is added to a growing list with the sender's name and the time it was submitted. Every submitted wish triggers a small fireworks celebration.

---

## 🗂️ Project Files

| File | Description |
|------|-------------|
| `nana_akua_birthday.html` | The complete birthday website — open this in Chrome |
| `app.py` | Python Flask backend server (optional, for hosting online) |
| `requirements.txt` | Python dependencies for the backend |
| `README.md` | This file |

---

## 🚀 How to Open the Website

### Option 1 — Open Directly in Chrome (Easiest)
1. Download `nana_akua_birthday.html` to your computer or phone
2. Double-click the file
3. It opens in Google Chrome automatically
4. Everything works instantly — photos, music, animations, all features

No internet. No setup. No installation. Just open and enjoy. ✅

### Option 2 — Run with Python Backend (For Sharing a Link)
Use this if you want to share a link with Nana Akua so she can open it from her own phone.

**Step 1 — Install dependencies:**
```bash
pip install flask flask-cors
```

**Step 2 — Run the server:**
```bash
python app.py
```

**Step 3 — Open in Chrome:**
```
http://localhost:5000
```

**Step 4 — Share publicly using ngrok:**
```bash
ngrok http 5000
```
This gives you a public link like `https://abc123.ngrok.io` that Nana Akua can open in Chrome from anywhere. 🌍

### Option 3 — Free Online Hosting
Deploy for free on platforms like:
- [Render](https://render.com) — free tier available
- [Railway](https://railway.app) — simple deployment
- [Netlify](https://netlify.com) — drag and drop the HTML file

---

## 🛠️ Backend API Reference (app.py)

The Flask backend provides a full REST API for managing the website's media content.

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Serves the birthday website |
| POST | `/api/visit` | Logs a visitor and returns total count |
| GET | `/api/visitors` | Returns total visitor count |
| GET | `/api/photos` | Lists all uploaded photos |
| POST | `/api/photos/upload` | Upload a photo (max 10MB) |
| DELETE | `/api/photos/<id>` | Delete a photo |
| GET | `/api/music` | Lists all uploaded songs |
| POST | `/api/music/upload` | Upload a song (max 50MB) |
| DELETE | `/api/music/<id>` | Delete a song |
| GET | `/api/poem` | Get the current poem text |
| PUT | `/api/poem` | Update the poem text |
| GET | `/api/health` | Server health check |

### File Storage
Uploaded files are stored locally under an `uploads/` folder:
```
uploads/
  ├── photos/
  └── music/
```

### Database
All metadata is stored in a local SQLite database (`birthday.db`) which is created automatically on first run.

---

## 🎨 Tech Stack

| Technology | Purpose |
|------------|---------|
| HTML5 | Website structure |
| CSS3 | Styling, animations, slideshow, layout |
| JavaScript (Vanilla) | Fireworks, slideshow, cake, countdown, guestbook, voice |
| Web Speech API | Poetry voice reading |
| Canvas API | Fireworks particle animation |
| Python 3 | Backend server |
| Flask | Web framework for the API |
| SQLite | Lightweight database for media metadata |
| Unsplash | Truck wallpaper images |
| Base64 | Embedding photos and music directly into the HTML |

---

## 🎨 Design

- **Theme:** Romantic & elegant blue
- **Primary colour:** `#1a6fc4` (Royal Blue)
- **Background:** Deep navy dark `#020d1a`
- **Fonts:** Playfair Display (headings & poetry), Lato (body text)
- **Animations:** Falling petals, fireworks, flickering candles, slideshow fade, countdown

---

## 📸 Embedded Content

All content is embedded directly into the HTML file so it works offline:

| Content | Details |
|---------|---------|
| Photo 1 | Nana Akua — white blazer, colourful painted background |
| Photo 2 | Nana Akua — white blazer, orange/red background |
| Photo 3 | Nana Akua — black floral dress |
| Photo 4 | Nana Akua — casual blue shirt with braids |
| Song | Céline Dion — The Power of Love (MP3) |

---

## 💡 Customisation Tips

- **Change the poem** — Edit the poem text inside `#poetry` section in the HTML
- **Change the letter** — Edit the letter paragraphs inside `#letter` section
- **Add more photos** — Click any photo slot in the gallery while viewing in Chrome
- **Change the song** — Click the "Upload your song" button in the music section
- **Update the surprise message** — Find the `surprise-msg` div in the HTML and edit the text
- **Change truck wallpapers** — Edit the `trucks` array in the JavaScript section

---

## 👨‍💻 Built By

| | |
|--|--|
| **Creator** | Newton |
| **For** | Nana Akua |
| **Occasion** | Her Birthday 🎂 |
| **Made with** | Love, HTML, CSS, JavaScript & Python 💙 |

---

> *"In a world that rushes past like wind, you are the stillness, the calm within."*
> 
> — From the birthday poem, written for Nana Akua

---

🌹 *Happy Birthday, Nana Akua — from Newton, with all his love.* 💙
