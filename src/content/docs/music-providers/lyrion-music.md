---
title: "Lyrion Music Library"
description: Music source provider for Lyrion libraries
---

# Lyrion Music Library <img src="/assets/icons/lyrion.png" alt="Preview image" style="width: 70px; float: right;" loading="lazy" />

Music Assistant supports the [Lyrion Music Server](https://lyrion.org/) (LMS) library as a music source. This provider connects to a Lyrion server and imports catalog, metadata, browse structure, and track URLs for playback.

If your players are also managed by Lyrion, add [Lyrion Players](/player-support/lyrion-player/) too. That combination is recommended for the best Lyrion-native playback behavior.

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
- Supports search for artists, albums, and tracks
- Supports browse folders for artists, albums, tracks, playlists, and genres
- Streams tracks by using Lyrion track URLs

## Configuration

1. Go to **Settings → Music Sources → Add a music source**.
2. Select `Lyrion Music Library`.
3. Enter the Lyrion host and JSON-RPC port (usually `9000`).
4. Save and wait for discovery.

If Music Assistant cannot reach Lyrion, check that the host/port is correct and that network/firewall rules allow access to port `9000` (or your custom port).

## Provider setting

- `Rescan artwork now`: Cleares cached artist/album artwork and starts a refresh from Lyrion.

## Known Issues / Notes

- This provider reads what Lyrion has indexed. If content is missing, rescan
  the library in Lyrion first.
- If you change existing artwork in Lyrion, you must run `Rescan artwork now`
  to refresh it in Music Assistant. (Just adding new items does not require
  this.)
- Large libraries are browsed in pages, so seeing `Next Page` in browse views
  is expected.
