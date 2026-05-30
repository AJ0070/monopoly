# monopoly

A JavaScript/HTML/CSS Monopoly implementation with full game play. Supports two-to-eight players.

Play online at [http://www.intrepidcoder.com/projects/monopoly/](http://www.intrepidcoder.com/projects/monopoly/).

## Features

- **Full classic economy** — buying, rent (with monopoly doubling, railroad/utility scaling, and mortgaged-property exemptions), houses & hotels with the even-build rule and the 32-house / 12-hotel bank limit, mortgaging, auctions, and player-to-player trading.
- **Online multiplayer rooms** — the host creates a room, shares a code or invite link, and guests join seats from their own browsers (peer-to-peer via PeerJS). The host stays authoritative and syncs the board to every seat. Empty or open seats can be filled by the AI.
- **Resilient connections** — a live link-status indicator, automatic snapshot resync for players who (re)join mid-game, client auto-reconnect, and graceful hand-off of an abandoned seat to the computer so play never stalls.
- **Local hotseat** — play with everyone on a single device.
- **Live game board** — a polished, responsive board with a center panel showing whose turn it is, the current dice, and a scrolling game log of every action.
- **AI opponents** — an experimental, example AI player is included (`ai.js`).

## Running

It is a static site — open `index.html` over any HTTP server (online multiplayer needs network access for the PeerJS signalling server and the CDN scripts):

```sh
python3 -m http.server 8000
# then visit http://localhost:8000/index.html
```

To switch to the New York City edition, comment out `classicedition.js` and uncomment `newyorkcityedition.js` in `index.html`.
