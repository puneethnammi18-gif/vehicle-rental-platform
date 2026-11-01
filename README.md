# Safe Rides

Static vehicle-rental website for a CSE326 assignment, hosted on GitHub Pages.

## Firebase Authentication

The Safe Rides web app is registered in the Firebase project **Safe Rides Vehicle Rental**, and its public web app config is connected in `firebase-config.js`.

To finish account sign-in, in the Firebase console:

1. Open **Authentication → Sign-in method** and enable **Email/Password** and **Google**.
2. Open **Authentication → Settings → Authorized domains** and add `puneethnammi18-gif.github.io`.

The website supports email/password registration and sign-in, password reset, Google sign-in, and sign-out. The Firebase web app config is public client configuration, not a private service-account key. Never put a service-account JSON file or private key in this website repository.

Vehicle photos are loaded from Unsplash and need an internet connection.
