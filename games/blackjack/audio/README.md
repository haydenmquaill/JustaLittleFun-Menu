# Blackjack HOST audio

Two manifests load at runtime; the host decodes whatever clips exist. **Every clip
is optional** — a missing file just stays silent and the game runs identically, so
you can add audio incrementally.

## Buses
- `music` — background playlist + fanfare
- `ambience` — cheer sting
- `sfx` — cards, chips, flip
- `voice` — dealer voice lines (ducks the other buses while playing)

## Adding variations
Any `url` (SFX) or line key (voice) that is an array holds interchangeable takes;
one is chosen at random each play. Add more by extending the array. Filenames only
need to match what you list. Hard-refresh after editing a manifest (JSON is cached).

## SFX  (`audio/sfx/sfx-manifest.json`)
Keys the game fires:
- `cardDeal` — per card as it slides in (deal, hits, dealer draws)
- `holeFlip` — dealer hole card flip
- `chipBet` — round start; on a player double; on a player split; and with the
  dealer outcome line when at least one player won
- `uiWhoosh` — screen wipe
- `fanfare` + `cheer` — finale winner reveal

(There are intentionally no bust/win/push/blackjack SFX — voice handles those.)

## Background music  (`music` array in the SFX manifest)
Plays from initial load in a shuffle bag (every track once before any repeat, no
repeat across the seam). Each entry `{ url, title, artist, cover }`; only `url`
required. The Now Playing toast (bottom-left, ~5s) is suppressed on the lobby/menu.

## Dealer voices  (`audio/vo/<pack>/vo-manifest.json`)
Three packs: `classic`, `vegas`, `smooth` — one chosen at random per session.
Every pack shares the same keys, each an array of takes (3 scaffolded). Drop files
at e.g. `audio/vo/vegas/dealer_bust/2.mp3`.

Event lines: `placeYourBets`, `betsClosed`, `dealersTurn`, `playerBust`,
`playerBlackjack`, `dealerBust`, `dealerBlackjack`, `dealerWin`, `dealerLose`,
`dealerPartial`, `pushAll`, `pushWinner`, `pushLoser`, `pushMixed`, `winner`,
`signoff`.

Hand-total calls (players only): `total_4` … `total_21` under `total/<n>/`.

### When each voice line fires
- `placeYourBets` — betting opens
- `betsClosed` — betting locks
- `playerBlackjack` — at deal, once per player dealt a natural (1s beat between)
- `total_N` — a player's hand total, called as each card finishes sliding in
  (turn start, and on every hit). Never for the dealer.
- `playerBust` — a player hand goes over 21
- `dealersTurn` — dealer begins to play
- `dealerBlackjack` / `dealerBust` — dealer state line (plays first, then an
  outcome line follows)
- Outcome line (always, after settle):
  - any tie present → `pushAll` / `pushWinner` / `pushLoser` / `pushMixed`
  - no ties → `dealerWin` (nobody beat dealer) / `dealerLose` (all beat dealer) /
    `dealerPartial` (mixed)
- `winner` + `signoff` — finale

## Timing
Card animation is 300ms; the turn loop polls every 150ms; total/bust calls fire as
the card finishes sliding in, so the sound lands with the card rather than early.

## Adding a fourth dealer
Create `audio/vo/<name>/vo-manifest.json` + folders and add `"<name>"` to the
`DEALER_PACKS` array near the top of the audio block in index-HOST.html.
