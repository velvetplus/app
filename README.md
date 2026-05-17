# Velvet

Velvet is a multi-platform IPTV player for watching live TV, movies, and series through the provider account you already use. Velvet does not sell channels, subscriptions, playlists, or provider access.

Current release: **v5.3.6+91**

Download the latest build from [GitHub Releases](../../releases/tag/v5.3.6%2B91).

## Downloads

Choose the file that matches your device:

| Platform | v5.3.6+91 download |
| --- | --- |
| Android | [APK](../../releases/download/v5.3.6%2B91/velvet-v5.3.6+91-android-apk.apk), [AAB](../../releases/download/v5.3.6%2B91/velvet-v5.3.6+91-android-aab.aab) |
| iOS | [IPA](../../releases/download/v5.3.6%2B91/velvet-v5.3.6+91-ios-ipa.ipa) |
| macOS | [App ZIP](../../releases/download/v5.3.6%2B91/velvet-v5.3.6+91-macos-app.zip) |
| Checksums | [SHA-256](../../releases/download/v5.3.6%2B91/velvet-v5.3.6+91-checksums.txt) |
| Linux | Not attached in `v5.3.6+91`; requires a Linux host build |
| Windows | Not attached in `v5.3.6+91`; requires a Windows host build |
| Web | Not attached in `v5.3.6+91`; requires a production web bundle |
| Tizen | Not attached in `v5.3.6+91`; requires a Flutter Tizen `.tpk` build |

Release tags use the app version and build number, for example `v5.3.6+91`.

## Features

- Device linking with an activation code and QR flow.
- Account profile sync for provider configuration and app settings.
- Live TV catalog with genre browsing, channel artwork, and now-playing metadata where available.
- Electronic program guide support for live channels when guide data is available.
- VOD browsing with genre/year filtering, sorting, artwork, and playback.
- Series browsing with shows, seasons, episodes, artwork, and playback.
- Favorites for live channels, VOD, and series.
- Search across synced catalog content.
- Targeted sync controls for refreshing live, VOD, and series catalogs.
- Multi-provider account support with a selectable default provider.
- Velvet+ purchase and restore controls on supported store platforms.
- Desktop fullscreen/window behavior for macOS builds.
- Support diagnostics for app version, platform, account hash, provider count, sync state, and backend health.

## Experimental Features

Experimental features are controlled by account feature flags and may not appear for every user or platform.

- Full Screen Live Guide: adds a timeline guide view from the home screen.
- Player Overlay Guide: shows upcoming live-channel programming from the player.
- Inline EPG Info: shows current program information next to player controls.
- Desktop Always on Top: keeps the desktop app above other windows.
- Picture-in-Picture: enables floating playback controls where the platform supports it.
- Chromecast and AirPlay controls: display cast controls when compatible devices are detected.
- Legacy Full Sync: exposes the older global sync control.
- Local Content Suggestions: local notifications for newly available catalog items.
- Thumbnail sizing: optional catalog card sizing controls.

## Pricing

Velvet can be used as a player. Velvet+ is an optional upgrade for the premium account experience.

| Plan | Price |
| --- | ---: |
| Monthly | `$1.99` |
| 6 Months | `$9.99` |
| Yearly | `$14.99` |

In-app purchases are available on iOS, Android, and macOS. Purchase and restore controls appear inside the app where store billing is supported.

## First Run

1. Install Velvet on your device.
2. Open Velvet and leave the link screen visible.
3. On your phone or computer, open the activation page shown in the app.
4. Enter the on-screen code or scan the QR code when available.
5. Add your provider account in your Velvet profile.
6. Return to Velvet and run sync.
7. Start watching from Live TV, VOD, Series, Favorites, or Search.

Velvet needs a linked account and a completed sync before your catalog appears.

## Install

### Android

Download the `.apk`, open it on your device, and allow installation from that source if Android asks.

### iOS

Use the `.ipa` with a valid Apple distribution method such as TestFlight, Apple Configurator, MDM, or another signed deployment flow.

### macOS

Download the `.zip`, extract it, and move Velvet into `/Applications`. If macOS blocks first launch, approve the app in System Settings and open it again.

### Linux

No Linux asset is attached to `v5.3.6+91`. Linux builds must be produced on a Linux host.

### Windows

No Windows asset is attached to `v5.3.6+91`. Windows builds must be produced on a Windows host.

### Web

No web static bundle is attached to `v5.3.6+91`.

### Tizen

No Tizen `.tpk` is attached to `v5.3.6+91`. Tizen builds require the Flutter Tizen toolchain.

## Use

### Live TV

Open **Live TV**, browse by genre, and select a channel. Guide data appears when it is available from your provider data.

### VOD

Open **VOD** to browse movies. Use filters and search after sync has completed.

### Series

Open **Series**, choose a show, select a season, and start an episode.

### Favorites

Use Favorites to keep common channels, movies, and shows easy to reach.

### Sync

Run sync when your provider lineup changes, guide data looks stale, or a title no longer opens.

## Limitations

- Velvet is a player and device-linking app. It does not provide channels, playlists, provider accounts, or media subscriptions.
- Catalog, guide, artwork, and playback availability depend on the provider account configured by the user.
- Some provider streams require headers, tokens, host matching, or formats that may behave differently across platforms.
- Browser playback cannot always inject the same transport headers as native apps.
- Guide data appears only when usable guide data is available after sync.
- Store billing is available in the iOS, Android, and macOS apps; other platforms do not expose in-app store billing in this release.
- Linux, Windows, Web, and Tizen assets are not attached to `v5.3.6+91`.
- Linux desktop builds must be produced on a Linux host.
- Windows desktop builds must be produced on a Windows host.
- Tizen packages require a configured Flutter Tizen toolchain and generated `.tpk`.
- Experimental features are feature-flagged and may change between releases.

## Troubleshooting

### No content appears

Confirm the device is linked, a provider account has been added in your Velvet profile, and sync has completed.

### Playback fails

Run sync and try again. If one item still fails while other content works, the upstream catalog entry or playback link may have changed.

### Guide data is missing

Run sync first. Guide coverage depends on the data available from your provider account.

### Wrong download

Return to [Releases](../../releases) and choose the asset for your platform.

## Support

Use [Issues](../../issues) for install problems, broken release downloads, playback regressions, and documentation corrections.

For security-sensitive reports, follow [SECURITY.md](SECURITY.md).
