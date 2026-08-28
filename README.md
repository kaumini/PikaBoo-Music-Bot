<h1 align="center">PikaBoo</h1>

<p align="center">
  Discord music bot for Spotify, YouTube, SoundCloud, and more. Built with Discord.js, Lavalink, and TypeScript.
</p>

<p align="center">
  <a href="https://discord.com/api/oauth2/authorize?client_id=907132113223028797&permissions=518683754304&scope=bot%20applications.commands"><img alt="Invite" src="https://img.shields.io/badge/Invite-PikaBoo-5865F2?style=for-the-badge&logo=discord&logoColor=white"></a>
  <a href="https://discord.com/invite/KBMRaFfjhq"><img alt="Support" src="https://img.shields.io/badge/Support-Server-5865F2?style=for-the-badge&logo=discord&logoColor=white"></a>
  <a href="https://pikaboobot.netlify.app"><img alt="Website" src="https://img.shields.io/badge/Website-pikaboobot-1DB954?style=for-the-badge&logo=netlify&logoColor=white"></a>
  <a href="CHANGELOG.md"><img alt="Version" src="https://img.shields.io/badge/Version-v4-111827?style=for-the-badge"></a>
</p>

<p align="center">
  <a href="#about">About</a> ·
  <a href="#features">Features</a> ·
  <a href="#getting-started">Getting started</a> ·
  <a href="#commands">Commands</a> ·
  <a href="#premium">Premium</a> ·
  <a href="#whats-new">Changelog</a> ·
  <a href="#feedback">Feedback</a> ·
  <a href="#support">Support</a>
</p>

---

## About

PikaBoo launched in 2021 as a music bot for Discord communities. Audio is handled by Lavalink. Playback sources include YouTube, Spotify, SoundCloud, Apple Music, Deezer, Yandex, and JioSaavn.

v4 rebuilds the operator-facing panels: a dedicated music channel, a single playlist manager, persistent Liked Songs, source-aware autoplay, and in-Discord reporting.

---

## Features

Priority surfaces in v4:

| Area | What changed |
| --- | --- |
| **Setup** | `/setup` creates a song-request channel and a live player panel. Refresh or repair the panel if the message is deleted. Play by typing a name or URL in that channel. |
| **Playlists** | `/playlist` replaces the old split commands. Create, view, load, edit, delete, or copy another member’s playlist from one panel. |
| **Liked Songs** | `/likesong` and the Like button on now-playing and setup panels save the current track. `/viewlikedsongs` lists, plays, and edits that list. |
| **Autoplay** | When the queue ends, recommendations follow the last source (Spotify, YouTube, JioSaavn) with a same-artist fallback. Already-played tracks in the session are skipped. |
| **Report** | `/report` files a bug, playback issue, or suggestion from Discord. GitHub remains available for tracked issues. |

Also included:

- Hybrid prefix and slash commands (default prefix `<`, configurable per server)
- Now-playing and setup controls: previous, rewind, pause, forward, skip, loop, stop, shuffle, like
- Audio filters from one menu (`/filters`) and as individual commands
- DJ role panel and 24/7 stay-connected mode
- Queue, volume, and loop restoration after a bot or host restart
- Lyrics, search-before-play, play-next, and seek

### Sources

YouTube · YouTube Music · Spotify · SoundCloud · Apple Music · Deezer · Yandex · JioSaavn

---

## Getting started

1. **Invite**  
   [Add PikaBoo](https://discord.com/api/oauth2/authorize?client_id=907132113223028797&permissions=518683754304&scope=bot%20applications.commands)

2. **Join a voice channel**

3. **Play**
   ```
   /play Peekaboo Kendrick Lamar
   <play https://open.spotify.com/track/...
   ```

4. **Optional — dedicated music channel**  
   Run `/setup` to create a request channel with a live panel. After that, song names and links typed in that channel start playback.

Documentation: [pikaboobot.netlify.app/docs](https://pikaboobot.netlify.app/docs)

---

## Commands

Prefix and slash commands are both supported. The prefix defaults to `=` and can be changed with `/prefix`.

### Music

| Command | Description |
| --- | --- |
| `/play <query or URL>` | Play a track or playlist |
| `/playnext` | Queue a track to play next |
| `/search` | Search and choose a result |
| `/pause` / `/resume` | Pause or resume |
| `/skip` / `/skipto` | Skip, or jump to a position |
| `/stop` | Stop and clear the player |
| `/queue` | Show the queue |
| `/nowplaying` | Show the current track |
| `/volume` | Set volume |
| `/loop` | Loop track, loop queue, or off |
| `/shuffle` | Shuffle the queue |
| `/seek` | Seek to a timestamp |
| `/replay` | Restart the current track |
| `/remove` / `/clearqueue` | Edit the queue |
| `/join` / `/leave` | Connect or disconnect |
| `/autoplay` | Continue with recommendations when the queue ends |
| `/lyrics` | Fetch lyrics |
| `/likesong` | Save the current track to Liked Songs |

### Playlists

| Command | Description |
| --- | --- |
| `/playlist` | Create, view, load, edit, delete, or copy playlists |
| `/viewlikedsongs` | Browse, play, or edit Liked Songs |

### Filters

| Command | Description |
| --- | --- |
| `/filters` | Apply a filter from the menu |
| `/8d` `/nightcore` `/bassboost` `/karaoke` `/lowpass` `/pitch` `/rate` `/rotation` `/speed` `/tremolo` `/vibrato` `/reset` | Individual filter commands |

### Server

| Command | Description |
| --- | --- |
| `/setup` | Song-request channel and live player panel |
| `/dj` | DJ roles and DJ mode |
| `/247` | Stay connected when the queue is empty |
| `/prefix` | Set the text-command prefix |

### Info

| Command | Description |
| --- | --- |
| `/help` `/about` `/invite` `/ping` | Help, about, invite, latency |
| `/report` | Bug, playback issue, or suggestion |
| `/changelog` | Version history |
| `/premium` | Premium status and plans |

Full list: [pikaboobot.netlify.app/commands](https://pikaboobot.netlify.app/commands)

---

## Configuration

- **Prefix** — `/prefix`
- **DJ roles** — `/dj`
- **Music channel** — `/setup`
- **24/7** — `/247`

---

## Premium

Autoplay, filters, and playlist commands are Advanced Premium features. They are available on a free trial through **11 September 2026**. After the trial they require a plan.

| | Included |
| --- | --- |
| Autoplay | Source-aware continuation when the queue ends |
| Filters | `/filters` and the individual filter commands |
| Playlists | `/playlist` and Liked Songs playlist management |

Plans and current status: [pikaboobot.netlify.app/premium](https://pikaboobot.netlify.app/premium)

In Discord: `/premium`

---

## What's new

**v4.0.0 — 28 August 2026**

- `/setup` rebuilt as a single panel with create, refresh/repair, and delete
- Live player panel with playback controls and a Like button that saves tracks
- `/playlist` consolidates playlist management
- Liked Songs persist across `/likesong`, now-playing, and the setup panel
- Autoplay recommendations follow the last source and skip already-played tracks
- `/report` for in-Discord feedback
- Queue, volume, loop mode, and position can be restored after a restart

Full history: [CHANGELOG.md](CHANGELOG.md) · [Updates](https://pikaboobot.netlify.app/updates)

---

## Feedback

Use **[GitHub Issues](https://github.com/kaumini/PikaBoo-Music-Bot/issues/new/choose)** for bugs, features, and improvements. Use **[Discussions](https://github.com/kaumini/PikaBoo-Music-Bot/discussions)** for questions.

| Intent | Template |
| --- | --- |
| Something is broken | [Bug report](https://github.com/kaumini/PikaBoo-Music-Bot/issues/new?template=bug_report.yml) |
| New feature | [Feature request](https://github.com/kaumini/PikaBoo-Music-Bot/issues/new?template=feature_request.yml) |
| Improve an existing feature | [Improvement](https://github.com/kaumini/PikaBoo-Music-Bot/issues/new?template=improvement.yml) |
| Track, playlist, or source failure | [Playback / source issue](https://github.com/kaumini/PikaBoo-Music-Bot/issues/new?template=playback_issue.yml) |
| Docs or website | [Documentation](https://github.com/kaumini/PikaBoo-Music-Bot/issues/new?template=documentation.yml) |
| Question | [Discussions → Q&A](https://github.com/kaumini/PikaBoo-Music-Bot/discussions/new?category=q-a) |

Before opening an issue: search [existing issues](https://github.com/kaumini/PikaBoo-Music-Bot/issues?q=is%3Aissue), check [status](https://pikaboobot.netlify.app/status), and confirm the version in the [changelog](CHANGELOG.md).

Do not post bot tokens or other credentials.

In Discord, `/report` sends the same categories to the team without leaving the server.

---

## Support

- [Support server](https://discord.com/invite/KBMRaFfjhq)
- [Documentation](https://pikaboobot.netlify.app/docs)
- [Status](https://pikaboobot.netlify.app/status)
- [GitHub Issues](https://github.com/kaumini/PikaBoo-Music-Bot/issues)
- [Discussions](https://github.com/kaumini/PikaBoo-Music-Bot/discussions)

---

## Links

| | |
| --- | --- |
| Website | https://pikaboobot.netlify.app |
| Invite | https://discord.com/api/oauth2/authorize?client_id=907132113223028797&permissions=518683754304&scope=bot%20applications.commands |
| Features | https://pikaboobot.netlify.app/features |
| Commands | https://pikaboobot.netlify.app/commands |
| Premium | https://pikaboobot.netlify.app/premium |
| Documentation | https://pikaboobot.netlify.app/docs |
| Updates | https://pikaboobot.netlify.app/updates |
| Changelog | [CHANGELOG.md](CHANGELOG.md) |
| Status | https://pikaboobot.netlify.app/status |
| Team | https://pikaboobot.netlify.app/team |
| Support | https://discord.com/invite/KBMRaFfjhq |
| Terms of Service | https://github.com/mrghost0001/PikaBoo-TOS-Privacy-Policy/blob/main/Terms%20of%20Services.md |
| Privacy Policy | https://github.com/mrghost0001/PikaBoo-TOS-Privacy-Policy/blob/main/Privacy%20Policy.md |

---

## Team

| Member | Role |
| --- | --- |
| PiK4CHU | Creator |
| GHO3T | Developer, designer, beta tester |
| VENUK | Beta tester / supporter |
| DIHEN | Beta tester / supporter |

---

<p align="center">
  <sub>© 2026 PikaBoo. Official Pika Palace music bot.</sub>
</p>
