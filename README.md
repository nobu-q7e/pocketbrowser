Pocket Browser
A small standalone desktop browser built with Python and Qt WebEngine (the same rendering engine Chrome and Edge use). It's a real browser window with tabs, back/forward, a choice of default search engine, and a lightweight extension system for running your own JavaScript on every page you visit.
> **Note on AI-generated content:** the majority of this project's code, its logo, and this README were generated with the help of AI (Claude, by Anthropic). It's been tested and works, but it's a personal/hobby project rather than a professionally audited one. The reason for this is because im currently doing
a project myself (which will be uploaded here) and I personaly dont feel like learing ANOTHER python import (the project im making myself will be uploaded to github with all of my notes/ learing files)

Features
Real web rendering — built on Qt WebEngine (Chromium), so JavaScript-heavy sites, logins, and modern web apps work normally, not like a stripped-down proxy.
Tabs — open, close, and switch between multiple tabs.
Choice of search engine — pick DuckDuckGo, Google, Bing, Startpage, or Ecosia from the Settings menu; it's remembered between launches.
Persistent sessions — cookies and logins are saved to disk, so you stay logged in to sites between restarts.
Saved tabs — closing the app remembers your open tabs and reopens them next time.
Extensions — drop a `.js` file into the `extensions` folder and it runs on every page you visit, similar to a Chrome/Edge content-script extension. Enable, disable, create, and reload extensions from the toolbar without restarting the app.
Download
Grab the latest build from the Releases page (or the itch.io page, if that's where you found this) and run the `.exe` — no installation needed.
Windows only, currently.
Building it yourself
If you'd rather build it from source for linux or mac then say somewhere (not added it yet)
Known limitations
Windows only. PyInstaller doesn't cross-compile, so Mac/Linux builds would need to be built separately on those platforms.
Unsigned executable. This isn't code-signed, so Windows Defender/SmartScreen or your antivirus may flag it or show a warning on first run. This is normal for small unsigned apps and not a sign of anything malicious — you can check the source yourself, it's all in this repo.
Extensions are simple content scripts. They can read and modify the page you're on, similar to a Tampermonkey userscript, but this isn't the full Chrome extension format — no `manifest.json`, background scripts, or toolbar popups per extension.
First launch is slow. Qt WebEngine (Chromium) takes a moment to spin up, especially from a `--onefile` build extracting itself to a temp folder. This is expected and only really noticeable on the very first startup after each new build. 
License
MIT — see LICENSE. Do whatever you like with it.
>[!NOTE]
>download from the releases
