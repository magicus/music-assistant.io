---
title: "Lyrion Players"
description: Player provider for devices managed by Lyrion
---

# Lyrion Players

This provider discovers and controls players that are already managed by a Lyrion LMS server.

Shared setup details are on [Lyrion](/music-providers/lyrion/).

## What to expect

- Discovers players known by Lyrion.
- Supports play, pause, stop, seek, next/previous, volume, mute and power.
- Supports native Lyrion-style player grouping.
- Mirrors queue updates between Music Assistant and Lyrion.

## Setup

1. Go to **Settings -> Player Providers -> Add a player provider**.
2. Select `Lyrion Players`.
3. Enter Lyrion host and JSON-RPC port (usually `9000`).
4. Save and wait for discovery.

If players do not appear, make sure those players are connected to the same Lyrion instance.

## Why this pairs with Lyrion Music Library

`Lyrion Players` can play content from any Music Assistant source, but it works best together with [Lyrion Music Library](/music-providers/lyrion-music/) when your catalog also lives in Lyrion.

That pairing lets Music Assistant preserve more Lyrion-native queue behavior for Lyrion library tracks, while still handling non-Lyrion sources through Music Assistant streams.

## Notes

- Status is experimental.
- Very large queues are guarded: queue mirroring is skipped above 500 items.
