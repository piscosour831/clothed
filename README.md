# clothed

**Anti-fast-fashion clothing longevity intelligence.**

Analyze a garment's tag, compare two garments head-to-head, and ask an expert materials guide anything about cotton, wool, cashmere, silk, polyester, and more — powered by AI, grounded in curated apparel knowledge.

---

## What it does

- **Analyze** — Type in or photograph a clothing tag. Get a longevity estimate, material quality score, brand reputation rating, and manufacturing origin score.
- **Compare** — Put two garments side by side and get a clear recommendation on which will last longer and why.
- **Materials guide** — Chat with an apparel materials expert. Questions are answered from a curated knowledge base first; web search fills in anything beyond it.

---

## Setup (one time only)

You need three things installed on your computer: Node.js, a code editor, and a terminal. Don't worry — this guide walks through each step.

---

### Step 1 — Install Node.js

Node.js is the software that runs the app on your computer.

1. Go to **https://nodejs.org**
2. Download the **LTS** version (the left button — it says "Recommended for most users")
3. Open the downloaded file and follow the installer
4. When it finishes, you're done

**To verify it worked:** Open Terminal (Mac) or Command Prompt (Windows) and type:
```
node --version
```
You should see something like `v20.11.0`. Any number works.

---

### Step 2 — Download this project

**If you have git:**
```
git clone https://github.com/YOUR_USERNAME/clothed.git
cd clothed
```

**If you don't have git:** Click the green **Code** button on the GitHub page → **Download ZIP** → unzip it → open the folder.

---

### Step 3 — Install the app's dependencies

In your terminal, make sure you're inside the `clothed` folder, then run:
```
npm install
```
This downloads the two small packages the server needs (Express and dotenv). It takes about 30 seconds.

---

### Step 4 — Get your Anthropic API key

The app uses Anthropic's Claude AI. You need your own key — this is what keeps your usage private and on your own account.

1. Go to **https://console.anthropic.com**
2. Sign up or log in
3. Click **API Keys** in the left sidebar
4. Click **Create Key**, give it a name like `clothed`, and copy the key

> **Important:** Your API key starts with `sk-ant-`. Keep it private — don't share it or post it anywhere.

---

### Step 5 — Add your API key to the app

1. In the `clothed` folder, find the file called `.env.example`
2. Make a copy of it and rename the copy to `.env` (just `.env` — no `.example`)
3. Open `.env` in any text editor (TextEdit on Mac, Notepad on Windows)
4. Replace `your_api_key_here` with your actual key, so it looks like:
   ```
   ANTHROPIC_API_KEY=sk-ant-xxxxxxxxxxxxxxxx
   ```
5. Save the file

> The `.env` file is listed in `.gitignore` — it will never be uploaded to GitHub. Your key stays on your computer only.

---

### Step 6 — Run the app

In your terminal (inside the `clothed` folder):
```
npm start
```

You should see:
```
  clothed is running!
  Open http://localhost:3000 in your browser
```

Open **http://localhost:3000** in Chrome, Firefox, or Safari. The app is running.

---

## Every time you want to use it

1. Open Terminal / Command Prompt
2. Navigate to the clothed folder: `cd path/to/clothed`
3. Run: `npm start`
4. Open http://localhost:3000

To stop the app, press `Ctrl + C` in the terminal.

---

## Troubleshooting

**"command not found: node"**
Node.js isn't installed or didn't install correctly. Repeat Step 1.

**"Cannot find module 'express'"**
You haven't run `npm install` yet. Run it from inside the clothed folder.

**"API key not configured"**
Your `.env` file is missing or the key is still set to `your_api_key_here`. Repeat Step 5.

**"Could not reach Anthropic API"**
Check your internet connection. If it persists, verify your API key is correct at https://console.anthropic.com.

**The page won't load**
Make sure `npm start` is still running in your terminal. The app only works while that process is active.

---

## Project structure

```
clothed/
├── public/
│   └── index.html      ← the entire frontend (HTML, CSS, JavaScript)
├── server.js           ← local Express server, proxies API calls
├── package.json        ← project metadata and dependencies
├── .env.example        ← template — copy this to .env and add your key
├── .env                ← your actual key (never committed to git)
└── .gitignore          ← keeps .env and node_modules out of git
```

---

## API usage and costs

Each analysis, comparison, or chat message uses your Anthropic API credits. Costs are very low — a typical garment analysis costs less than $0.01. You can monitor your usage at https://console.anthropic.com.

---

## License

MIT — use it, modify it, share it.
