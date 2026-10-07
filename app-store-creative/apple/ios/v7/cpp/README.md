# Custom product page videos (Reflection 7.0)

One cut per custom product page. Each opens on the page's topic, titled with the page's first-screenshot
headline, then runs the default app preview from the photos card on. At exactly 5 s each shows the topic at rest,
because that frame is the thumbnail whenever a video can't autoplay (Apple's API ignores the poster frame and
uses 5 s).

| Page | Page ID | Title | At 5 s |
| --- | --- | --- | --- |
| `selfcare` | 18500915-3415-4707-a2e2-e54b7a47035e | A self-care journal that writes back. | Nightly Reflection Ritual, "What went well today?" answered, the Coach's reply complete |
| `prompts` | 44986ef9-d49f-4b1b-b975-51c526f2e758 | Never face a blank page. | The Guides library: Featured Guides and Featured Voices |
| `shadowwork` | 12ac5229-6d12-493d-90a8-f2a0d19f0e01 | Shadow work, one question at a time. | Healing Your Inner Child, the Coach asking why |
| `daily` | 13da47be-f55f-4bcb-89c8-0889d2a9393a | Daily reflections in 5 minutes. | The daily question's entry, written |
| `anxiety` | 2bdf6ca4-1a35-41b1-8d97-2952f67e4846 | A calmer place for anxious thoughts. | Go From Fear to Confidence, a reply that slows things down |

## Files

| Placement | Path | Spec |
| --- | --- | --- |
| iOS 27 search results | `app-store-creative/apple/ios/v7/cpp/<page>/app-store_apple_ios_cpp-<page>_search-results_3840x2560.mp4` | 3:2, 3840 × 2560, HEVC, 30 fps, 21.6 s, silent loop |
| the same, H.264 | `app-store-creative/apple/ios/v7/cpp/<page>/app-store_apple_ios_cpp-<page>_search-results_1920x1280.mp4` | 1920 × 1280, for anything that refuses the HEVC master |
| App preview (iPhone 6.7") | `app-store-videos/apple/ios/v7/cpp/<page>/app-store_apple_ios_iphone-6.7in_cpp-<page>_app-preview.mp4` | 886 × 1920, H.264 + AAC, 30 fps, 25.1 s |

The search videos are silent on purpose: Apple plays search-results video muted, with no way to unmute.

**Format check (7 Oct 2026).** Apple's App Store Connect help, updated for the 5 Oct 2026 creative-assets launch,
says creative assets can be uploaded "from Custom Product Pages", and that a custom product page's submission
includes "any assets assigned to it". So the search video (and header) can be set per page. Two things follow:

- **The App Store Connect API (4.5) cannot upload or assign creative assets yet**, so the search videos are uploaded
  by hand in App Store Connect: the page, then Header and Search Results, then Search Results.
- **The search video shows only on iOS 27 and later.** On earlier iOS, search shows the page's app preview, which
  the API can upload today.

**Copy.** Sam Ellery is the app's synthetic test persona. Guides appear exactly as the CMS inserts them, the daily
questions are real ones from the CMS, and the library shows real published guides and their authors' photos. The
Coach is labeled only "Coach": nothing says anyone reads the journal, and no reply makes clinical or therapy claims.
US English throughout.

Built in `reflectionapp/reflection_marketing`, `videos/app_preview/` (see its README).
