# WeCom trusted domain (GitHub Pages)

Public site (domain **root**): **https://wasif-deep-bridge.github.io/**

WeCom needs the verify file at the **domain root**, so we use this user site
(`wasif-deep-bridge.github.io`), not a project subpath.

## Steps

1. WeCom admin → **App Management** → **Roy Testing**
2. **Web Authorization and JS-SDK** → **Set trusted domain name**
3. Enter domain only (no `https://`):

   `wasif-deep-bridge.github.io`

4. Download `WW_verify_xxxxx.txt` from WeCom
5. Save it into **this folder** (same level as `index.html`)
6. Tell the agent to push, or run:

   ```bash
   git add WW_verify_*.txt
   git commit -m "Add WeCom verify file"
   git push
   ```

7. Open `https://wasif-deep-bridge.github.io/WW_verify_xxxxx.txt`
   and confirm the file contents show in the browser
8. Click **verify** in WeCom
9. **Company's Trusted IP** → add your current public IP (`what is my ip`)
10. Retry browser `gettoken`

Do **not** commit Corp Secret.
