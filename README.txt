Match Map — installable web app (PWA)
=====================================

Folder contents:
- index.html ...... the game (English by default, Arabic via the language button)
- manifest.json ... app name, icons and launch settings
- sw.js ........... lets the game work offline after the first visit
- icons/ .......... app icons in every size

Important: installing does not work if you open index.html straight from your computer.
The folder must be uploaded to an https site such as Netlify or GitHub Pages.

Easiest: Netlify Drop (one minute, no code)
1. Unzip the file.
2. Open https://app.netlify.com/drop
3. Drag the whole "khareetat-altawafuq" folder onto the page.
4. You get a link like https://random-name.netlify.app right away.
   Create a free account to keep the site permanently; you can rename it in Site settings.

GitHub Pages
1. Create a free account on github.com and a new Public repository, e.g. match-map.
2. Click "uploading an existing file" and upload everything inside the folder
   (index.html, manifest.json, sw.js and the icons folder). index.html must be at the top level. Commit.
3. Settings → Pages: Source = Deploy from a branch, Branch = main, / (root), Save.
4. After a minute or two: https://your-username.github.io/match-map/

Installing on a phone
- Android (Chrome): open the link → tap "📲 Install app" at the top, or menu ⋮ → Install app.
- iPhone (Safari): open the link → Share → Add to Home Screen.

Updating later
Upload the new index.html, then in sw.js change  const CACHE = "matchmap-v3";
to matchmap-v4 (then v5 ...) so installed copies pick up the new version.

Optional next step: Google Play
Once the site is live, open https://www.pwabuilder.com, paste your link and choose Android
to get a package ready for Google Play (needs a Google Play developer account).

-------------------------------------------------------------
بالعربية باختصار:
1. فك الضغط، وافتح https://app.netlify.com/drop واسحب المجلد إليها لتحصل على رابط.
2. على أندرويد: افتح الرابط واضغط «📲 Install app». على آيفون: مشاركة ← إضافة إلى الشاشة الرئيسية.
3. اللعبة بالإنجليزية افتراضياً، وزر «عربي» أعلى الصفحة يحوّلها للعربية (ويتذكر اختيارك).
4. عند التحديث: غيّر رقم النسخة في sw.js (matchmap-v3 ← matchmap-v4).
