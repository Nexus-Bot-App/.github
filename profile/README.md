# Nexus

**Nexus** is a Discord and Twitch bot that brings your community together. It announces your streams in Discord the moment you go live, keeps your server informed about Discord, GitHub and Twitch outages, helps you moderate, and adds useful commands to your Twitch chat. Everything can be managed from the [Nexus Dashboard](https://nexus.nerdscode.dev).

**Quick links:** [Dashboard](https://nexus.nerdscode.dev) · [Add to your Twitch channel](https://nexus.nerdscode.dev/dashboard/twitch/join) · [Support server](https://discord.gg/ph8WmyuQRR)

---

## Add Nexus to your Discord server

1. Go to the [Nexus Dashboard](https://nexus.nerdscode.dev) and sign in with Discord.
2. Open the **Discord** section to see the servers you manage.
3. Click **Add Bot** next to your server, and approve the permissions Discord asks for.

That's it. Nexus's slash commands appear in your server right away. Type `/` to see them.

> Nexus asks for Administrator permission so every feature works without extra setup. If you restrict it in specific channels with channel permissions, features that post in those channels (like live notifications) won't be able to.

## Add Nexus to your Twitch channel

1. Open **[nexus.nerdscode.dev/dashboard/twitch/join](https://nexus.nerdscode.dev/dashboard/twitch/join)**.
2. Sign in with Twitch and approve access.
3. Nexus joins your chat, and you're taken to your channel's dashboard.

You can also use the **Add me to your channel** button in Nexus's `/info me` card in Discord.

**Recommended:** make the bot a moderator in your channel by typing `/mod nexus_app` in your chat. Moderators aren't held back by slow mode or follower-only mode, so Nexus can always reply.

---

## Features

### For Discord servers

- **Twitch live notifications**: Nexus posts an alert the moment a streamer goes live, with the stream title, game and a live preview. The alert updates if the title or category changes, and turns into a summary with the stream's length and a VOD link when the stream ends. You can follow as many streamers as you like, each with its own channel, custom message and role ping.
- **API status updates**: get notified in a channel of your choice when Discord, GitHub or Twitch report an outage, with each update posted as it happens.
- **Moderation**: warnings, timeouts, kicks and bans with case history, evidence, message purging and moderation stats.
- **Support tickets**: members open tickets with a button, and conversations are saved as transcripts.
- **Role messages**: messages members can use to pick their own roles.
- **Event logs**: choose which server events Nexus logs.
- **Games**: Tic-Tac-Toe, Rock Paper Scissors and Connect 4 against friends or the bot, with stats.
- **Pokémon**: "Who's That Pokémon?" and a full Pokédex.
- **Handy tools**: translation, weather, timezones, country facts, movie and TV info, avatars, emoji enlarging, and adding emojis or stickers from other servers.

### For Twitch channels

- Useful chat commands like uptime, follow age and account age.
- Custom commands that you and your moderators can add, edit and disable from chat or the dashboard.
- A command prefix of your choice (the default is `!`).

### The dashboard

Sign in at [nexus.nerdscode.dev](https://nexus.nerdscode.dev) with Discord or Twitch to manage your server settings and live notifications, or your Twitch channel's commands, alerts and moderation, all in one place.

---

## Setting things up in Discord

| To... | Use |
| --- | --- |
| Announce a streamer's streams | `/twitch add`, then choose the streamer, channel and message |
| Get outage updates | `/api discord set`, `/api github set` or `/api twitch set`, then choose a channel |
| Configure moderation | `/setup`, which opens an interactive menu |
| Create a role picker | `/roles create` |
| Choose which events are logged | `/events toggle` |

You can also manage live notifications from the dashboard.

---

## Discord commands

| Command | What it does |
| --- | --- |
| `/info` | Information about a member, a role, the server, or Nexus itself (`/info me`) |
| `/twitch` | Add, edit, remove and list Twitch live notifications |
| `/api` | Choose channels for Discord, GitHub and Twitch status updates |
| `/moderation` | Warn, timeout, kick, ban and unban members, view cases and stats, and purge messages |
| `/setup` | Set up moderation for your server |
| `/roles` | Create and edit role messages |
| `/events` | Turn server event logging on or off |
| `/games` | Play Tic-Tac-Toe, Rock Paper Scissors or Connect 4, and see stats |
| `/pokemon` | Who's That Pokémon, the Pokédex and Pokémon lists |
| `/translate` | Translate text into another language. Also available by right-clicking a message. |
| `/timezone` | Set your timezone and see other members' local times |
| `/weather` | The current weather for a city |
| `/country` | Facts and stats about a country |
| `/tmdb`, `/movie`, `/tv` | Details about movies and TV shows |
| `/avatar` | View a member's avatar in full size |
| `/enlarge` | See an emoji at full size |
| `/steal` | Add an emoji from another server to yours |
| `/joke` | Hear a joke from one of several categories |

---

## Twitch chat commands

| Command | Also works as | Who can use it | What it does |
| --- | --- | --- | --- |
| `!help` | `!commands`, `!cmds`, `!h` | Everyone | Lists the commands in your channel |
| `!uptime` | `!live` | Everyone | How long you've been live |
| `!followage` | `!followedon`, `!followed` | Everyone | How long someone has followed your channel |
| `!accountage` | `!age` | Everyone | How old a Twitch account is |
| `!cd` | `!countdown` | Moderators | Starts a countdown in chat |
| `!command` | `!com`, `!customcom` | Moderators | Manages custom commands |
| `!setprefix` | | Broadcaster | Changes the command prefix |

### Custom commands

Moderators can manage custom commands straight from chat:

```
!com add <name> <global cooldown> <user cooldown> <response>
!com edit <name> <global cooldown> <user cooldown> <response>
!com del <name>
!com enable <name>
!com disable <name>
```

Cooldowns are in seconds. The global cooldown applies to everyone, and the user cooldown to each person. For example, this adds `!discord`, which can be used once every 10 seconds in chat, and once a minute per person:

```
!com add discord 10 60 Join our Discord: https://discord.gg/example
```

Command names can only contain letters and numbers. You can also manage custom commands from your channel's page on the dashboard.

---

## Languages

Nexus speaks 10 languages: English (US and UK), German, Spanish, French, Hindi, Japanese, Korean, and Simplified and Traditional Chinese. It replies in your Discord language automatically.

---

## Need help?

Join the [Nexus support server](https://discord.gg/ph8WmyuQRR) for help, to report a bug, or to suggest a feature.
