# GitWand runtime for BB

This repository publishes signed builds of the [GitWand](https://github.com/devlint/GitWand)
runtime (the headless `gitwand-bridge` backend plus the GitWand UI) for the
`makosh-gitwand` BB plugin.

- The `bb-runtime` branch holds only the release workflow. It carries no
  upstream history and no changes to GitWand itself.
- Builds come from a pinned upstream tag and commit, with the patches and build
  scripts in [`Mesteriis/bb-marketplace`](https://github.com/Mesteriis/bb-marketplace/tree/main/plugins/gitwand).
- Each release attaches one archive per platform, `channel.json` and its
  minisign signature. The plugin verifies the signature and every sha256
  before it installs a build.

GitWand is MIT-licensed, © 2026 Laurent Guitton. See `LICENSE` and `NOTICES`
inside each archive.
