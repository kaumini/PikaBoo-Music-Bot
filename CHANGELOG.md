# Changelog

All notable changes to PikaBoo are documented in this file.

## [4.0.0] — 2026-09-16

Major release. Setup, playlists, Liked Songs, player controls, and session persistence have been rebuilt. Several previously separate commands are now unified interactive panels.

The PikaBoo website has also received a major rework centred on an interactive Premium `/setup` demonstration and Discord-linked Patreon memberships.

### Added

- **`/setup` music channel and live player panel.** Replaces the former create, delete, and info subcommands. The panel reports whether a request channel exists and whether the player message is intact. Server managers can create a dedicated song-request channel, refresh or repair the panel if it was deleted, or remove the setup after confirmation. Members can start playback by sending a song name or URL in the channel.

- **Live player controls.** The setup and now-playing panels include Previous, Rewind, Pause, Forward, Skip, Loop, Stop, Shuffle, and Like. Idle, paused, and playing states use distinct panel colours, while album artwork supplies the playing accent colour.

- **`/playlist` management panel.** Replaces the former create, delete, list, load, addsong, removesong, and steal commands. Members can view playlists and tracks, create or delete playlists, load them into the queue, add or remove tracks, and copy another member’s playlist.

- **Liked Songs.** Each member receives a persistent Liked Songs playlist. `/likesong`, the Like button on the now-playing panel, and the Like button on the setup panel all use the same save system. Duplicate tracks are ignored, and simultaneous likes no longer overwrite one another.

- **`/viewlikedsongs`.** Members can browse their Liked Songs, load them into the player, or remove individual tracks.

- **`/report`.** Reports can now be submitted from Discord under Bug Report, Music or Playback Issue, Feature Suggestion, or Something Else. Reports include the author, server, and channel.

- **Unified `/filters` menu.** A single dropdown provides 8D, Nightcore, Vaporwave, Karaoke, Low Pass, Tremolo, Vibrato, Bass Boost levels, Rate Reset, and Reset All. Individual filter commands remain available.

- **`/loop` control panel.** Members can switch between Loop Song, Loop Queue, and Off. The setup and now-playing panels update to reflect the selected mode.

- **`/dj` management panel.** Server managers can add or remove DJ roles, enable or disable DJ mode, and clear configured roles.

- **Player session persistence.** Following a process or host restart, PikaBoo can rejoin the previous voice channel and restore the queue, current track, playback position, volume, and loop mode.

- **`/changelog` and `/premium`.** `/changelog` displays the latest release notes, while `/premium` explains Premium and Pro features and provides access to the available plans.

### Website

- **Interactive Premium `/setup` demonstration.** The homepage now includes a responsive Discord-style simulation of PikaBoo’s song-request channel and live player. Visitors can enter a song name or URL, play supported demonstration tracks, and interact with the controls.

- **Live player state demonstration.** The website player moves between idle, paused, and playing states with artwork-based colours, playback progress, queue information, and interactive feedback matching the bot’s Discord interface.

- **Interactive Music Setup panel.** The website demonstrates the Premium `/setup` workflow, including setup status, song-request channel creation, player-panel refresh and repair, setup removal with confirmation, and the Refresh Status action.

- **Patreon and Discord Premium integration.** Members can sign in with Discord, connect Patreon, and link an active Premium or Pro membership to the same Discord account.

- **Verified membership system.** Patreon OAuth and signed membership webhooks synchronize Premium entitlements without relying on users manually claiming that they purchased a plan.

- **Premium account dashboard.** Signed-in members can view their Free, Premium, or Pro status, refresh their membership data, browse servers they can manage, and add PikaBoo to a selected server.

- **Developer Premium controls.** Authorized developer accounts can manually grant or revoke Premium and Pro plans when support intervention is required.

- **Free, Premium, and Pro plans.** A dedicated Premium page compares included features and limits for queues, playlists, songs per playlist, and Liked Songs.

- **Searchable command directory.** Commands can be searched and filtered by Music, Playlists, Filters, Server, and Info. Each entry includes its slash command, prefix usage, aliases, description, and Premium label where applicable.

- **Feature guides.** Dedicated pages explain the live player, playback, playlists, Liked Songs, autoplay, audio filters, DJ roles, 24/7 mode, reports, and the complete `/setup` process.

- **Dedicated status page.** The website now includes a status page covering the Discord gateway, Lavalink audio nodes, commands, player persistence, and setup panels.

- **Additional information pages.** Added dedicated Help, Team, Updates, Changelog, Setup, Commands, Features, Premium, and Dashboard pages.

- **Major visual rework.** The website now uses a responsive dark interface with animated neon-gradient PikaBoo branding, Discord-styled components, clearer navigation, and carefully placed PikaBoo artwork.

- **Accurate supported sources.** The website presents the four currently supported sources: YouTube, YouTube Music, Spotify, and SoundCloud.

### Changed

- **Autoplay recommendation system.** `/autoplay` remains a toggle. When the queue becomes empty, PikaBoo requests recommendations based on the last-played source. Tracks already played during the session are excluded to prevent repeated recommendations.

- **Like button behaviour.** The Like button now saves the track to the member’s persistent Liked Songs playlist instead of only sending a copy through DM.

- **Filter handling.** Equalizer changes no longer clear unrelated active filters.

- **Command interfaces.** Setup, playlists, DJ, Liked Songs, reports, loop controls, and now-playing now use a consistent ribbon-style layout instead of mixed classic embeds.

- **Premium feature presentation.** Premium commands and features are now labelled consistently across the bot, website command directory, feature pages, and plan comparison.

- **Command descriptions and user-facing text** have been standardized throughout the bot and website.

### Fixed

- Fixed a race condition where two near-simultaneous likes could cause one saved track to be lost.

- Fixed autoplay repeatedly queueing tracks already played during the current session.

- Fixed deleted or desynchronized setup panels requiring a complete setup rebuild. `/setup` can now resend or repair the existing panel.

### Commands

| Command | Aliases | Description |
| --- | --- | --- |
| `/setup` | `set` | Create, refresh, repair, or remove the song-request channel and player panel |
| `/playlist` | `pl`, `plist` | Create, view, load, edit, delete, or copy playlists |
| `/likesong` | `like`, `grab`, `ls` | Save the current track to Liked Songs |
| `/viewlikedsongs` | `vls`, `likedsongs`, `mylikes` | Browse, play, or edit Liked Songs |
| `/filters` | `fx`, `filter` | Open the audio-filter menu |
| `/report` | `bugreport` | Submit a bug report, playback issue, or suggestion |
| `/loop` | `repeat` | Set the current loop mode |
| `/autoplay` | `ap` | Toggle automatic queue recommendations |
| `/dj` | — | Configure DJ roles and DJ mode |
| `/changelog` | `updates`, `whatsnew` | View the latest release notes |
| `/premium` | `vip`, `pro` | View Premium and Pro information |

**Music:** `play`, `playnext`, `search`, `pause`, `resume`, `skip`, `skipto`, `stop`, `queue`, `nowplaying`, `volume`, `loop`, `shuffle`, `seek`, `forward`, `rewind`, `replay`, `remove`, `move`, `removedupes`, `history`, `clearqueue`, `join`, `leave`, `autoplay`, `lyrics`, `likesong`

**Playlists:** `playlist`, `viewlikedsongs`

**Filters:** `filters`, `8d`, `bassboost`, `nightcore`, `karaoke`, `lowpass`, `pitch`, `rate`, `rotation`, `speed`, `tremolo`, `vibrato`, `reset`

**Server:** `prefix`, `247`, `dj`, `setup`

**Info:** `help`, `about`, `botinfo`, `ping`, `invite`, `lavalink`, `players`, `report`, `changelog`, `premium`
