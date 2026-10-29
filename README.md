# CMF Companion for Homebrew

[![Cask checks](https://github.com/usamabinshahid97/homebrew-tap/actions/workflows/cask.yml/badge.svg)](https://github.com/usamabinshahid97/homebrew-tap/actions/workflows/cask.yml)

Install [CMF Companion](https://github.com/usamabinshahid97/cmf-companion), an unofficial native macOS menu bar app for **CMF Buds 2 (B179)**.

Requires **Apple Silicon** and **macOS 14 or later**. Liquid Glass is available on macOS 26+; macOS 14–15 use a material fallback. Intel Macs and other earbud models are not supported by this binary.

```sh
brew install --cask usamabinshahid97/tap/cmf-companion
```

Homebrew adds this tap automatically. If Homebrew asks whether to trust this community cask, review [the cask](Casks/cmf-companion.rb) and confirm if you trust it.

## First launch

Launch **CMF Companion** from Applications. The current release is **ad hoc signed, not Developer ID signed or Apple notarized**. If macOS blocks its first launch, try opening it once, then use **System Settings → Privacy & Security → Open Anyway** if you trust this release. See [Apple's instructions](https://support.apple.com/en-ie/102445). This cask preserves normal quarantine behavior.

Allow Bluetooth access when macOS asks, connect CMF Buds 2 in macOS Bluetooth settings, and click the earbuds icon in the menu bar. The app has no Dock icon. Developer ID signing and notarization will be added in a future release.

This is the app's own community tap. It is not listed in Homebrew's official cask catalog. [Release notes and known limitations](https://github.com/usamabinshahid97/cmf-companion/releases/latest) are published with the app.

## Update

Quit CMF Companion from its More menu, then run:

```sh
brew update
brew upgrade --cask usamabinshahid97/tap/cmf-companion
```

## Uninstall

Quit the app, then run:

```sh
brew uninstall --cask cmf-companion
```

To remove the app's preferences too, use `brew uninstall --cask --zap cmf-companion`. Neither action unpairs the buds or resets their settings.

## Maintenance

For each new release, update `version` and the SHA-256 of its published ZIP in `Casks/cmf-companion.rb`, then copy that exact cask to the [compatibility tap](https://github.com/usamabinshahid97/homebrew-cmf-companion) so existing installation links receive the same updates. Keep published version archives immutable. The URL and livecheck follow [the app's GitHub releases](https://github.com/usamabinshahid97/cmf-companion/releases).

```sh
brew style --cask usamabinshahid97/tap/cmf-companion
brew audit --cask --strict --online usamabinshahid97/tap/cmf-companion
```

Full release instructions and source are in the [app repository](https://github.com/usamabinshahid97/cmf-companion/blob/main/DISTRIBUTION.md). The app and this tap use AGPL-3.0; see [LICENSE](LICENSE).
