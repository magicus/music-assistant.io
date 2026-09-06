---
title: "Lyrion"
description: Shared setup notes for the Lyrion Music Library and Lyrion Players providers
---

# Lyrion

Use this page as the shared setup reference for:

- [Lyrion Music Library](/music-providers/lyrion-music/)
- [Lyrion Players](/player-support/lyrion-player/)

## Why there are two providers

Music Assistant splits library and player control into separate provider types.

- `lyrion_music` is a music source (catalog, search, library sync, track URLs).
- `lyrion_player` is a player provider (discover/control players, queue sync, grouping).

This is why both exist even though they connect to the same Lyrion LMS server.

## Before you add them

- Make sure your Lyrion server is running and reachable from Music Assistant.
- Use the Lyrion JSON-RPC endpoint host and port (default port is `9000`).
- If a firewall is in place, allow Music Assistant to reach Lyrion on that port.

## Recommended setup order

1. Add [Lyrion Music Library](/music-providers/lyrion-music/).
2. Add [Lyrion Players](/player-support/lyrion-player/).

The second provider can reuse host/port details from the first one, which reduces setup mistakes.

## Connection troubleshooting

If setup fails, these messages usually mean:

- `host_required`: Hostname/IP is empty.
- `invalid_port`: Port is not a number between `1` and `65535`.
- `host_unresolvable`: DNS/hostname cannot be resolved.
- `endpoint_unreachable`: Music Assistant cannot open a TCP connection to Lyrion.
- `endpoint_not_lyrion`: Host is reachable, but not a valid Lyrion JSON-RPC endpoint.
- `serverstatus_invalid`: Endpoint responded, but not with a valid Lyrion serverstatus payload.

Quick checks:

- Confirm the host/port in Lyrion itself.
- Test with the server IP instead of hostname.
- Avoid reverse proxy paths here; use direct Lyrion host + port.
