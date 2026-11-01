# Safe Rides

Static vehicle-rental website for a CSE326 assignment, hosted on GitHub Pages.

## Firebase Authentication

Firebase Authentication is connected to the **Safe Rides Vehicle Rental** project. The website supports email/password registration and sign-in, password reset, Google sign-in, and sign-out.

Enabled providers:
- Email/Password
- Google

Authorized web domain: `puneethnammi18-gif.github.io`

## Email verification

Email/password signups receive a Firebase verification email. Users can resend it from the website; after following the link, they can return to Safe Rides or refresh the page. Unverified email/password accounts cannot count as referrals. Google sign-in uses the provider's verified email status.

## Referral campaign

Signed-in users see a 45-day referral event with a three-friend progress bar. The first two referrals unlock 20% off a next ride each; the third unlocks 50% off a next ride. Referral relationships and progress use Cloud Firestore. The security rules are in `firestore.rules`; the database must be created before referral tracking can run.

Firebase Auth user accounts are listed under **Authentication → Users**. Firestore stores only referral profile timestamps/counts and inviter/invitee user IDs. Rules require verified Firebase email claims for referral writes, limit each account to one referral record, cap the count at three, enforce the 45-day window, and prevent users from listing other profiles.

The Firebase web app config in `firebase-config.js` is public client configuration. Never put a service-account JSON file or private key in this website repository.

Vehicle photos are loaded from Unsplash and need an internet connection.
