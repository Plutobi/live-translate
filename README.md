# Live Übersetzer — German → English

A live captioning web app: it listens to German speech through your microphone and shows English translations as people speak.

## Use it
Open the GitHub Pages link in **Chrome** (Android / desktop), **Edge**, or **Safari** (iPhone), tap **Start**, and allow microphone access.

- **Text size / Hide German** — adjust the display.
- **Save** — download the transcript (German + English) as a text file.
- **Quota** — optionally add your email to raise the free MyMemory translation limit from 5,000 to 50,000 characters/day.
- **Space bar** — start/stop on desktop.

## How it works
- Speech recognition: the browser's built-in Web Speech API (`de-DE`). Needs an internet connection.
- Translation: Chrome desktop's on-device Translator API when available (unlimited, fast), otherwise the free [MyMemory](https://mymemory.translated.net/) API.
