# JoAnne Gomez, RN: Video Resume

A 65-second video introduction for nursing job applications.

**Watch it here:** https://msjag416.github.io/video-resume/

## What's in this repo

- `index.html` is the web page employers see: my name and nursing roles, the video player with captions, my licences and certifications, a short work history, a written transcript, and links to my LinkedIn and business card. It also holds link preview tags (so the link shows my photo and title when shared) and schema.org "Person" details for search engines.
- `video-resume.mp4` is the video (square, 1080 x 1080, about 65 seconds, about 10 MB so it still loads fast on phones). It's saved with a restart point (keyframe) every second so the picture can start quickly. It was made with Kling AI Avatar Pro on KIE from my photo and my own voice recording.
- `captions.vtt` is the caption file the player shows on top of the video. It was made from my recording with Whisper and checked by hand.
- `poster.jpg` is my photo with the blue play button, shown on top of the player before the video plays.
- `share.jpg` is the wider image used when the link is shared on LinkedIn, email or text.
- `favicon.svg`, `favicon.ico` and `apple-touch-icon.png` are the blue "RN" icon for browser tabs and phone home screens.

## How it works

GitHub Pages serves this repo as a website from the `main` branch. When someone opens the link, their browser loads `index.html`, which plays `video-resume.mp4` with `captions.vtt`. A few lines of script under the video switch the captions on when the page loads and when the video first plays, because phone browsers often ignore the caption "default" setting. Another short script handles the photo on top of the player: tapping it starts the video, and the photo is removed only once the moving picture is ready. There's no other code, server, or database.

## Why the player is built this way (November 2026 iPhone fix)

On JoAnne's iPhone, the sound started right away but the picture lagged when the video played inside the page. Full screen, her iPad and her partner's iPhone were fine. Side-by-side test pages showed the cause was the video's built-in `poster` (cover photo) setting: her iPhone kept the cover photo up after play was pressed. So:

- Don't add a `poster` attribute back to the `<video>` tag. The photo is a separate button laid over the player instead, and the page controls when it goes away.
- The video loads as soon as the page opens (`preload="auto"`), and the player has square corners with no shadow, matching the version tested on her iPhone.
- Test any change on an iPhone in Safari, without going full screen, before calling it done.

## Updating it

- New video: replace `video-resume.mp4` (keep the name), then make a new `captions.vtt` and update the transcript in `index.html` so all three match.
- After replacing the video, captions or cover image, raise the `?v=` number on those file names in `index.html` (for example `?v=3` to `?v=4`). Phones that saw the page before keep saved pieces of the old file, and mixing old and new pieces can make the picture lag behind the sound. A new number makes every phone fetch the new file.
- Dates and credentials on the page come from my master resume (JoAnne_Gomez_RN_UHN_PACU_Resume). Change them there first, then here.
