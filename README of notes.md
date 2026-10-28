# Petal Notes

A light-pink note-taking app with rich-text tools, color tags, and one small voice-dictation feature. Pure HTML/CSS/JS — a single `index.html` file, no build step, no backend, no API keys.

## Features

- **Rich text tools:** bold, italic, underline, strikethrough, headings, highlight, bullet lists, numbered lists, and checklists (tap the checkbox to tick items off).
- **Color tags:** give each note one of six pastel colors to spot it at a glance.
- **Custom tags:** add your own text tags and search by them.
- **Pin notes:** keep important notes at the top of the list.
- **Search:** filters by title, content and tags as you type.
- **Voice dictation (the app's one AI feature):** tap the mic button and speak — your phone's built-in speech recognition types what you say into the note. This uses the browser's own speech service; the app does not call any external AI service.
- **Smart Assist:** two small on-device helpers, not a cloud AI — "Suggest a title" picks the first sentence of your note, and "Suggest tags" picks the most frequent meaningful words in it. Both run entirely in your browser.
- **Works on phones:** on a narrow screen, the note list and the editor are separate full-screen views with a back button and a floating "+" button; on a wider screen they sit side by side.
- **Saves automatically:** every note is saved to the browser's local storage as you type, so nothing needs a Save button.

## Run it locally

Just open `index.html` in a browser.

## Deploy on GitHub Pages

1. Create a new GitHub repository (public).
2. Upload `index.html` to the root of the repository.
3. Go to the repo's **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`.
5. Pick the branch (usually `main`) and folder `/ (root)`, then **Save**.
6. After a minute, the app is live at:
   `https://<your-username>.github.io/<repo-name>/`

## Notes on the voice feature

Voice dictation uses the Web Speech API, which is built into the browser (not a server Petal Notes runs). Support varies:
- Works well in Chrome on Android and on desktop.
- Limited or unavailable in some versions of Safari and Firefox — the mic button disables itself automatically when the browser doesn't support it.
- It needs an internet connection and microphone permission, since most browsers process speech through their own cloud speech service.

## Data and privacy

All notes, tags and colors are stored only in the browser's local storage on the device you're using. They are not sent anywhere, and they do not sync between devices or browsers.
