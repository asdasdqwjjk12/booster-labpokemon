Booster Lab — online Google Sites + jsDelivr export

IMPORTANT — publish the updated Booster Lab app to Replit BEFORE uploading these
CDN files or replacing the Google Sites embed code. The deployed production
backend must include the anonymous guest-trading routes. The existing public
app URL alone is not enough: an older deployment can still load at that URL
while its backend lacks those routes. Wait for the updated Replit deployment to
complete before continuing; otherwise embedded trading will not work.

The CDN hosts only the Booster Lab frontend and static game images. Anonymous
online trading requires the updated live backend at https://fair-trade-forge.replit.app. This embed is
for anonymous guest trading only. Live account sign-in and account-specific
features are separate: the Google Sites code does not embed Clerk or a live
account session. Use the live Booster Lab app for account-based features.
All money, grading and rewards are simulated gameplay, not real transactions.

The Google Sites document is configured for anonymous online use. It initializes
BOOSTER_EMBEDDED_GUEST=true, BOOSTER_OFFLINE=false, BOOSTER_API_BASE=https://fair-trade-forge.replit.app,
and BOOSTER_ASSET_BASE=https://cdn.jsdelivr.net/gh/asdasdqwjjk12/booster-lab@main/

Update an existing public repo (small ZIP):
1. First publish the updated Replit app and wait for the deployment to complete,
   as described above. Do not upload the new CDN files or replace the embed
   before the guest-trading backend routes are live.
2. Extract booster-lab-jsdelivr-online.zip and upload its new versioned .js and .css files
   and all included pack-photo files to the ROOT of https://github.com/asdasdqwjjk12/booster-lab. Upload
   google-sites-embed.html and embed-code.txt for your records.
3. Keep older versioned JS/CSS files: an already-published embed may still use
   one of those immutable URLs. Do not rename the new files to booster-lab.js/css.
4. Paste all of embed-code.txt in Google Sites: Insert > Embed > Embed code.
   The document includes a viewport meta tag and a small iframe-safe reset.
   Set the Sites embed tall enough for the app and publish.
5. Open the newly published page and test embedded anonymous trading. The
   backend must allow requests from the published site's origin.

To open the game directly through jsDelivr instead of Google Sites, upload
booster-lab.svg to the repository root, then open:
https://cdn.jsdelivr.net/gh/asdasdqwjjk12/booster-lab@main/booster-lab.svg#/
For this update, use the cache-safe versioned link:
https://cdn.jsdelivr.net/gh/asdasdqwjjk12/booster-lab@main/booster-lab.ea134a157fb4.svg#/
Open this as a webpage, not as an image element: scripts are disabled when SVG
is loaded through an img tag. The SVG launches the same online guest frontend
inside a regular HTML frame; the live backend is still required for trading.

For a mounted QA preview, place local-preview.html and its hashed JS/CSS files
beside one another at /cdn-check/. It uses this repo's CDN as its image base, so
the two large image folders do not need to be copied to the web app.

The small update ZIP includes the pack photos at its root, matching the existing
GitHub upload layout. Upload those files together with the new JS, CSS and SVG.
It omits the duplicate pack-images folder and the large crown-card-images folder.
Keep the existing Crown Zenith image folder in your public repo. For a first-time upload or to
refresh every image, use booster-lab-jsdelivr-online-full.zip and upload both
image folders at the repository root, preserving their names and paths.


NEW REPOSITORY / COMPLETE FILE PACKAGE
Extract the full ZIP, then upload the CONTENTS of booster-lab-jsdelivr-online to your new
repository root (not the outer booster-lab-jsdelivr-online folder). Include all root files
and preserve crown-card-images/ with all 230 scans. Pack photos are supplied at
the root and in pack-images/. Do not flatten the Crown Zenith folder.

The SVG launcher automatically uses the repository URL it was opened from:
https://cdn.jsdelivr.net/gh/YOUR_USERNAME/YOUR_NEW_REPOSITORY@main/booster-lab.ea134a157fb4.svg#/
You do not need to edit the SVG or JavaScript for the new repository.
index.html also works with relative assets on GitHub Pages or another static host.
jsDelivr serves HTML as text, so open the SVG when using jsDelivr directly.
For Google Sites only, replace the old repository base https://cdn.jsdelivr.net/gh/asdasdqwjjk12/booster-lab@main/
throughout embed-code.txt with your new repository's jsDelivr base before embedding.
Trading still uses the existing published Replit backend, not GitHub.
