# 🎓 UPSC Quiz Hub — GitHub Setup Guide

## 📁 Folder Structure (GitHub par aise rakho)

```
upsc-quiz-hub/                    ← Your GitHub Repository
│
├── index.html                    ← MAIN PAGE (ye file)
│
├── geography/
│   ├── AtmoGeo_Quiz_62Q.html     ← Physical Geography & Climatology
│   ├── RiverIQ_Quiz_44Q.html     ← Rivers & Lakes
│   └── AgriIndia_Quiz_43Q.html   ← Indian Agriculture
│
├── history/
│   ├── AncientIndia_Quiz.html    ← (add karo jab ready ho)
│   ├── MedievalIndia_Quiz.html
│   └── ModernIndia_Quiz.html
│
├── polity/
│   ├── Constitution_Quiz.html
│   └── Parliament_Quiz.html
│
├── economy/
│   └── EconBasics_Quiz.html
│
└── science/
    └── SciTech_Quiz.html
```

---

## 🚀 Step-by-Step: GitHub par Upload Karo

### Step 1 — GitHub Account & Repository
1. **github.com** par jao → Sign In karo
2. Top right `+` button → **"New repository"** click karo
3. Repository name: `upsc-quiz-hub`
4. **Public** select karo (GitHub Pages ke liye)
5. ✅ "Add a README file" check karo
6. **"Create repository"** click karo

---

### Step 2 — Files Upload Karo

#### Option A: Browser se (Simplest)
1. Repository page par jao
2. **"Add file"** → **"Upload files"** click karo
3. `index.html` pehle upload karo
4. Phir `geography/` folder ke liye:
   - "Upload files" → apne HTML files drag karo
   - **Commit message** mein likho: `geography/AtmoGeo_Quiz_62Q.html`
   - ⚠️ GitHub browser upload se folders automatically nahi bante

#### Option B: GitHub Desktop (Recommended — Easy!)
1. **desktop.github.com** se GitHub Desktop download karo
2. **"Clone repository"** → apna `upsc-quiz-hub` select karo
3. Local folder mein exactly wahi structure banao jo upar diya hai
4. Files wahan rakho
5. GitHub Desktop mein **"Commit to main"** → **"Push origin"**

#### Option C: Git Command Line
```bash
git clone https://github.com/YOUR_USERNAME/upsc-quiz-hub.git
cd upsc-quiz-hub

# Folders banao
mkdir geography history polity economy science

# Files move karo
# (apni files yahan rakho)

git add .
git commit -m "Add UPSC quiz files"
git push origin main
```

---

### Step 3 — GitHub Pages Enable Karo

1. Repository page par jao
2. **Settings** tab click karo (top menu mein)
3. Left sidebar mein **"Pages"** click karo
4. **Source** section mein:
   - Branch: **main** select karo
   - Folder: **/ (root)** select karo
5. **Save** click karo

✅ 2-3 minutes baad aapka site live hoga:
```
https://YOUR_USERNAME.github.io/upsc-quiz-hub/
```

---

## ✏️ Naya Quiz Add Karna (Super Easy!)

### Step 1 — HTML file ready karo
- Claude se naya quiz banwao
- File ko save karo apne computer par

### Step 2 — File upload karo
- GitHub par jaake sahi folder mein upload karo
  - Geography quiz → `geography/` folder
  - History quiz → `history/` folder

### Step 3 — index.html update karo
`index.html` file open karo, `quizData` array mein yeh add karo:

```javascript
{
  subject: "geography",          // geography / history / polity / economy / science
  title: "GeoMaster",           // Quiz ka naam
  subtitle: "Geomorphology PYQ", // Short description
  emoji: "🌋",                  // Emoji
  questions: 37,                 // Kitne questions
  minutes: 25,                   // Time limit
  years: "2000–2023",           // Year range
  difficulty: "med",             // easy / med / hard
  path: "geography/GeoMaster_Quiz_37Q.html",  // ← FILE KA PATH
  tags: ["Geomorphology","Rocks","Landforms"], // Topics
  color: "var(--geo)"           // Color variable
},
```

### Step 4 — Coming Soon → Live banana
Jab file ready ho, sirf `coming: true` hata do:
```javascript
// Before (coming soon):
{ ..., coming: true }

// After (live!):
{ ..., }  // bas coming: true remove karo
```

---

## 🎨 Subject Color Codes

| Subject    | Variable      | Color     |
|-----------|---------------|-----------|
| Geography  | `var(--geo)`  | 🟢 Teal   |
| History    | `var(--his)`  | 🟡 Amber  |
| Polity     | `var(--pol)`  | 🔵 Violet |
| Economy    | `var(--eco)`  | 🟢 Emerald|
| Sci & Tech | `var(--sci)`  | 🩷 Pink   |

---

## 📱 Features of the Dashboard

- ✅ **Subject filter** — Geography/History/Polity etc.
- ✅ **Live search** — type karo, cards filter ho jaate hain
- ✅ **Coming Soon** cards — placeholder for future quizzes
- ✅ **Difficulty badge** — Easy/Medium/Hard
- ✅ **Question count + time** shown on every card
- ✅ **Dark themed** matching your quiz style
- ✅ **Mobile friendly**
- ✅ **Click → directly opens quiz** (same tab)

---

## 🔗 Your Live URLs (after setup)

```
Main Page:   https://YOUR_USERNAME.github.io/upsc-quiz-hub/
Geography:   https://YOUR_USERNAME.github.io/upsc-quiz-hub/geography/AtmoGeo_Quiz_62Q.html
Rivers:      https://YOUR_USERNAME.github.io/upsc-quiz-hub/geography/RiverIQ_Quiz_44Q.html
Agriculture: https://YOUR_USERNAME.github.io/upsc-quiz-hub/geography/AgriIndia_Quiz_43Q.html
```

---

## ❓ Troubleshooting

**Quiz open nahi ho raha?**
→ Check karo ki file ka naam index.html ke `path` field se exactly match karta hai (case-sensitive!)

**Images nahi dikh rahi?**
→ Images external links (ibb.co etc.) se aa rahi hain — internet chahiye

**GitHub Pages 404 error?**
→ Settings → Pages mein branch "main" select hai? 2-3 min wait karo after enabling

**Naya quiz main page par nahi dikh raha?**
→ index.html ke `quizData` array mein add kiya? `coming: true` toh nahi hai?

---

*Made with ❤️ for UPSC 2026-27 aspirants*
