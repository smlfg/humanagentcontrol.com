# humanagentcontrol.com

**How does a human stay in control when agents are faster than they are?**

A manifesto by Samuel Fleig: eight principles for staying in charge of your own attention and
judgment when the agents you run outpace you. Not AI safety, not compliance: one person and their
mind.

## Status

Early version. Live at [humanagentcontrol.com](https://humanagentcontrol.com); every response sends
`X-Robots-Tag: noindex, nofollow` (see `public/_headers`), so search engines do not index it yet.

## What is on the page

- An interactive hourglass: a one-minute simulation with clearly fictional items in which you
  decide at the "neck" what passes to the agents. It needs JavaScript; without it the page
  explains the five moves in text.
- The eight principles, in order, with notes on where they come from.

Everything is in a single file, `public/index.html`, with no external resources and a light and
dark theme.

## Run locally

```bash
git clone https://github.com/smlfg/humanagentcontrol.com.git
cd humanagentcontrol.com
python3 -m http.server 8000 --directory public
```

Then open `http://localhost:8000`.

## Deployment

The site is a Cloudflare Worker with static assets; `wrangler.jsonc` points the asset directory to
`./public`.

```bash
npx wrangler deploy
```

## License

No license file yet; all rights reserved by default.
