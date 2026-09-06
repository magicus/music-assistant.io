---
title: "Lyrion Music Library"
description: Music source provider for Lyrion libraries
---

# Lyrion Music Library

This provider connects Music Assistant to an existing Lyrion LMS server library.

Shared setup details are on [Lyrion](/music-providers/lyrion/).

## What to expect

- Imports and syncs library metadata from Lyrion.
- Supports artists, albums, tracks and playlists.
- Supports search and browse folders (including genres in browse).
- Streams tracks by using Lyrion track URLs.

## Setup

1. Go to **Settings -> Music Sources -> Add a music source**.
2. Select `Lyrion Music Library`.
3. Enter Lyrion host and JSON-RPC port (usually `9000`).
4. Finish setup and run a library sync.

## Works best with Lyrion Players

You can use this source with any Music Assistant player provider.

If you also use Lyrion-managed players, add [Lyrion Players](/player-support/lyrion-player/) as well. That lets Music Assistant and Lyrion keep queue metadata and playback behavior aligned more closely.

## Provider setting

- `Rescan artwork now`: starts a new artist/album artwork refresh from Lyrion.

## Notes

- Status is experimental.
- This provider reads what Lyrion has indexed. If content is missing, rescan/update the library in Lyrion first.
