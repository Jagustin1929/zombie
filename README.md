# Patch Zero — The Last Relay

A single-file, offline cyber security quiz game with a zombie-apocalypse theme, built for classroom use. No installation, no server, no internet connection required once downloaded.

## What it is

You're the night operator at Blackridge, the last relay tower still broadcasting. Fifteen safe houses have gone dark — not from anything with teeth, but because someone clicked a link, trusted a caller, or reused a password. Answer fifteen real cyber security scenarios (phishing, MFA, passwords, ransomware, social engineering, and more) to bring the network back online before the horde pressure meter maxes out and the fence comes down.

## How to run it

Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari) — double-click the file, or drag it into a browser window. That's it. Everything (art, sound, logic) is contained in the one file, so it also works from a USB stick, a shared drive, or a school LMS file upload with no extra setup.

## How to play

- Read each scenario and pick one of four answers.
- **Ask Vex** for a hint before locking in — costs 40 charge.
- **Lock in the call** to see the outcome and explanation.
- A correct answer earns 100 charge, restores some calm, and drops a piece of "salvage" — evidence of what really happened at that safe house.
- A wrong answer raises horde pressure by 25%. Pressure maxing out triggers a breach: you lose 150 charge and the screen tells you about it.
- Finish all 15 calls to see your rank and a debrief of anything worth reviewing.

**Keyboard shortcuts:** A/B/C/D or 1–4 to choose, Enter to lock in or advance, H to ask Vex, Esc to close panels.

## Features

- 15 original scenarios covering phishing, passphrases, MFA, public wifi, updates, USB drops, breach response, smishing, app permissions, ransomware, pretexting calls, oversharing, voice-clone scams, and marketplace scams — all Australia-specific where relevant (Scamwatch, ReportCyber, eSafety, 7226).
- **Field guide** — real Australian reporting resources (Scamwatch, ReportCyber, eSafety, IDCARE, Kids Helpline, Have I Been Pwned).
- **Salvage log** — a collectible evidence trail built from correct answers, giving the outbreak its own light backstory.
- Zombie atmosphere: an illustrated hero figure and background horde, shuffling silhouettes along the bottom edge, a window widget that shows a figure getting closer as pressure rises, corner claws and a screen vignette at high pressure, and a breach sequence with sound.
- All visuals are original SVG (no external image files or fonts to lose), all sound is generated in-browser with the Web Audio API (no audio files).
- Respects the browser/OS "reduce motion" setting automatically.
- Responsive down to mobile phone width.

## Customising it

Everything is editable by opening the file in a text editor — no build tools needed.

- **Questions:** find the `QUESTIONS` array near the top of the `<script>` section. Each entry has `locale`, `title`, `scenario`, `options` (4 strings), `answer` (index 0–3), `hint`, and `why` (the explanation shown after answering).
- **Salvage clues:** the `SALVAGE` array holds one line per safe house, in the same order as `QUESTIONS`.
- **Colours:** the `:root { --ash: ...; }` block near the top of the `<style>` section controls the whole palette.
- **Difficulty:** adjust the charge/pressure numbers inside the `lockIn()` and `askVex()` functions in the script.

## Notes

- Built as a single HTML file by design, so it can be shared, hosted, or embedded anywhere without a build step.
- No student data is collected or stored anywhere — nothing leaves the browser.
