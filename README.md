# Las Ramblas Digital Sommelier

Mobile-first AI chatbot για το Las Ramblas The Lab. Υποστηρίζει Ελληνικά & Αγγλικά.

## Δομή

```
las-ramblas-bot/
├── public/
│   └── index.html          ← Το frontend (mobile-first)
├── netlify/
│   └── functions/
│       └── chat.js         ← Serverless function (Claude API proxy)
└── netlify.toml
```

## Deploy στο Netlify

### 1. Ανέβασε στο GitHub
```bash
git init
git add .
git commit -m "Las Ramblas Sommelier v1"
git remote add origin https://github.com/YOUR_USERNAME/las-ramblas-bot.git
git push -u origin main
```

### 2. Σύνδεσε με Netlify
- Πήγαινε στο netlify.com → "Add new site" → "Import from Git"
- Επέλεξε το repository
- Build settings: αφησε κενά (το netlify.toml τα ρυθμίζει αυτόματα)

### 3. Πρόσθεσε το API Key
- Netlify Dashboard → Site → **Environment variables**
- Πρόσθεσε: `ANTHROPIC_API_KEY` = το κλειδί σου

### 4. Deploy!
Κάνε redeploy και το site είναι έτοιμο.

## QR Code
Μόλις πάρεις το Netlify URL (π.χ. `las-ramblas-sommelier.netlify.app`),
δημιούργησε QR code στο: https://qr.io ή https://www.qr-code-generator.com

## Κόστος
Χρησιμοποιεί **claude-haiku-4-5** — το πιο οικονομικό μοντέλο.
Εκτιμώμενο κόστος: ~$0.001 ανά μήνυμα (~$1 για 1.000 μηνύματα).
