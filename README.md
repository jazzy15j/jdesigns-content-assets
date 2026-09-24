# JDesigns Content Assets

Public image host for the JDesigns content engine (`meta-publisher`, and any future
Instagram/Facebook content). This repo exists purely so content images have a stable,
publicly-fetchable URL — Instagram's Content Publishing API requires one and does not
accept direct uploads.

**Why a separate repo instead of the main website (Netlify):** the Netlify deploy path
has failed unpredictably multiple times (see JDesigns's own `decisions.md`, 2026-09-08)
and pushing content images through the live site's deploy pipeline risks the real site.
This repo is decoupled from jdesigns.info entirely.

**Why raw GitHub URLs instead of GitHub Pages:** no build step, no publish delay — a
pushed file is fetchable immediately at its raw URL. Simpler and just as reliable for
this narrow purpose.

## Usage

Drop an image in `images/`, commit, push. Its public URL is:

```
https://raw.githubusercontent.com/jazzy15j/jdesigns-content-assets/main/images/<filename>
```

Use that URL as `image_url` in a `meta-publisher` batch.json.

## Scope

Images only. No client data, no credentials, no anything sensitive — this repo is
public by design.
