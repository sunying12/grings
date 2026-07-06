# Growth Rings

Growth Rings is a Rare Flora-themed decision archive. It keeps the same functionality as the prior Decision Ledger, but the visuals and wording now align with the idea of **company growth rings**: every decision becomes another visible layer of organizational memory.

## Files
- `index.html` — single-file app you can host on GitHub Pages or open locally.
- `public/index.html` — same app, ready for Firebase Hosting.
- `firebase.json` — Firebase Hosting config.
- `firestore.rules` — basic Firestore rules.

## Current storage mode
By default the app runs in **local browser storage**.

To enable **shared multi-user mode**, edit `index.html` and replace:

```js
const FIREBASE_CONFIG = null;
```

with your Firebase web config.

The Firestore collection name is:

```js
const FIREBASE_COLLECTION = 'growthRingsDecisions';
```

## GitHub Pages
1. Create a new GitHub repo.
2. Upload `index.html` to the repo root.
3. Commit to `main`.
4. In GitHub: **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Choose branch `main` and folder `/root`.
7. Save.

## Firebase Hosting
From this folder:

```bash
npm install -g firebase-tools
firebase login
firebase init hosting
firebase init firestore
firebase deploy --only hosting
firebase deploy --only firestore:rules
```

If you already have a Firebase project, you can also run:

```bash
firebase use --add
firebase deploy
```

## Naming changes in the UI
- **Decision Ledger** → **Growth Rings**
- **Log Decision** → **Add Ring**
- **Ledger List** → **Archive**
- **Decision Guide** → **Field Guide**
- Dashboard copy updated to reflect the “rings” metaphor

## Visual changes
- Warm paper background
- Bark-brown sidebar
- Moss green primary actions
- Tree-ring inspired stat cards and accents
- More natural, archival Rare Flora feel
