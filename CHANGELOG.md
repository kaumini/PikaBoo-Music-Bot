# 🚀 PikaBoo v4 Changelog

> A major update focused on better music management, cleaner controls, persistence, and an improved Discord experience.

## ✨ Highlights

- 🎶 **Unified Playlists** — Manage playlists through a single `/playlist` panel instead of separate commands.
- ❤️ **Liked Songs** — Like the currently playing track to save it to your personal Liked Songs playlist and receive the track in your DMs.
- 💾 **Persistent Likes** — The Like button on now-playing panels now permanently saves the track.
- 🐛 **In-Discord Reports** — Use `/report` to submit bug reports, playback issues, feature suggestions, or other feedback without leaving Discord.
- 🔄 **Queue Persistence** — After a bot or host restart, the player can reconnect and restore the queue, volume, loop mode, and playback position.
- 🎨 **Improved Panels** — Now-playing, playlists, setup, DJ, and Liked Songs use cleaner ribbon-style interfaces with album-art accent colors.

## 🆕 New Commands

| Command | Aliases | Description |
|---|---|---|
| `/playlist` | `pl`, `plist` | Create, view, load, add to, remove from, delete, or copy playlists from one panel |
| `/likesong` | `like`, `grab`, `ls` | Save the current track to Liked Songs and DM the track |
| `/viewlikedsongs` | `vls`, `likedsongs`, `mylikes` | Browse, play, or remove songs from your Liked Songs |
| `/filters` | `fx`, `filter` | Manage available audio filters from a dropdown |
| `/report` | `bugreport` | Submit a bug report, playback issue, suggestion, or other feedback |

## 📂 `/playlist` Panel

One panel with **eight actions**:

1. 📋 **View My Playlists** — See playlist names and song counts
2. 🎵 **View Song List** — Browse the tracks inside a playlist
3. ➕ **Create a Playlist** — Enter a playlist name through a popup
4. 🗑️ **Delete a Playlist**
5. ▶️ **Load into Queue** — Load and play a playlist in the current server
6. ➕ **Add a Song**
7. ➖ **Remove a Song**
8. 📥 **Copy from Another User** — Create a copy of another user's playlist

## ⚙️ `/setup` & `/dj` Improvements

### `/setup`

- 🎵 Create a dedicated song-request channel
- 🔄 **Refresh / repair the player panel** if it was deleted
- 🗑️ Delete the setup

### `/dj`

- 👤 Add a DJ role with a role picker
- ➖ Remove a DJ role
- 🔛 Enable or disable DJ mode
- 🧹 Clear all configured DJ roles

## 🐛 `/report` Categories

- 🪲 **Bug Report**
- 🎵 **Music / Playback Issue**
- 💡 **Feature Suggestion**
- 📝 **Something Else**

## 🔧 Improvements

| Feature | Improvements |
|---|---|
| `/loop` | Now accepts `repeat` and uses a clear 3-button panel: **Loop Song** · **Loop Queue** · **Off** |
| `/filters` | Adds a unified filter menu with Vaporwave and Bass Boost levels: **High / Medium / Low / Off** |
| Now Playing | Cleaner layout, album-art accent colors, and a Like button that saves tracks |
| Queue | Improved presentation and persistent queue restoration after restart |
| Playlists | Playlist management consolidated into one interactive panel |
| Setup | Player panel can be refreshed or repaired directly from `/setup` |
| DJ | DJ management is handled through a single interactive panel |
| Commands | Cleaner, more consistent command descriptions and user-facing text |

## 🎛️ Available Filters

`8D / Rotation` · `Nightcore` · `Vaporwave` · `Karaoke` · `Low Pass` · `Tremolo` · `Vibrato` · `Bass Boost (High / Medium / Low / Off)` · `Rate Reset` · `Reset All`

> ℹ️ The individual filter commands such as `/nightcore`, `/8d`, and `/bassboost` remain available.

## 🎮 Player Controls

Every now-playing panel includes controls for:

`Previous` · `Rewind` · `Pause` · `Forward` · `Skip` · `Loop` · `Stop` · `Shuffle` · `Like Song`

❤️ **Like Song** now saves the current track instead of only sending it to your DMs.

## 🎵 Music Features

PikaBoo v4 includes:

- ▶️ Play, pause, resume, skip, stop, and queue controls
- 🔎 Search and choose tracks before playing
- ⏭️ Play a song next in the queue
- 🔁 Replay the current track
- ⏩ Seek to a specific timestamp
- 🔀 Shuffle and queue management
- 🔊 Volume control
- 🎛️ Multiple audio filters
- 🎤 Lyrics
- 🤖 Autoplay
- 🔄 24/7 voice-channel support

## 📚 Playlist & Personal Music

- 📂 Create and manage personal playlists
- ▶️ Load playlists directly into the queue
- 👥 Copy playlists from other users
- ❤️ Save tracks to Liked Songs
- 🎵 Play your saved Liked Songs whenever you want

## 🛠️ Reliability & Persistence

- 💾 Queue state is preserved across restarts
- 🔊 Volume settings persist
- 🔁 Loop mode persists
- ⏱️ Playback position persists
- 🎵 The full queue can be restored after a restart
- 🔄 The player reconnects to the last active voice channel

## ℹ️ Command Overview

### 🎵 Music

`play` · `playnext` · `search` · `pause` · `resume` · `skip` · `skipto` · `stop` · `queue` · `nowplaying` · `volume` · `loop` · `shuffle` · `seek` · `replay` · `remove` · `clearqueue` · `join` · `leave` · `autoplay` · `lyrics` · `likesong`

### 📂 Playlists

`playlist` · `viewlikedsongs`

### 🎛️ Filters

`filters` · `8d` · `bassboost` · `nightcore` · `karaoke` · `lowpass` · `pitch` · `rate` · `rotation` · `speed` · `tremolo` · `vibrato` · `reset`

### ⚙️ Server Configuration

`prefix` · `247` · `dj` · `setup`

### ℹ️ Information & Utilities

`help` · `about` · `botinfo` · `ping` · `invite` · `lavalink` · `players` · `report`
