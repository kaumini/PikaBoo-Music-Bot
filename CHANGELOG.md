# Changelog

All notable changes to PikaBoo are documented in this file.

## [4.0.0] — 2026-08-28

Major release. Setup, playlists, liked songs, player controls, and session persistence have been rebuilt. Several previously separate commands are now single interactive panels.

### Added

- **`/setup` music channel and live player panel.** Replaces the former create, delete, and info subcommands. The panel reports whether a request channel exists and whether the player message is intact. Operators can create a dedicated song-request channel, refresh or repair the panel message if it was deleted, or remove the setup after confirmation. Playback in that channel is started by sending a track name or URL.
- **Live player controls on the setup and now-playing panels:** Previous, Rewind, Pause, Forward, Skip, Loop, Stop, Shuffle, and Like. Idle, paused, and playing states use distinct panel colors. Album artwork supplies the accent color. The playback source is labeled.
- **`/playlist` management panel.** Replaces the former create, delete, list, load, addsong, removesong, and steal commands. Available actions: view playlists, view tracks in a playlist, create, delete, load into the current queue, add a track, remove a track, and copy another member’s playlist. Target selection uses dropdowns; names and queries use modals; destructive actions require confirmation.
- **Liked Songs.** Each user has a persistent Liked Songs playlist. `/likesong` (`like`, `grab`, `ls`), the Like button on the now-playing panel, and the Like button on the setup panel all write through the same save path. Duplicate likes are ignored. Concurrent likes no longer drop a save. A confirmation is posted in the channel and a track card is sent by DM when DMs are open.
- **`/viewlikedsongs` (`vls`, `likedsongs`, `mylikes`).** Lists liked tracks, loads them into the current player, and removes individual entries.
- **`/report` (`bugreport`).** In-Discord reports with four categories: Bug Report, Music / Playback Issue, Feature Suggestion, and Something Else. Submissions include the author, guild, and channel. A GitHub issues link is provided for accounts that prefer the tracker.
- **`/filters` (`fx`, `filter`).** Single dropdown for 8D / Rotation, Nightcore, Vaporwave, Karaoke, Low Pass, Tremolo, Vibrato, Bass Boost (High / Medium / Low / Off), Rate Reset, and Reset All. Per-filter commands remain available.
- **`/loop` (`repeat`) control panel** with Loop Song, Loop Queue, and Off. The now-playing and setup panels follow the selected mode.
- **`/dj` management panel** to add a DJ role, remove a role, enable or disable DJ mode, and clear configured DJ roles.
- **Player session persistence.** After a process or host restart the client can rejoin the last voice channel and restore the queue, current track, playback position, volume, and loop mode.

### Changed

- **Autoplay recommendation path.** `/autoplay` (`ap`) remains a toggle. When the queue is empty, the next tracks are requested from the source of the last played track: Spotify recommendation seeds, YouTube mix / radio follow-ups, or JioSaavn recommendations. Other sources fall back to a same-artist search. Identifiers already played in the session are excluded so a small recommendation pool cannot cycle the same tracks. Enqueued recommendations are marked as originating from autoplay.
- **Like button behavior.** The control persists the track to Liked Songs. It no longer only delivers a DM copy.
- **Filter equalizer updates** no longer clear unrelated active filters.
- **Command surfaces** for setup, playlists, DJ, liked songs, report, loop, and now-playing use a consistent ribbon-style layout (accent color, heading, supporting notes) in place of mixed classic embeds.
- Command descriptions and user-facing copy have been standardized.

### Fixed

- Liked-song writes that previously raced (read-then-write) could lose one of two near-simultaneous likes. Add-if-missing is now a single database operation.
- Autoplay could re-queue tracks already heard in the session when a source returned a small rotating set. Session identifiers are filtered before enqueue.
- A deleted or desynchronized setup panel required a full rebuild. `/setup` can resend or repair the existing panel.

### Commands

| Command | Aliases | Description |
| --- | --- | --- |
| `/setup` | `set` | Create, refresh, or remove the song-request channel and player panel |
| `/playlist` | `pl`, `plist` | Create, view, load, edit, delete, or copy playlists |
| `/likesong` | `like`, `grab`, `ls` | Save the current track to Liked Songs |
| `/viewlikedsongs` | `vls`, `likedsongs`, `mylikes` | Browse, play, or edit Liked Songs |
| `/filters` | `fx`, `filter` | Apply an audio filter |
| `/report` | `bugreport` | Submit a bug report, playback issue, or suggestion |
| `/loop` | `repeat` | Set loop mode |
| `/autoplay` | `ap` | Toggle automatic continuation of the queue |
| `/dj` | — | Configure DJ roles and DJ mode |

**Music:** `play`, `playnext`, `search`, `pause`, `resume`, `skip`, `skipto`, `stop`, `queue`, `nowplaying`, `volume`, `loop`, `shuffle`, `seek`, `replay`, `remove`, `clearqueue`, `join`, `leave`, `autoplay`, `lyrics`, `likesong`

**Playlists:** `playlist`, `viewlikedsongs`

**Filters:** `filters`, `8d`, `bassboost`, `nightcore`, `karaoke`, `lowpass`, `pitch`, `rate`, `rotation`, `speed`, `tremolo`, `vibrato`, `reset`

**Server:** `prefix`, `247`, `dj`, `setup`

**Info:** `help`, `about`, `botinfo`, `ping`, `invite`, `lavalink`, `players`, `report`
