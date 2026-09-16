# Live Übersetzer — German → English

A live captioning web app: it listens to German speech through your microphone and shows English translations as people speak.

## Use it
Open the GitHub Pages link in **Chrome** (Android / desktop), **Edge**, or **Safari** (iPhone), tap **Start**, and allow microphone access.

- **Text size / Hide German** — adjust the display.
- **Save** — download the transcript (German + English) as a text file.
- **Settings** — add a Google Translate API key (recommended for long classes) or an email for MyMemory's higher free limit.

## Listening for a whole class (~1 hour)
- Keep the page open and in front — the app keeps the screen awake while listening.
- Speech recognition restarts automatically whenever the browser pauses it.
- The transcript is saved in the browser, so reloading the page doesn't lose it.
- An hour of German is roughly 50,000 characters. MyMemory's free limit won't cover that, so add a
  [Google Cloud Translation API key](https://cloud.google.com/translate/docs/setup) in Settings
  (the free tier covers about 500,000 characters a month). Restrict the key to your GitHub Pages URL.
- Keep your phone plugged in.
- **Space bar** — start/stop on desktop.

## How it works
- Speech recognition: the browser's built-in Web Speech API (`de-DE`). Needs an internet connection.
- Translation: Chrome desktop's on-device Translator API when available, otherwise Google Cloud Translation (if a key is set), otherwise the free [MyMemory](https://mymemory.translated.net/) API.
