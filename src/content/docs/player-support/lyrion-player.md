---
title: "Lyrion Players"
description: Player provider for devices managed by Lyrion
---

# Lyrion Players <img src="/assets/icons/lyrion.png" alt="Preview image" style="width: 70px; float: right;" loading="lazy" />

Music Assistant supports players managed by a [Lyrion Music Server](https://lyrion.org/) (LMS) as a player provider. This provider connects to a Lyrion server and discovers/controls players, including native queue sync and player grouping.

If your library is also in Lyrion, add [Lyrion Music Library](/music-providers/lyrion-music/) too. That combination is recommended for the best Lyrion-native playback behavior.

## Features

- Expose all Lyrion players to Music Assistant
- Supports all standard playback controls such as play, pause, seek, next/previous, volume, mute, and power
- Play queues are mirrored between Music Assistant and Lyrion
- Grouping of players are mirrored between Music Assistant and Lyrion
- Tracks queued from a Lyrion Music library provider are treated as native Lyrion tracks, for a complete Lyrion-native playback experience
- Tracks queued from other sources are also handled correctly

## Configuration

1. Go to **Settings → Player Providers → Add a player provider**.
2. Select `Lyrion Players`.
3. Enter the Lyrion host and JSON-RPC port (usually `9000`).
4. Save and wait for discovery.

If players do not appear, make sure those players are connected to the same Lyrion instance.
If Music Assistant cannot reach Lyrion, check that the host/port is correct and that network/firewall rules allow access to port `9000` (or your custom port).

## Known Issues / Notes

- Play queue mirroring is skipped if the queue contains more than 500 items.
- Lyrion has a tri-state shuffle mode: "track shuffle", "album shuffle", and
  "no shuffle", while Music Assistant only supports "shuffle" and "no shuffle".
  If you set "album shuffle" in Lyrion it will just show up as "shuffle" in
  Music Assistant. There is no way to set album shuffle mode in Lyrion from
  within Music Assistant.
