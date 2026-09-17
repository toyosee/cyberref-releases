# CyberRef

**Fast, offline command reference for cybersecurity practitioners.**

Single binary. No install. No server. No internet required.

---

## What is CyberRef?

CyberRef is a searchable command reference for cybersecurity work — pentesting, blue team,
SOC, and Linux administration. It serves a modern web UI on `localhost` from a single
executable. Everything is embedded: the interface, the dataset, the styling. It runs fully
offline, which makes it usable in air-gapped labs, isolated VMs, and from a USB stick.

Built by [ToyotechICT Solutions](https://toyotechict.com.ng).

---

## Download

Grab the latest `cyberref.exe` from the
[**Releases page**](https://github.com/toyotechict/cyberref-releases/releases).

---

## Run it

1. Double-click `cyberref.exe`
2. Your default browser opens to `http://localhost:8787`
3. Use it — search, browse, copy commands
4. Press **Ctrl+C** in the console window to stop

That's it. No configuration, no first-run setup, nothing to install.

### Optional flags

cyberref.exe --port 9000 # use a different port
cyberref.exe --no-open # don't auto-open the browser
text


---

## Features

- 🔍 **Instant fuzzy search** across commands, descriptions, and tools
- 📋 **Placeholder substitution** — commands like `nmap -A -p- {TARGET}` prompt you for
  values inline; type once, reuse everywhere
- 💾 **Persistent values** — your lab IPs, domains, and usernames are remembered between
  sessions
- 🎨 **Modern dark UI** — clean, responsive, keyboard-friendly
- ⚡ **Zero dependencies** — a single `.exe`, nothing else
- 📡 **Fully offline** — works with no network, in air-gapped environments

### Keyboard shortcuts

| Key | Action |
|---|---|
| `/` | Focus the search box |
| `Esc` | Clear the search |
| `Ctrl+C` | Stop the server |

---

## Usage Tips

### Placeholder substitution

Commands with `{TOKEN}` placeholders (like `{TARGET}`, `{USER}`, `{DOMAIN}`) show inline
inputs under the command. Fill them in once:

- The **Preview** line shows the final command with your values substituted
- The **Copy** button copies the substituted version — paste-ready
- Values are **shared across all commands** using the same token
- Values **persist** across page reloads and restarts (stored in your browser)

To clear all saved values, open your browser DevTools console and run:

```js
localStorage.removeItem("cyberref.placeholders");

Search

Just start typing in the search box. Results are ranked by relevance and updated live.
Press Esc or click the × to clear and return to browsing.
Windows SmartScreen Notice

Windows may show a "Windows protected your PC" warning the first time you run
cyberref.exe. This is normal for unsigned binaries — many open-source tools trigger it.

To run: click More info → Run anyway.

Code signing is on the roadmap. Once the binary is signed, this warning disappears.
Platform Support

Currently shipping Windows 64-bit (.exe).

macOS and Linux builds are planned. If you need them sooner, get in touch.
Feedback

    Bug reports / feature requests:
    open an issue

    Direct contact:
    ToyotechICT Solutions

About

CyberRef is developed by ToyotechICT Solutions. The public repository here hosts binary
releases only. Source is maintained privately.

© ToyotechICT Solutions. All rights reserved.
text


---

## Notes on the README

1. **`screenshot.png`** — drop a screenshot of the running app at the repo root with that
   name. If you don't have one yet, either remove the image line or leave it until you add
   the file (broken images look unpolished, so I recommend adding the screenshot first).
2. **Issue tracker** — this README points issues at `cyberref-releases` repo. That works
   fine — the issues tab on a public repo is a good place for user feedback.
3. **No build instructions** — intentional. This repo is for consumers, not contributors.
4. **Link to `toyotechict.com.ng`** — swap if you'd rather point elsewhere.

---

## Setting Up the Public Repo — Quick Steps

1. On GitHub, click **New repository**
2. Name it `cyberref-releases` (or `cyberref-downloads`, your choice)
3. Set it to **Public**
4. Check **Add a README file**
5. Click **Create repository**
6. Replace the default README with the one above
7. Upload `screenshot.png` (optional but recommended)
8. Go to **Releases** → **Draft a new release**
9. **Tag**: `v0.2.0`, **Title**: `CyberRef v0.2.0`
10. Paste the release description from earlier
11. Drag `cyberref.exe` into the binaries box
12. **Publish release**

Now `cyberref.exe` is publicly downloadable, while your source stays private.

---

If you want, I can also write a shorter **one-paragraph release description** to go with the
v0.2.0 release on this new repo, tailored to first-time visitors. Just say the word.
