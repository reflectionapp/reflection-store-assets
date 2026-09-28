# reflection-store-assets

Images for Reflection's App Store in-app events, served as a static site so the
store-presence MCP server can fetch them by URL and upload them to App Store
Connect.

## Layout

```
events/<event-slug>/card.png       event card, 1920 × 1080, PNG or JPEG
events/<event-slug>/details.png    event details page, 1080 × 1920, PNG or JPEG
```

Use a fresh slug per event, for example `events/october-reset-2026/`.

## URLs

Every file is served at

```
https://reflection-store-assets.vercel.app/<path in this repo>
```

so the card above is `https://reflection-store-assets.vercel.app/events/october-reset-2026/card.png`.
Each push to `main` deploys, and Vercel invalidates its cache on deploy, so
replacing a file at the same path serves the new bytes.

## How the MCP server is allowed to read this

The server only fetches from hosts on its allowlist:

```
ASC_ASSET_HOST_ALLOWLIST=reflection-store-assets.vercel.app
```

## Privacy

This repository is private, so its history and anything not deployed stay
private. Deployed files are reachable by anyone holding the exact URL, which
the upload path requires; there is no directory listing, and `robots.txt` plus
an `X-Robots-Tag: noindex` header keep search engines from indexing them.
