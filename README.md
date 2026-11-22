# frazo-app.github.io

Static site served by GitHub Pages at https://frazo-app.github.io.

- `.well-known/assetlinks.json`: lets Android verify the Frazo App Link, so a link to an Assignment opens the app.
  Add the Play app signing key fingerprint (Play Console > Setup > App integrity) for `com.tomsoftix.english` before
  the closed test.
- `index.html`: the page a phone without Frazo sees; it points to Google Play.
- `.nojekyll`: without it Jekyll drops the `.well-known` folder.

Check on a phone: `adb shell pm get-app-links <package>` should say `verified` for `frazo-app.github.io`.
