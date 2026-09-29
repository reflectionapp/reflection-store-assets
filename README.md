# reflection-store-assets

Images for Reflection's App Store listing: in-app event art, and the store
screenshots under `app-store-screenshots/` (see its README for the naming). The repository is public so
GitHub's raw host can serve the files, which lets the store-presence MCP server
fetch them by URL and upload them to App Store Connect.

## Layout

```
events/<event-slug>/card.png       event card, 1920 × 1080, PNG or JPEG
events/<event-slug>/details.png    event details page, 1080 × 1920, PNG or JPEG
```

Use a fresh slug per event, for example `events/october-reset-2026/`.

```
app-store-screenshots/apple/ios/v7/iphone-6.7in/app-store_apple_ios_iphone-6.7in_01_hero.png
```

## URLs

Every file on `main` is served at

```
https://raw.githubusercontent.com/reflectionapp/reflection-store-assets/main/<path in this repo>
```

so the card above is

```
https://raw.githubusercontent.com/reflectionapp/reflection-store-assets/main/events/october-reset-2026/card.png
```

GitHub's raw host caches for a few minutes. If you replace a file at the same
path and need the new bytes immediately, either give the new file a new name
or put the commit SHA in place of `main` in the URL, which is immutable.

## How the MCP server is allowed to read this

The server only fetches from entries on its allowlist, and this entry confines
it to this one repository rather than all of GitHub:

```
ASC_ASSET_HOST_ALLOWLIST=raw.githubusercontent.com/reflectionapp/reflection-store-assets/
```

Keep the owner and repository lowercase in URLs so they match the entry.

## Privacy

Because the repository is public, anyone who finds it can browse it, including
event art committed before its event goes live. Commit only images that are
fine to be seen early. Nothing else belongs here.
