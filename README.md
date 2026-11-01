# Safe Rides

Static vehicle-rental website for a CSE326 assignment, hosted on GitHub Pages.

## Connect real accounts with Firebase Authentication

The site is wired for email/password registration, email/password sign-in, password reset, Google sign-in, and sign-out. It needs a Firebase web app before those features can create or authenticate users.

1. Create a Firebase project at https://console.firebase.google.com/ and register a **Web app**.
2. In **Authentication → Sign-in method**, enable **Email/Password** and **Google**.
3. In **Authentication → Settings → Authorized domains**, add `puneethnammi18-gif.github.io`.
4. Copy the web app config values from **Project settings → Your apps** into `firebase-config.js` (`apiKey`, `authDomain`, `projectId`, and `appId`).
5. Commit the updated `firebase-config.js` to the GitHub repository. GitHub Pages will redeploy automatically.

The web app config is public client configuration, not a private service-account key. Never put a service-account JSON file or private key in this website repository.

Until the Firebase project config is added and providers are enabled, the account buttons show a setup message. Vehicle photos are loaded from Unsplash and need an internet connection.

