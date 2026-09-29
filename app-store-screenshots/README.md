# App Store screenshots

Store listing screenshots, one folder per store, platform, release and device size.

```
app-store-screenshots/<store>/<platform>/<release>/<device>/
  app-store_<store>_<platform>_<device>_<NN>_<screen-name>.png
```

- `store`: `apple` (Google Play would sit beside it as `google`).
- `platform`: `ios`. iPad and Mac sizes go under the same release, for example
  `ios/v7/ipad-13in/`, `macos/v7/mac/`.
- `release`: the app version the set was made for, for example `v7`.
- `device`: the display class and the size App Store Connect files it under, for
  example `iphone-6.7in` (1290 × 2796).
- `NN`: the position in the store listing, two digits, starting at `01`.
- `screen-name`: a short kebab-case label for what the screen shows.

The filename repeats the folder path on purpose: a screenshot pulled out of this
repository still says what it is and where it goes.

Each device folder has a README listing its screens and their copy.

The source for these images (the HTML stage, the app screens, and the render
script) is in `reflectionapp/reflection_marketing`, under `app_store/<release>/`.
