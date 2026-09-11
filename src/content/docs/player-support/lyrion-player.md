---
title: "Lyrion Players"
description: Player provider for devices managed by Lyrion
---

# Lyrion Players <img src="/assets/icons/lyrion.png" alt="Preview image" style="width: 70px; float: right;" loading="lazy" />

Music Assistant has support for players managed by a [Lyrion Music Server](https://lyrion.org/). This provider discovers and controls players that are already known to a Lyrion server, including native queue sync and player grouping.

If your library is also in Lyrion, add [Lyrion Music Library](/music-providers/lyrion-music/) too. That combination is recommended.

## Features

- Discovers players known by Lyrion
- Supports all standard playback controls such as play, pause, seek, next/previous, volume, mute, and power
- Supports native Lyrion-style player grouping
- Mirrors queue updates between Music Assistant and Lyrion
- Works with mixed LMS-native and Music Assistant playback sources

## Configuration

1. Go to **Settings → Player Providers → Add a player provider**.
2. Select `Lyrion Players`.
3. Enter the Lyrion host and JSON-RPC port (usually `9000`).
4. Save and wait for discovery.

If players do not appear, make sure those players are connected to the same Lyrion instance.
If Music Assistant cannot reach Lyrion, check that the host/port is correct and that network/firewall rules allow access to port `9000` (or your custom port).

## Known Issues / Notes

- Play queue mirroring is skipped if the queue contains more than 500 items.
