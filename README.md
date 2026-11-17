# JoAnne Gomez, RN: Video Resume

A 65-second video introduction for nursing job applications.

**Watch it here:** https://msjag416.github.io/video-resume/

## What's in this repo

- `index.html` is the web page employers see: my name and nursing roles, the video player with captions, my licences and certifications, a short work history, a written transcript, and links to my LinkedIn and business card. It also holds link preview tags (so the link shows my photo and title when shared) and schema.org "Person" details for search engines.
- `video-resume.mp4` is the video (square, 1080 x 1080, about 65 seconds, about 9 MB so it still loads fast on phones). It was made with Kling AI Avatar Pro on KIE from my photo and my own voice recording.
- `captions.vtt` is the caption file the player shows on top of the video. It was made from my recording with Whisper and checked by hand.
- `poster.jpg` is the still image shown before the video plays.
- `share.jpg` is the wider image used when the link is shared on LinkedIn, email or text.
- `favicon.svg`, `favicon.ico` and `apple-touch-icon.png` are the blue "RN" icon for browser tabs and phone home screens.

## How it works

GitHub Pages serves this repo as a website from the `main` branch. When someone opens the link, their browser loads `index.html`, which plays `video-resume.mp4` with `captions.vtt`. A few lines of script under the video switch the captions on when the page loads and when the video first plays, because phone browsers often ignore the caption "default" setting. There's no other code, server, or database.

## Updating it

- New video: replace `video-resume.mp4` (keep the name), then make a new `captions.vtt` and update the transcript in `index.html` so all three match.
- Dates and credentials on the page come from my master resume (JoAnne_Gomez_RN_UHN_PACU_Resume). Change them there first, then here.
