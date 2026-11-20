# Privacy Policy

Kiwibot — the Discord bot and the Activities it serves · last updated 20 November 2026

**The short version.** Kiwibot stores what it needs to run the features a server asks for, and nothing
else. The Activity games keep nothing at all: a duel or a blackjack table lives in the game server's
memory while it is being played and is gone when it ends. Nothing is sold, and nothing is shared with
anyone but Discord, which the app has to talk to in order to work.

## What is stored, and why

- **Server configuration** — the settings a server's managers choose: which modules are on, which
  channels and roles they use, welcome text, shop items, log destinations, and so on. This lives in a
  SQLite database on the host the operator runs the bot on.
- **Member identifiers and the profile details a feature needs** — for example an id and a display name
  for levels, a balance for the economy, invite counts, a birthday, a reminder you asked for, or a
  linked game account. Stored per server, and only for the features that are on.
- **Linked game accounts** (Xbox, Steam) — only if you link one yourself. The stored access token is
  encrypted, the key is kept outside the database, and a stored record carries neither the token nor the
  key in readable form.
- **Activity sessions** — when you open a game, the Activity asks Discord for your user id, display name
  and avatar so the table can show who is playing, and receives the instance id of the voice-channel
  session. This is held in memory for as long as you are in the game, is never written to a database, and
  is not kept after the game ends.

## What is never done

- No advertising, no profiling, no analytics, and no tracking pixels.
- No selling, renting or sharing of data with third parties — the only other party involved is Discord's
  API, which the app must use to function.
- No reading of messages beyond the channels where a feature is explicitly watching for something (a
  counting channel, a suggestion channel, a bump reminder), and then only for that feature.

## Where the data goes

Kiwibot runs on a host the operator controls, and server data stays in that host's database. Activity
traffic passes through Discord's own proxy, because that is how Activities run; that part is covered by
Discord's Privacy Policy. The games send nothing anywhere else.

## Keeping it, and deleting it

- A server's settings are removed when the operator deletes them, and a member's row can be removed on
  request.
- To ask what is stored about you, or to have it deleted, contact us through the support server below
  and we will answer as quickly as we can.
- Activity game state needs no deletion: it never outlives the game.

## Age

Kiwibot is for people old enough to use Discord where they live (13 and over, or older where local law
requires it). It does not knowingly store data about anyone below that age.

## Changes and contact

When this policy changes, the date at the top changes with it. Questions go to
**dischub@icloud.com** or the support server **[dischub support server](https://discord.gg/tYW6T4G8FK)**.

---

*This page describes what Kiwibot actually does, in plain language rather than legal language, and the
operator of this instance is responsible for it.* · [Terms of Service](terms.md)
