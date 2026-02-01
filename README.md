# 🌍 Express Translator  (Express.js + Nodemon)

Welcome, Agent Linguist. Your mission: build a **Translator Website** using:
- ✅ Express.js (server)
- ✅ nodemon (auto-restart dev tool)
- ✅ A real Translation API (MyMemory)

⚠️ IMPORTANT RULE:
- The project code is NOT written inside this README.
- You will COPY the code from `/code-packs/*.txt` into the real project files.

---

## 🎯 Learning Goals
By completing this, you will practice:
- Running an Express server
- Serving a website using `public/`
- Creating your own API route (`/api/translate`)
- Calling an external API from your server
- Using nodemon to speed up development
- Handling errors and returning clean JSON

---

## 🧰 Requirements
- Node.js 18+ (recommended)
- Git + GitHub account
- VS Code or any editor

Check Node version:
```bash
node -v
```

---

## 📦 Step 0 — Create the Project Folder
Open terminal in your desired folder:

```bash
mkdir express-translator
cd express-translator
npm init -y
```

Install dependencies:
```bash
npm install express
npm install --save-dev nodemon
npm install dotenv
```

---

## 📁 Step 1 — Create the Folder Structure
Create these folders/files (empty for now):

```
express-translator/
  server.js
  package.json
  .gitignore
  .env            (optional - do NOT commit this)
  .env.example
  public/
    index.html
    app.js
    styles.css
  code-packs/
    01-server.js.txt
    02-index.html.txt
    03-styles.css.txt
    04-app.js.txt
    05-gitignore.txt
    06-env.example.txt
    07-package-scripts.txt
```

✅  `/code-packs/` files in the repo.  

---

## 🧩 Step 2 — Copy/Paste from the Code Packs (VERY IMPORTANT)
You will open each `.txt` file and copy its full content into the “real” file.

### Copy Map (DO THIS EXACTLY)
1) Copy `/code-packs/01-server.js.txt` ➜ paste into `server.js`  
2) Copy `/code-packs/02-index.html.txt` ➜ paste into `public/index.html`  
3) Copy `/code-packs/03-styles.css.txt` ➜ paste into `public/styles.css`  
4) Copy `/code-packs/04-app.js.txt` ➜ paste into `public/app.js`  
5) Copy `/code-packs/05-gitignore.txt` ➜ paste into `.gitignore`  
6) Copy `/code-packs/06-env.example.txt` ➜ paste into `.env.example`  
7) Copy `/code-packs/07-package-scripts.txt` ➜ use it to update your `package.json` scripts section  

✅ Checkpoint:
- Your folders match the structure above
- Your real files now contain the code

---

## ⚙️ Step 3 — Update package.json Scripts
Open `package.json`, find `"scripts"` and replace it with the version from:

`/code-packs/07-package-scripts.txt`

✅ Checkpoint:
Run:
```bash
npm run dev
```

---

## 🔥 Step 4 — Run the Server (Nodemon Mode)
Start the dev server:
```bash
npm run dev
```

Open:
- http://localhost:3000/health  
You should see JSON like: `Server is alive ✅`

---

## 🌍 Step 5 — Open the Website
Go to:
- http://localhost:3000

You should see:
- A translator UI (textbox, language dropdowns, button, result area)

---

## 🧪 Step 6 — Test the Translation API Route
Open this in your browser (example):

http://localhost:3000/api/translate?text=Hello%20world&from=en&to=it

✅ You should see JSON with:
- `translatedText`
- `history` (last 5 translations)

---

## 📧 Step 7 — Increase Free API Quota (Optional but Recommended)
This API is free but has daily limits unless you provide an email.

### A) Create your `.env` file
Make a file named `.env` in the project root.

### B) Add your email:
```
MYMEMORY_EMAIL=your_email@example.com
```

### C) Restart nodemon
Stop terminal (Ctrl+C) then run again:
```bash
npm run dev
```

---

## ✅ Nodemon Proof Challenge (Required)
Prove nodemon is working:

1) While `npm run dev` is running, open `server.js`
2) Find the `/health` route message
3) Change the text to something funny like:  
   “Server is alive ✅ (and I need coffee ☕)”
4) SAVE the file
5) Refresh:  
   http://localhost:3000/health



---

## 📸 Submission Checklist

1) Home page loaded (translator UI)
2) Successful translation result (on the webpage)
3) `/api/translate` returning JSON in the browser
4) `/health` showing your custom nodemon message


---

## 🆘 Troubleshooting
### “fetch is not defined”
Use Node 18+.

### Port already in use
Change port:
```bash
PORT=3001 npm run dev
```

### API limit reached
Add `.env` with `MYMEMORY_EMAIL=...` and restart.

---

## ✅ Done
You built a mini full-stack app:
- Frontend (HTML/CSS/JS)
- Backend (Express route)
- External API integration
- nodemon dev workflow

Good luck, Agent Linguist. 🕵️‍♂️🌍
