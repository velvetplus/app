# Release Setup Notes

Current public app release: **v5.3.6+92**

This repository is the public release surface for Velvet app downloads. It should stay free of source code, build scripts, provider examples, secrets, certificates, keys, and private release tooling.

## GitHub Organization

Organization: `velvetplus`

Configured through the GitHub API:

- Organization description: `Velvet builds multi-platform IPTV player releases for mobile, desktop, web, and TV devices.`
- Default repository permission: `read`
- Member repository creation: disabled
- Public/private member repository creation: disabled
- Repository creation type: `none`

Fields that GitHub still reported as unchanged through the API after update:

- `two_factor_requirement_enabled`
- `members_can_delete_repositories`
- `members_can_change_repo_visibility`
- `members_can_invite_outside_collaborators`

Those should be reviewed in the GitHub organization settings UI if tighter enforcement is required.

## Repository Setup

Repository: `velvetplus/app`

Configured state:

- Public repository
- Issues enabled
- Wiki enabled
- Repository description: `Official Velvet app downloads, release notes, installation help, and support tracking.`
- Single signed root commit on `main`
- GitHub labels reduced to public support labels only

The public repo intentionally contains only:

- `README.md`
- `LICENSE.md`
- `SECURITY.md`
- `CONTRIBUTING.md`
- `NOTES.md`
- GitHub issue templates and labels

## Signing

Git author:

- `Pragith <pragith@gmail.com>`

GPG key:

- Key ID: `C93D935A3FF2B868`
- Signing key fingerprint: `6FB975833C5F064E08AA7E07C93D935A3FF2B868`

The public release repo root commit and `v5.3.6+92` tag were signed with this key.

## Release v5.3.6+92

Release URL:

https://github.com/velvetplus/app/releases/tag/v5.3.6%2B92

Attached assets:

- `velvet-v5.3.6+92-android-apk.apk`
- `velvet-v5.3.6+92-checksums.txt`

Direct download URL pattern:

```text
https://github.com/velvetplus/app/releases/download/v5.3.6%2B92/<asset-name>
```

Example:

```text
https://github.com/velvetplus/app/releases/download/v5.3.6%2B92/velvet-v5.3.6+92-android-apk.apk
```

## Source App Repo Work

Repository: `Pragith/velvet`

Local path:

```text
/Users/pragith/Downloads/projects/velvet/app
```

Committed and pushed:

- Commit: `0aeb5b6`
- Message: `release: bump app version to 5.3.6+92`
- Signed with `C93D935A3FF2B868`

That source app commit included:

- `pubspec.yaml` version update to `5.3.6+92`

The untracked file `../secrets/admob-token.json` was not committed or pushed.

## Web Portal Work

Repository: `Pragith/velvet`

Local path:

```text
/Users/pragith/Downloads/projects/velvet/web
```

The web portal download page is generated from:

```text
src/velvet_app/pages/static.py
```

The `/download` page was updated to show direct GitHub release asset links for the attached `v5.3.6+92` builds.

Platforms without attached assets in `v5.3.6+92` are shown as pending instead of linking to nonexistent files.

Committed and pushed:

- Commit: `4123399`
- Message: `web: link downloads to Velvet v5.3.6+91 release assets`
- Signed with `C93D935A3FF2B868`

## Linux Build Attempt

Command attempted from the Flutter app repo:

```bash
flutter build linux --release
```

Result:

```text
"build linux" only supported on Linux hosts.
```

This was run on macOS, so a Linux `.tar.gz` asset could not be produced locally. Build Linux on a Linux host, then upload the resulting bundle to the `v5.3.6+92` release or a later release.

## Tizen Status

No `.tpk` artifact was available locally for `v5.3.6+92`.

`flutter-tizen` was not installed on the machine used for this release work. Tizen requires a configured Flutter Tizen toolchain before a `.tpk` can be produced and attached.

## Wiki Status

Wiki is enabled for `velvetplus/app`, but GitHub returned `Repository not found` for both:

```text
git@github.com:velvetplus/app.wiki.git
https://github.com/velvetplus/app.wiki.git
```

Prepared wiki pages were created locally under:

```text
/tmp/velvetplus-app-wiki
```

GitHub needs to materialize the backing wiki repository before those pages can be pushed.
