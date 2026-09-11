---
title: "Lyrion Music Library"
description: Music source provider for Lyrion libraries
---

# Lyrion Music Library <img src="/assets/icons/lyrion.png" alt="Preview image" style="width: 70px; float: right;" loading="lazy" />

Music Assistant has support for the [Lyrion Music Server](https://lyrion.org/) library as a music source. This provider connects Music Assistant to an existing Lyrion LMS server and imports the music catalog, metadata, browse structure, and track URLs needed for playback.

This provider is designed to be used together with [Lyrion Players](/player-support/lyrion-player/), and that combination is recommended. Lyrion Music Library handles catalog and metadata, while Lyrion Players handles player control.

Shared setup details are on [Lyrion](/music-providers/lyrion/).

## Features

|           |                     |
|:-----------------------|:---------------------:|
| Subscription FREE | Yes |
| Self-Hosted Local Media | Yes |
| Media Types Supported | Artists, Albums, Tracks, Playlists |
| [Recommendations](/ui/#view---discover) Supported | No |
| Lyrics Supported | No |
| [Endless Mix](/ui/#track-menu) | No |
| Artist Top Tracks Support | No |
| Similar Artists Support | No |
| Similar Tracks Support | No |
| Maximum Stream Quality | Depends on the source/stream provided by Lyrion |
| Login Method | None |

### Other

- Imports and synchronizes library metadata from Lyrion
- Supports browse folders for artists, albums, tracks, playlists, and genres
- Supports search for artists, albums, and tracks
- Streams tracks by using Lyrion track URLs

## Configuration

1. Go to **Settings → Music Sources → Add a music source**.
2. Select `Lyrion Music Library`.
3. Enter the Lyrion host and JSON-RPC port (usually `9000`).
4. Finish setup and run a library sync.

## Works best with Lyrion Players

You can use this source with any Music Assistant player provider.

If you also use Lyrion-managed players, add [Lyrion Players](/player-support/lyrion-player/) as well. That lets Music Assistant and Lyrion keep queue metadata and playback behavior aligned more closely.

Without Lyrion Players, playback still works through other player providers, but you lose Lyrion-native player behavior.

## Provider setting

- `Rescan artwork now`: starts a new artist/album artwork refresh from Lyrion.

## Known Issues / Notes

- This provider reads what Lyrion has indexed. If content is missing, rescan or update the library in Lyrion first.
- Large libraries are browsed in pages, so seeing `Next Page` in browse views is expected.
- This source is best paired with [Lyrion Players](/player-support/lyrion-player/) if your players are managed by the same Lyrion server.
