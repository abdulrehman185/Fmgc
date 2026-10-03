# FMCG Stockout Risk Prediction Dashboard

A responsive dashboard matching the supplied FMCG Inventory Intelligence design.

## Included
- `index.html` – dashboard UI
- `style.css` – responsive styling
- `script.js` – charts, risk table and live demo prediction
- `assets/reference-dashboard.png` – supplied design reference

## Google deployment

### Option A — Firebase Hosting
1. Install Node.js.
2. Install Firebase CLI:
   `npm install -g firebase-tools`
3. Sign in:
   `firebase login`
4. Create/select a Firebase project in the Firebase Console.
5. In this folder run:
   `firebase init hosting`
6. Set the public directory to the project folder (or a `public` folder after copying the three web files).
7. Deploy:
   `firebase deploy --only hosting`

### Option B — Google Cloud Run
For a production version, place the dashboard behind a small Flask/FastAPI service and containerize it. Cloud Run can then serve the application and the ML model/API.

## Important
This package is a frontend/demo dashboard. The prediction shown by `script.js` is a demonstration formula, not the XGBoost model from a trained dataset. For a real ML deployment, connect the form to a Python API that loads the trained XGBoost model and returns `probability`, `risk_level`, and `recommendation`.
