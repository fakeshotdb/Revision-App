# Revise

A tiny, revision-first planner for the phone. There's no account and no server:
everything is saved on the device it's used on.

**Revision tab (opens by default)**
- First run: enter the questions left in the bank and the exam date.
- It shows one big number: how many questions to do today.
- Log progress either as "I did 40" or "Bank says 890 left", whichever is easier.
- It also shows days left, questions left and the daily pace for the days after
  today. That pace goes down when she does extra.
- Days left counts today but not exam day.

**Admin tab**
- Type a task, tap how long it'll take (5 min – 2 hr+) and how urgent it is
  (Whenever / This week / Urgent).
- Tasks are sorted **urgent first, then shortest first**, so the one at the top
  ("Next up") is always the one to do.
- Tap the circle to tick a task off. Everything can be undone for a few seconds.

## Getting it on the phone

The app is a single static page (a PWA), so it can be hosted for free on GitHub Pages
and added to the home screen like a normal app. It also works offline.

1. On GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
   (Pages on a *private* repo needs a paid GitHub plan. Otherwise make the repo
   public: it holds no personal data, because her data only lives on her phone.)
2. Run the **Deploy to GitHub Pages** workflow (Actions tab), or push to `main`.
   The site appears at `https://<username>.github.io/<repo>/`.
3. **iPhone:** open that link in **Safari** → Share → **Add to Home Screen**.
   **Android:** open it in Chrome → ⋮ → **Add to Home screen / Install app**.
4. Open it from the home-screen icon from now on. Data saved in the home-screen
   app stays on the phone and isn't shared with the Safari tab.

To try it on a laptop: `npx serve .` then open the printed URL.

## Files
- `index.html`: the whole app (HTML, CSS and JS)
- `sw.js`: offline cache
- `manifest.webmanifest`, `icons/`: home-screen name and icon
