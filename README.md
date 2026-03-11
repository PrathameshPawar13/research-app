# 🔬 Research Agent

An AI-powered 3-step research agent. Powered by **Groq** (free, no credit card needed).

## Project Structure

```
research-agent/
├── api/
│   └── research.js      ← Node.js backend (proxies to Groq)
├── public/
│   └── index.html       ← Frontend
├── vercel.json          ← Vercel deployment config
├── package.json
└── README.md
```

---

## 🚀 Deploy in 10 Minutes (Completely Free)

### Step 1 — Get a FREE Groq API Key (no credit card)
1. Go to https://console.groq.com
2. Sign up for free (just an email, no credit card)
3. Click API Keys → Create API Key
4. Copy the key (starts with gsk_...)

### Step 2 — Push to GitHub
1. Go to https://github.com and create a free account
2. Click New Repository → name it research-agent → Public → Create
3. Click "uploading an existing file" and drag in all files from this zip
   - Keep the folder structure: api/research.js, public/index.html, etc.
4. Click Commit changes

### Step 3 — Deploy on Vercel (free)
1. Go to https://vercel.com → sign up with your GitHub account
2. Click Add New → Project
3. Select your research-agent repo → click Import
4. Leave all settings as default → click Deploy
5. Wait ~30 seconds ✅

### Step 4 — Add your Groq Key
1. In Vercel → your project → Settings → Environment Variables
2. Add:
   - Name:  GROQ_API_KEY
   - Value: your key from Step 1 (gsk_...)
3. Click Save
4. Go to Deployments → three dots → Redeploy

### Done!
Your agent is live at https://your-project.vercel.app

---

## Cost Breakdown

- Vercel hosting:           Free forever
- Groq API (LLaMA 3.3 70B): Free tier — 14,400 requests/day
- Domain (.vercel.app):     Free

Total: $0

---

## How It Works

The agent runs 3 sequential AI calls powered by LLaMA 3.3 70B on Groq:

1. Plan    — AI decides the research angle and 3 key questions to answer
2. Research — AI writes a full summary and extracts 4 key facts
3. Relate  — AI suggests 4 related topics to explore next

The backend (api/research.js) keeps your API key safe on the server — never exposed to the browser.
