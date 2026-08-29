# Spin & Dare — INDICODE NIT Delhi

This is the **online multiplayer** version intended for GitHub Pages.

## Important
GitHub Pages can host the frontend, but it does **not** provide a shared realtime database. This project therefore uses **Firebase Realtime Database + Anonymous Authentication**.

### Setup
1. Create a Firebase project.
2. Enable **Authentication → Sign-in method → Anonymous**.
3. Create **Realtime Database**.
4. Register a Web App and copy its Firebase config.
5. Open `script.js` and replace the `PASTE_...` values in `firebaseConfig`.
6. For a quick prototype, use these Realtime Database rules:

```json
{
  "rules": {
    "rooms": {
      ".read": true,
      ".write": true
    }
  }
}
```

**Do not use those open rules for a real production site.** They allow anyone to change/delete data. Tighten the rules before public launch.

## GitHub Pages
Upload `index.html`, `style.css`, `script.js` and this README to a GitHub repository.
Then:
**Settings → Pages → Deploy from branch → main → /root → Save**

Your GitHub Pages URL can then be shared.

## Admin
The included admin screen is a **demo UI only**. The browser login is not secure because all frontend code is public on GitHub.

For real admin control (secure password, delete rooms, inspect every room, etc.), add Firebase Authentication with an admin account and Firebase Security Rules / Cloud Functions. Do not put an admin password in JavaScript.

## Included features
- Public/private rooms
- Up to 10 players
- Online room sharing
- Realtime player list
- Realtime party chat
- Custom Truth/Dare/Joke chat shortcuts
- Animated bottle spin
- Truth/Dare selection
- Round counter
- Active/closed room status
- Admin dashboard UI
- No premium option
- Mobile-friendly interface
- Created by INDICODE · NIT Delhi · Janak
