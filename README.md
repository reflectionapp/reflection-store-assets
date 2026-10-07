# Reflection store assets

Everything uploaded to the app stores, by type, store, platform and version:
`<type>/<store>/<platform>/<version>/`. Custom product pages sit in a `cpp/<page>/` folder beside the default page's
files, where `<page>` is `selfcare`, `prompts`, `shadowwork`, `daily` or `anxiety`.

## Videos (v7)

| What | Where it goes in App Store Connect | File |
| --- | --- | --- |
| App preview, default page | Product page, App Previews, iPhone 6.7" | `app-store-videos/apple/ios/v7/app-store_apple_ios_iphone-6.7in_app-preview.mp4` |
| App preview, each custom product page | That page, App Previews, iPhone 6.7" | `app-store-videos/apple/ios/v7/cpp/<page>/app-store_apple_ios_iphone-6.7in_cpp-<page>_app-preview.mp4` |
| Search results video, default page | Header and Search Results, Search Results | `app-store-creative/apple/ios/v7/app-store_apple_ios_search-results_3840x2560.mp4` (H.264 copy: `_1920x1280.mp4`) |
| Search results video, each custom product page | That page, Header and Search Results, Search Results | `app-store-creative/apple/ios/v7/cpp/<page>/app-store_apple_ios_cpp-<page>_search-results_3840x2560.mp4` (H.264 copy: `_1920x1280.mp4`) |
| Product page header | Header and Search Results, Header | `app-store-creative/apple/ios/v7/app-store_apple_ios_header_3840x1646.mp4` |

App previews have the score; search-results and header videos are silent loops, because Apple plays them muted.
The default page's search results and header also have still versions (`.png`, `.jpg`) beside their videos. The custom product pages'
titles, page IDs and 5 s frames are in `app-store-creative/apple/ios/v7/cpp/README.md`.

The App Store Connect API (4.5) cannot upload header or search-results assets yet: those go in by hand. App previews
and screenshots upload through the API.
