# Live Übersetzer — German → English

A live captioning web app for **class lectures, conferences and conversations**: it listens to German speech through your microphone and shows English translations as people speak.

**Open the app:** https://plutobi.github.io/live-translate/

## Use it
Open the link in **Chrome** (Android / desktop), **Edge**, or **Safari** (iPhone) and allow microphone access.

**Lectures & conferences** — choose *Transcribe*, *Translate* or *Both* and tap the red mic. German appears live; English follows a few seconds behind.

**Conversations** — choose *Talk*. Tap **Deutsch** when the other person speaks German, or **English** when you speak. Each message is translated and read aloud (toggle *Read aloud*); German translations are shown large so you can show your screen.

- **UK / US** — British or American English (spelling like colour/color and a few words like flat/apartment).
- **Text size**, **Save** (download transcript or conversation), **Clear**, **Settings** (Google key / MyMemory email).
- The line under the mic shows how much free translation you have left.

## How long can I listen?
There is no time limit in the app — it keeps restarting speech recognition for as long as you like. The real limit is the free translation quota (German speech is roughly 850 characters per minute):

| Translation engine | Free allowance | About |
|---|---|---|
| MyMemory (default) | 5,000 characters/day | ~6 minutes a day |
| MyMemory + email in Settings | 50,000 characters/day | ~1 hour a day |
| Google Cloud Translation key | 500,000 characters/month | ~10 hours a month |
| Chrome on a computer (on-device) | unlimited | no limit |

Speech recognition itself is free. Keep the phone plugged in and the app on screen for long sessions.

## Listening for a whole class (~1 hour)
- Keep the page open and in front — the app keeps the screen awake while listening.
- Speech recognition restarts automatically whenever the browser pauses it.
- The transcript is saved in the browser, so reloading the page doesn't lose it.
- An hour of German is roughly 50,000 characters. MyMemory's free limit won't cover that, so add a
  [Google Cloud Translation API key](https://cloud.google.com/translate/docs/setup) in Settings
  (the free tier covers about 500,000 characters a month). Restrict the key to your GitHub Pages URL.
- Keep your phone plugged in.
- **UK / US** — choose British or American English (spelling like colour/color and a few words like flat/apartment).
- **Space bar** — start/stop on desktop.

## How it works
- Speech recognition: the browser's built-in Web Speech API (`de-DE`). Needs an internet connection.
- Translation: Chrome desktop's on-device Translator API when available, otherwise Google Cloud Translation (if a key is set), otherwise the free [MyMemory](https://mymemory.translated.net/) API.
