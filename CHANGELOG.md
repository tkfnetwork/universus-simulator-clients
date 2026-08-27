# Changelog

What changed in each build of the Universus Simulator client, newest first.

The version you are running is written in the corner of the main menu.

## 0.0.2

- Board is landscape and 4:3. Cards are drawn larger and the window opens at the
  board's own shape, so there are no black bars.
- Card pool sits above your own stage. Both run the full width of the board.
- A stage row holds ten foundations before it wraps.
- Deck, discard and removed from game stand in the right-hand channel. Token
  pile and momentum stand in the left. All are drawn in full.
- Arena is a full sized face up card in the left channel. Hovering one turns it
  upright.
- Turn banner sits below your own row instead of across the phase strip.
- Main menu is drawn larger to suit the narrower window.
- Fixed: finishing a mulligan with Ready gives back the cards you set aside on
  your deck. They were left there and the hand stayed short.
- Fixed: the deck manager and other menus ran off the top of the window. Every
  view now keeps a clear margin inside the screen.
- Fixed: the version stamp and the account line were carried off the bottom of
  the main menu when it was drawn larger.
- Fixed: an attack printed "this attack cannot be blocked" could still be
  blocked. Burning Fist is the card in Standard that says it.
- Fixed: a bonus granted to the next attack you play went to the attack being
  resolved instead, or to no attack at all. Unexpected Reunion's sacrificed
  foundation bought nothing.
- Fixed: the same misreading on seven more cards. Some lost the bonus outright,
  some gave away only half of it.

## 0.0.1

- First alpha build.
