# DimerBuilder Binder/Voila app

This repository is set up to publish `DimerBuilder.ipynb` as a code-hidden web app using Binder + Voila.

## What users get
- A browser-based interactive UI
- A live Python kernel for widget interaction and plotting
- Code cells hidden in the Voila app view

## Files
- `DimerBuilder.ipynb`: cleaned notebook for the web app (xTB section removed)
- `requirements.txt`: Python packages Binder installs
- `.binder/postBuild`: trusts the notebook after build

## How to publish
1. Create a new **public GitHub repository**.
2. Upload all files from this folder to the repo root, keeping the `.binder` folder.
3. Wait until GitHub finishes processing the upload.
4. Open this URL in your browser, replacing `YOUR-USER` and `YOUR-REPO`:

   `https://mybinder.org/v2/gh/YOUR-USER/YOUR-REPO/HEAD?urlpath=voila/render/DimerBuilder.ipynb`

5. Test the app. The first launch can take a bit because Binder builds the environment.
6. Share that Binder URL with users.

## Notes
- Binder sessions are temporary and do not persist files after the session ends.
- If you update the notebook, Binder may rebuild the environment on the next launch.
- If `py3Dmol` rendering is blocked in a browser, ask users to allow JavaScript and reload.
