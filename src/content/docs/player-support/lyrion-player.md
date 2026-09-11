---
title: "Lyrion Players"
description: Player provider for devices managed by Lyrion
---

# Lyrion Players <img src="/assets/icons/lyrion.png" alt="Preview image" style="width: 70px; float: right;" loading="lazy" />

Music Assistant has support for players managed by a [Lyrion Music Server](https://lyrion.org/). This provider discovers and controls players that are already known to a Lyrion server, including native queue sync and player grouping.

This provider is designed to be used together with [Lyrion Music Library](/music-providers/lyrion-music/), and that combination is recommended. Lyrion Players handles player control and queue behavior, while Lyrion Music Library handles catalog and metadata.

Shared setup details are on [Lyrion](/music-providers/lyrion/).

## Features

- Discovers players known by Lyrion
- Supports basic playback controls such as play, pause, seek, next/previous, volume, mute, and power
- Supports native Lyrion-style player grouping
- Mirrors queue updates between Music Assistant and Lyrion
- Works with mixed LMS-native and Music Assistant playback sources

## Configuration

1. Go to **Settings → Player Providers → Add a player provider**.
2. Select `Lyrion Players`.
3. Enter the Lyrion host and JSON-RPC port (usually `9000`).
4. Save and wait for discovery.

If players do not appear, make sure those players are connected to the same Lyrion instance.
If discovery still fails, verify the host and port on the shared [Lyrion](https://lyrion.org/) server and check the network path from Music Assistant.

## Why this pairs with Lyrion Music Library

`Lyrion Players` can play content from any Music Assistant source, but it works best together with [Lyrion Music Library](/music-providers/lyrion-music/) when your catalog also lives in Lyrion.

That pairing lets Music Assistant preserve more Lyrion-native queue behavior for Lyrion library tracks, while still handling non-Lyrion sources through Music Assistant streams.

## Known Issues / Notes

- Very large queues are guarded: queue mirroring is skipped above 500 items.
- Host and port values shown after setup are read-only and come from the saved setup flow.
- This provider works best when the players are managed by the same Lyrion server as the music library.
