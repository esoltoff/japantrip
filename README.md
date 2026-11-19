# Japan & Hong Kong itinerary — install on your iPhone

Two ways to do this. The first gives you a real home-screen icon and works
with no signal. The second is a thirty-second fallback with no icon.

---

## A. Home screen icon, works offline (recommended)

The whole folder needs to sit on an HTTPS address. iOS will not add a
downloaded file to the home screen — that is an Apple restriction, not a
limitation of this file.

**1. Put these files online.** Any free static host works. GitHub Pages:

  - Create a free github.com account
  - New repository, name it anything, tick **Public**
  - Upload **all six files** from this folder (index.html, sw.js,
    manifest.webmanifest, icon-180.png, icon-192.png, icon-512.png)
  - Settings -> Pages -> Source: **Deploy from a branch**, branch **main**, folder **/ (root)**
  - Wait a minute or two, then open the URL it gives you

Do not put the files in a subfolder. index.html must be at the top level.

**2. Add it to the home screen.**

  - Open that URL **in Safari** (not Chrome — only Safari can install to the home screen)
  - Let the page finish loading
  - Share button -> scroll down -> **Add to Home Screen** -> Add

**3. Prime the cache before you fly.**

  - Open the icon from the home screen **while you still have wifi**
  - Let it load fully, then swipe through every tab once
  - Turn on Airplane Mode and open it again. If it loads, you are done.

Do this the day before you fly. The offline cache only exists after the app has
been opened online at least once.

## Updating it later

Re-upload the new `index.html` **and** the new `sw.js` together. The version
string at the top of `sw.js` is already bumped for you on every rebuild — this
kit is `japan-itinerary-v34`. Without a new `sw.js`, the phone keeps serving
the old cached copy no matter how many times you reload.

Then open the app twice: once to fetch the update, once to see it. If it still
looks old, close it from the app switcher and reopen.

---

## B. No hosting: keep it in Files

Works completely offline, no account, no setup — you just tap through Files
instead of a home-screen icon.

  - Save `index.html` (or the standalone file) into **Files -> On My iPhone**
  - Tap it. It opens and works, including all tabs and maps.
  - Add the Files app to your dock so it is two taps away

Worth doing **as well as** option A, as a belt-and-braces backup. It depends on
nothing.

---

## Notes

- Everything is self-contained. No fonts, tiles, images or scripts are fetched
  from the internet at any point. Once installed it never touches the network.
- Installed home-screen web apps are not subject to Safari's 7-day storage
  eviction, so a 12-day cruise is fine. Opening it occasionally does no harm.
- Anything on the Bookings tab that is a link will need signal. Everything
  else — every day, map, timeline and note — works with the radio off.
