# Nexus

**Nexus** is a Discord and Twitch bot that brings your community together. It announces your streams in Discord the moment you go live, keeps your server informed about Discord, GitHub and Twitch outages, and helps you moderate. On Twitch, it thanks your followers and supporters in chat, keeps spam out automatically, and adds useful commands. Everything can be managed from the [Nexus Dashboard](https://nexus.nerdscode.dev).

**Quick links:** [Add to Discord](https://discord.com/oauth2/authorize?client_id=1488183510643773460&permissions=8&scope=bot+applications.commands) · [Add to your Twitch channel](https://nexus.nerdscode.dev/dashboard/twitch/join) · [Dashboard](https://nexus.nerdscode.dev) · [Support server](https://discord.gg/ph8WmyuQRR)

---

## Add Nexus to your Discord server

**[Click here to add Nexus to your server](https://discord.com/oauth2/authorize?client_id=1488183510643773460&permissions=8&scope=bot+applications.commands)**, choose your server, and approve the permissions Discord asks for.

Or add it from the dashboard:

1. Go to the [Nexus Dashboard](https://nexus.nerdscode.dev) and sign in with Discord.
2. Open the **Discord** section to see the servers you manage.
3. Click **Add Bot** next to your server, and approve the permissions.

That's it. Nexus's slash commands appear in your server right away. Type `/` to see them.

> Nexus asks for Administrator permission so every feature works without extra setup. If you restrict it in specific channels with channel permissions, features that post in those channels (like live notifications) won't be able to.

## Add Nexus to your Twitch channel

1. Open **[nexus.nerdscode.dev/dashboard/twitch/join](https://nexus.nerdscode.dev/dashboard/twitch/join)**.
2. Sign in with Twitch and approve access.
3. Nexus joins your chat straight away, and you're taken to your channel's dashboard.

You can also use the **Add me to your channel** button in Nexus's `/info me` card in Discord.

### What you're approving

Approving access lets Nexus act on your own channel, so every feature works without making it a moderator:

| Permission | What Nexus uses it for |
| --- | --- |
| Chat as a bot in your channel | Replying in chat with Twitch's verified **Chat Bot** badge |
| Read followers, subscriptions, Bits and channel point redemptions | Chat alerts, and the `!followage` command |
| Ban and time out users, delete messages, and change chat settings | Chat filters, and moderating from the dashboard |
| Read moderation info | The dashboard's banned users list |
| Manage channel point redemptions, and read chatters | Upcoming channel point and moderation features (not used yet) |

Nexus only acts on your channel, and you can disconnect it at any time from your Twitch settings under **Connections**.

### Other ways to add it

- Type `!join` in [Nexus's own Twitch chat](https://www.twitch.tv/nexus_app), and `!leave` there to remove it. Nexus joins your chat, but doesn't get the permissions above. To turn on alerts, filters and dashboard moderation later, click **Reconnect with Twitch** on your channel's dashboard.
- If your channel was added before a new feature arrived, your dashboard shows a **Reconnect with Twitch** banner when new permissions are needed.

**Tip:** if you added Nexus without approving access, make it a moderator by typing `/mod nexus_app` in your chat. It can then run chat filters and `!followage`, and isn't held back by slow mode or follower-only mode.

---

## Features

### For Discord servers

- **Twitch live notifications**: Nexus posts an alert the moment a streamer goes live, with the stream title, game and a live preview. The alert updates when the title or category changes, and turns into a summary with the stream's length and a VOD link when the stream ends. You can follow as many streamers as you like, each with its own channel, custom message and role ping.
- **API status updates**: get notified when Discord, GitHub or Twitch report an outage. Each post shows the platform's logo, the affected components (like "Client (Android)") and every update, and is edited in place as the incident progresses.
- **Moderation**: warnings, timeouts, kicks and bans with case history, evidence, message purging and moderation stats.
- **Support tickets**: members open tickets with a button, and conversations are saved as transcripts.
- **Role messages**: messages members can use to pick their own roles.
- **Event logs**: choose which server events Nexus logs.
- **Games**: Tic-Tac-Toe, Rock Paper Scissors and Connect 4 against friends or the bot, with stats.
- **Pokémon**: "Who's That Pokémon?" and a full Pokédex.
- **Handy tools**: translation, weather, timezones, country facts, movie and TV info, avatars, emoji enlarging, and adding emojis or stickers from other servers.

### For Twitch channels

- **Chat alerts**: Nexus thanks viewers in chat for follows, subs, resubs, gift subs, Bits, raids and channel point redemptions, with your own messages.
- **Chat filters**: automatically delete, time out or ban for links, caps spam, emote spam and blocked words, with `!permit` to let someone post a link.
- **Moderation from the dashboard**: change chat settings, ban and time out users, see and lift bans, and clear chat, without opening Twitch.
- **Verified Chat Bot badge**: Nexus's messages show Twitch's **Chat Bot** badge in your chat.
- **Chat commands** like uptime, follow age and account age.
- **Custom commands** that you and your moderators manage from chat or the dashboard.
- **Your own command prefix** (the default is `!`).

### The dashboard

Sign in at [nexus.nerdscode.dev](https://nexus.nerdscode.dev) with Discord or Twitch:

- **Discord servers:** manage your server settings and Twitch live notifications.
- **Twitch channels:** manage your custom commands and prefix, set up chat alerts on the **Alerts** page, and use the **Moderation** page for chat settings, bans, clearing chat and chat filters.

Only you can manage your Twitch channel's settings on the dashboard.

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

## Setting things up on Twitch

| To... | Go to |
| --- | --- |
| Thank followers, subs, cheers, raids and redemptions | Dashboard → your channel → **Alerts** |
| Block links, caps spam, emote spam or words | Dashboard → your channel → **Moderation** → Chat Filters |
| Turn on slow mode, followers-only and other chat modes | Dashboard → your channel → **Moderation** → Chat Settings |
| Ban, time out or unban someone | Dashboard → your channel → **Moderation**, or Twitch as usual |
| Add custom commands | `!com add` in chat, or the dashboard |

---

## Chat alerts

Turn each alert on or off and write your own message on the dashboard's **Alerts** page. Use these placeholders in your messages:

| Alert | Placeholders |
| --- | --- |
| New Follow | `{user}` |
| New Sub | `{user}` `{tier}` |
| Resub | `{user}` `{months}` `{streak}` `{tier}` `{message}` |
| Gift Subs | `{user}` `{amount}` `{total}` `{tier}` |
| Bits | `{user}` `{bits}` `{message}` |
| Raid | `{user}` `{viewers}` |
| Channel Points | `{user}` `{reward}` `{input}` `{cost}` |

For example, `Thanks {user} for the {bits} bits!` becomes "Thanks Ninja for the 500 bits!"

- The Bits alert is on by default, and has a minimum amount so small cheers can be skipped. The others start off until you turn them on.
- Gift subs are announced once per gift ("gifted 5 subs"), not once per person who received one.
- Alerts need you to have approved access (see [What you're approving](#what-youre-approving)), except raids, which work for every channel.

---

## Chat filters

Set up filters on the dashboard's **Moderation** page. Each one can **delete** the message, **time out** the chatter (you choose how long), or **ban** them:

| Filter | Catches | Options |
| --- | --- | --- |
| Block Links | Links like `https://…`, `www.…` and `example.com` | Let subscribers post links, and allow domains (`twitch.tv` is allowed by default, including clips) |
| Caps Spam | Messages that are mostly capital letters | How many capitals (70% by default) and how long a message must be. Emote names like `KEKW` don't count. |
| Emote Spam | Messages with too many emotes | Maximum emotes (10 by default) |
| Blocked Words | Words or phrases you choose, in any language | Your word list. Whole words only, so blocking "ass" won't catch "class". |

- Every filter starts off. Nothing changes in your chat until you turn one on.
- Moderators, VIPs and you are never filtered.
- If a message breaks several filters, only the strongest action is taken (ban, then timeout, then delete).
- Timed-out and banned chatters see the reason, like "Posting links".

### Letting someone post a link

Moderators can give a chatter a short window to post links with `!permit`:

```
!permit <user>          Lets them post links for 60 seconds
!permit <user> 300      For 5 minutes (up to 1 hour)
!permit <user> 0        Removes the permit early
```

A permit only lifts the link filter; the other filters still apply.

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
| `!permit` | | Moderators | Lets a chatter post links for a while |
| `!setprefix` | | Broadcaster | Changes the command prefix |
| `!join` | | Anyone, in [Nexus's chat](https://www.twitch.tv/nexus_app) | Adds Nexus to your channel |
| `!leave` | | Anyone, in [Nexus's chat](https://www.twitch.tv/nexus_app) | Removes Nexus from your channel |

`!followage` needs you to have approved access, or Nexus to be a moderator in your channel.

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

Nexus speaks 10 languages in Discord: English (US and UK), German, Spanish, French, Hindi, Japanese, Korean, and Simplified and Traditional Chinese. It replies in your Discord language automatically.

---

## Need help?

Join the [Nexus support server](https://discord.gg/ph8WmyuQRR) for help, to report a bug, or to suggest a feature.
