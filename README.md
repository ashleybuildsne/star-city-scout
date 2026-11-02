# Star City Scout

A small tool built for one person's real daily job: running Star City Deals, a
Lincoln deals page on Facebook. It turns a deal screenshot, or a few typed
details, into a complete, ready-to-post Facebook post kit in seconds.

Built during the Meta Global AI Developer Hackathon (October 26 – November 4,
2026) for the "Build for Your World" track, by @ashleybuildsne.

## What it does

- **Deal form:** paste a deal link, product name, sale price, original price,
  deal tag (like "Limited time deal"), an optional promo code, and notes.
- **Post kit:** builds a playful-first caption with the price in the caption
  only, a shop link, a "from a Lincoln mom" sign-off, a prices-can-change
  warning, `#ad` plus the Amazon Associates disclosure, and hashtags. No em
  dashes, ever.
- **Promo codes get their own first comment:** if a deal has a promo code, the
  kit includes a separate first-comment block with its own copy button, so
  the code stays easy to copy.
- **Screenshot reading:** drop in a screenshot of a deal and Scout reads the
  product name, sale price, original price, percent off, deal tag, visible
  link, and promo code straight out of the image, then builds the kit.
- **Fresh AI captions:** a "Write it fresh with AI" button writes a new
  playful opening line for each deal, kept under 50 words and checked against
  the house rules (no price, link, hashtags, `#ad`, em dashes, or invented
  claims in the opening).
- **Make a picture:** an optional prompt box that generates a promo image
  for a deal, with a preview and a Download button.

## How it works

Scout is a single web page. It calls Meta's models through the Meta Model
API:

- A vision model reads deal screenshots.
- A text model writes fresh caption openings.
- Muse Image generates pictures.

## Your key stays yours

Scout asks for your Meta API key in a box on the page itself. The key lives
only in that browser tab's memory. It is never saved to a file, never sent
anywhere except to Meta's services to do the work above, and never typed
into a chat. Close the tab and it's gone, so you paste it fresh each time
you open the page. No key is included anywhere in this project.

## Run it yourself

This page must be run locally, from a file on your own computer. Links
hosted on the web block the API calls Scout needs, so open the downloaded
page directly, paste your key into the key box, and go. You can test the key
with the "Test this key" button in the key box before you start.
