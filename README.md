# billing-auth-form

CRM Panel · Billing Authorization Form — single-file HTML app.

## Setup

1. Open `billing-auth-form.html` in a text editor.
2. Find the `FIREBASE_CONFIG` block near the top of the `<script>` section.
3. Replace every `YOUR_*` placeholder with your actual Firebase project values  
   (get them from the [Firebase Console](https://console.firebase.google.com/) → Project Settings → Your apps).
4. Open the file in a browser — no build step required.

```js
var FIREBASE_CONFIG = {
  apiKey:            "YOUR_FIREBASE_API_KEY",
  authDomain:        "YOUR_PROJECT_ID.firebaseapp.com",
  databaseURL:       "https://YOUR_PROJECT_ID-default-rtdb.firebaseio.com",
  projectId:         "YOUR_PROJECT_ID",
  storageBucket:     "YOUR_PROJECT_ID.firebasestorage.app",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId:             "YOUR_APP_ID"
};
```

## ⚠️ Security

- **Never commit real API keys** to this repository.  
- Firebase Web API keys are restricted by domain in the Firebase Console  
  (Authentication → Settings → Authorized domains). Keep that list tight.  
- Gemini / Callmebot keys are stored in Firebase at runtime — they are **not** in this file.

## Features

- PIN-protected login
- Lead & client management
- Waiver & Billing Authorization (with signature pad + QR send)
- Dashboard with charts
- AI Tools panel (Gemini integration)
- PDF / print exports
- Firebase Realtime Database sync
