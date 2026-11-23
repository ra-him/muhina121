# Birthday Surprise Website

A responsive romantic birthday experience built with **HTML5, CSS3 and Vanilla JavaScript**. No framework or build step is required.

## Project files

```text
birthday-surprise/
├── index.html
├── style.css
├── script.js
├── our-photo.jpg           # add your own photograph
├── romantic-music.mp3      # optional; add your own audio
└── README.md
```

## 1. Personalize the website

Open `script.js` and edit the `CONFIG` object at the very top:

```js
const CONFIG = {
  wifeName: "YOUR_WIFE_NAME",
  husbandName: "YOUR_NAME",
  birthdayDate: "YYYY-MM-DD",
  birthdayTime: "00:00:00",
  couplePhoto: "images/our-photo.jpg",
  backgroundMusic: "audio/romantic-music.mp3",
  enableMusic: true,
  loveLetter: `...`
};
```

- Replace `YOUR_WIFE_NAME` with your wife's name.
- Replace `YOUR_NAME` with your name.
- Set `birthdayDate` in `YYYY-MM-DD` format, for example `2026-12-05`.
- Set `birthdayTime` in 24-hour format, for example `00:00:00`.
- The date and time are interpreted as **Asia/Dhaka (Bangladesh) local time**, even if the visitor opens the link from another timezone.
- Edit `loveLetter` in the same object to change the letter. Keep `{HUSBAND_NAME}` where you want your name to appear.

## 2. Add your couple photograph

Copy your real photograph into the main `birthday-surprise` folder and name it exactly:

`our-photo.jpg`

The page uses that same image in the memory section and final surprise. If the file is missing, it shows a simple instructions panel rather than substituting a generated or stock couple photo. For a fast-loading mobile experience, use a compressed JPG/WebP image around 1600px wide or smaller.

If you prefer a different filename, update `couplePhoto` in `CONFIG`.

## 3. Add background music (optional)

Put a music file in the main `birthday-surprise` folder and name it `romantic-music.mp3`, or change `backgroundMusic` to match your filename. Keep `enableMusic: true`. To remove the music control, set `enableMusic: false`.

Browsers block autoplay in many situations. Music therefore starts only after your wife taps the floating Music button. It continues across the page sections and does not restart while scrolling.

Only use music you have permission to share.

## 4. Run locally

**Quick method:** open `index.html` in a modern browser.

**Recommended method:** serve the folder with a local web server. If Python is installed, open a terminal in the `birthday-surprise` folder and run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## 5. Publish free with GitHub Pages

1. Sign in to GitHub and create a new public repository, for example `birthday-surprise`.
2. Upload the contents of this folder (make sure `index.html` is at the repository root).
3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish. Your URL will look like `https://YOUR-USERNAME.github.io/birthday-surprise/`.

You can also publish by dragging the whole project folder into Netlify Drop at https://app.netlify.com/drop. Netlify will provide a public URL.

## 6. Share through WhatsApp

1. Open your published website URL and test it on your phone.
2. Copy the public URL.
3. Open WhatsApp, choose your wife's chat, paste the link and send it with a short note.
4. Send it before the configured birthday if you want her to see the countdown first.

## Important checks before sharing

- Set the correct name, date and time in `CONFIG`.
- Confirm the birthday date is correct in Bangladesh local time.
- Add `our-photo.jpg` and test that it loads.
- Add the optional music file and test the Music button.
- Open the published URL in a private/incognito tab and test both the countdown (temporarily set a future date/time) and birthday experience (temporarily set a past date/time). Restore the real date/time before sharing.
- The page automatically switches at the configured moment without refreshing. If opened after that moment, it opens directly on the birthday celebration.
