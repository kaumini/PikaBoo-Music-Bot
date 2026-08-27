# 📋 Changelog

All notable changes to **PikaBoo Music** are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and PikaBoo aims to follow
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

> 📰 Release announcements are also posted on the [Updates page](https://pikaboobot.netlify.app/updates)
> and in the [Support Server](https://discord.gg/QsJTFvDWZd).

---

## [4.0.0] Coming soon

Nothing yet — [open an issue](https://github.com/kaumini/PikaBoo-Music-Bot/issues/new/choose) to suggest
what lands next.

---

## [3.0.0] — 2025-02-20

> 🎉 **Major upgrade** — released on 20 February 2025.
> See the [Updates page](https://pikaboobot.netlify.app/updates) for the original announcement.

### Added

- **Additional music sources integrated** — SoundCloud, Apple Music, Deezer and Amazon Music are now fully
  functional with PikaBoo, joining YouTube and Spotify.
- **Button controls in embeds** — music control buttons are now integrated into the player embed, eliminating
  the need to type commands.
- **Advanced track setup system** — a reworked setup flow for track handling.
- **More slash commands** — additional commands are now available as native Discord slash commands.
- **Moderation and DJ commands** — new commands for server moderators and DJ roles.

### Fixed

- **Lavalink WebSocket errors** — fixed `Track not found` and `No route found` errors by improving route
  resolution and track validation.

---

## [1.0.0] — 2021

🎉 Initial public release of PikaBoo.

### Added

- Discord music streaming powered by [Lavalink](https://github.com/lavalink-devs/Lavalink).
- **YouTube** and **Spotify** playback support.
- Core playback commands — `play`, `pause`, `resume`, `skip`, `stop`, `volume`.
- Queue management — `queue`, `clear`, `shuffle`, `remove`.
- Bot info commands — `help`, `ping`, `about`.

---

## Earlier history

PikaBoo has been running since 2021, and detailed release notes for the versions between the initial launch
and v3 predate this changelog. Only changes published on the
[Updates page](https://pikaboobot.netlify.app/updates) are recorded above.

---

<details>
<summary><strong>📝 How to add a new entry</strong> (for maintainers)</summary>

<br>

Add changes to the `[Unreleased]` section as you make them, grouped under whichever of these headings apply:

| Heading | Use it for |
|---|---|
| `Added` | New features, commands or sources |
| `Changed` | Changes to existing behaviour |
| `Deprecated` | Features that will be removed in a future version |
| `Removed` | Features removed in this version |
| `Fixed` | Bug fixes |
| `Security` | Security or privacy fixes |

When you cut a release, rename `[Unreleased]` to the new version with the release date in `YYYY-MM-DD`
format, and start a fresh empty `[Unreleased]` above it.

Version numbers follow [SemVer](https://semver.org/spec/v2.0.0.html):

- **MAJOR** (`3.0.0`) — breaking changes, such as renamed or removed commands
- **MINOR** (`3.1.0`) — new features that don't break anything existing
- **PATCH** (`3.0.1`) — bug fixes only

Link issues and pull requests where relevant, so users can trace a change back to the report that prompted it:

```markdown
- Fixed Spotify playlists silently dropping tracks past #100 ([#42](https://github.com/kaumini/PikaBoo-Music-Bot/issues/42))
```

</details>

---

[Unreleased]: https://github.com/kaumini/PikaBoo-Music-Bot/compare/v3.0.0...HEAD
[3.0.0]: https://github.com/kaumini/PikaBoo-Music-Bot/releases/tag/v3.0.0
[1.0.0]: https://github.com/kaumini/PikaBoo-Music-Bot/releases/tag/v1.0.0
