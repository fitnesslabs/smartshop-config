# Smart Shop store settings

The Smart Shop app reads this file to know, for each supermarket, where to search, where the basket is,
and the small scripts it runs on the supermarket's pages (skipping adverts, pressing the checkout button).
Publishing a fix here reaches every phone within a few hours, with no App Store update.

- `stores.signed.json` is what the app downloads. It is signed with a key kept only on the developer's Mac;
  the app ignores any copy whose signature doesn't match, so a change made directly on GitHub has no effect.
- `stores.json` is the same settings, readable.

This repository is public on purpose: it holds no passwords, keys or personal data.

To publish: edit `SmartShop/Stores.json` in the app project, raise `version`, then run
`sh Tools/publish-store-settings.sh`. Gather several fixes into one version where you can.

Keep this repository free of GitHub Actions workflows. It only needs to hold the file.
