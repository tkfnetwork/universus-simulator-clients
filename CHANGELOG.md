# Changelog

What changed in each build of the Universus Simulator client, newest first.

The version you are running is written across the bottom of the home screen, in the middle.

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
- Fixed: Young and Free sealed one of your own foundations. It prints a choice
  between unfreezing and unsealing, and both halves were being carried out.
- Fixed: Vengeful Intent, Backstab and Plate of the Dawnmartyr charged your
  rival's price for cancelling to you as well. You discarded a card, or flipped
  two foundations, for nothing.
- Fixed: Plate of the Dawnmartyr never took the 5 health it prints.
- Fixed: Duplicitous Recollection and Momo Yaoyorozu (III) built the card being
  resolved instead of the card you chose from your discard pile. King Ghidorah,
  Emperor of the Cosmos removed the wrong card the same way.
- Fixed: The Beast Titan's Call never milled, and rebuilt itself rather than the
  Titan card it turned over.
- Fixed: Aerial Reinforcement and Seize Opportunity never asked you to name a
  keyword, so nothing was drawn and Seize Opportunity counted your whole card
  pool.
- Fixed: Abyss Damnation's seal was permanent. It is given back when the attack
  resolves unless you have a Heat token.
- Fixed: Oxygen Destroyer refused to be played from your discard pile after you
  had destroyed two of your rival's cards, which is exactly what it asks for. It
  was counting the cards your rival had destroyed rather than the ones they
  lost, so your rival destroying two of yours let it through instead.
- Fixed: Hange's Thunder Spear Strike, Rabbit Finesse and Chucking Cars never
  noticed a card being destroyed. Each of them asks whether a foundation or an
  asset has been destroyed, and only one of the ways a card can be destroyed
  was being recorded, so destroying a foundation the ordinary way told them
  nothing at all.
- Fixed: Swagger Step never noticed you readying a card. It asks whether you have
  readied a card in your stage, and "ready this card", which 45 abilities
  print, was recorded nowhere. Readying one of your rival's foundations was
  written down as though the card had been yours, which armed it instead.
- Fixed: Rooftop Rumble did not see you committing a card. It asks whether you
  committed a foundation during the Enhance Step, and "commit this card",
  which seven abilities print, was recorded nowhere, along with three other
  ways an effect commits one.
- Fixed: Shoot Style: Knee Smash, The Final Test and Master of a Thousand
  Faces never noticed a card discarded to pay for something. Each asks whether
  a card has been discarded, and discarding is the price of 68 abilities, so
  the commonest way you discard, paying for the very ability that then asks,
  was recorded nowhere. Milling to pay a price was silent in the same way.
- Fixed: Interview Specialty and Dorian's Lute never noticed a card being
  revealed. Both ask whether you have revealed one, and revealing a card to pay
  for an ability, which is how most reveals happen, was filed under a different
  question entirely. Revealing a card from your hand, the way Heaven or Hell
  does, was not written down at all.
- Fixed: Last-Second Dodge did not remove Throw from the attack.
- Fixed: Massive Blow did not make your rival flip a foundation.
- Fixed: 80% Power had your rival build one card face up rather than two
  committed.
- Fixed: Potato did not build itself, and Big Freakin' Explosion did not take
  the health it costs you.
- Fixed: The Rumbling, Triple Trouble, I-No, Ramlethal's Greatswords and Reboot
  never offered your rival the chance to cancel them.
- Fixed: an attack printed "this attack cannot be blocked" could still be
  blocked. Burning Fist is the card in Standard that says it.
- Fixed: a bonus granted to the next attack you play went to the attack being
  resolved instead, or to no attack at all. Unexpected Reunion's sacrificed
  foundation bought nothing.
- Fixed: the same misreading on seven more cards. Some lost the bonus outright,
  some gave away only half of it.
- Fixed: counters with a two word name were never placed. King Ghidorah and
  Devil Gene counters went missing, so every card reading them found nothing.
- Fixed: a card that removes itself "with a counter on it" dropped the counter.
  The counter is the mark used to play the card back out of the removed pile.
- Fixed: a card drained at the start of the End Phase waited for a counter it
  was supposed to place itself, so it sat in the pool forever.
- Fixed: counters added to a card in your rival's stage went onto your own
  card, and your rival's screen never drew the badge on the card carrying it.
- Fixed: the win condition counting your rival's foundations ignored whether
  they carried counters, and could win the game off an ordinary board.
- Fixed: spending a counter to pay a cost left the old number on the card.
- Fixed: Destoroyah Emerges and Standing Tall were not sacrificed on your
  rival's screen when you paid for them with Power tokens. They went on seeing
  the card sitting on your board after you had spent it.
- Counter badges are coloured for every counter in Standard. Seven were drawn
  white.
- Fixed: sixteen Form abilities whose name carried a qualifier in front of it,
  such as Deadlock Form Commit or Warrior First Form, could not be played at
  all.
- Fixed: an attack printing "cannot be blocked by mid attacks" or "cannot be
  partially blocked" was blocked anyway.
- Fixed: a block bonus granted by a card in your card pool never applied, and
  did not stop when the card left the pool.
- Fixed: "your checks to play attacks get +1" raised every check you made, not
  only the ones it names. Nine cards print the wider version, and two more
  print it on a character where it did nothing at all.
- Fixed: nine cards let you pay a keyword's momentum cost another way, and none
  of them ever offered it.
- Fixed: "commit assets as though they were foundations" counted the asset
  toward passing the check and then would not let you click it.
- Fixed: two cards that act at the start of your End Phase or Combat Phase
  never fired.
- Fixed: "ready 1 non-Unique asset or foundation" offered foundations only, and
  could offer a Unique card.
- Fixed: a card that removes itself when it leaves your card pool was discarded
  instead.
- Fixed: a card that rebuilds itself face down committed when cleared during
  your Combat Phase went to the discard.
- Fixed: an attack that removes itself the fourth time it is played in a turn
  never did.
- Fixed: "if you would mill 1 or more cards, mill that many plus 1 instead"
  did nothing.
- Fixed: a character that replaces losing the game replaced it and then never
  paid for it. King Ghidorah's three lives were unlimited ones.
- Fixed: two of the three characters that replace losing the game did not.
  Reiner Braun never transformed, and Kazuya's Devil Gene counter never went on.
- Fixed: the peer whose character died called the game before its own character
  could answer, so a replacement could not arrive in time.
- Fixed: the game was awarded to the wrong player when a killing blow was
  replaced and then landed anyway.
- Fixed: an attack printing its own bonus as a continuous rule was played at
  its printed numbers. Rurouni Kenshin's speed and damage per attack in your
  card pool counted nothing.
- Fixed: "rival effects cannot modify your check to play this card" did not
  stop them.
- Fixed: a card you may play as a block from your stage was removed as the
  ability resolved, so it never blocked.
- Fixed: Sung Jinwoo's choice of skill tree was never offered. The Assassin
  tree could not be taken, and levelling up read the wrong tree.
- Turn start token clean-up reads what a token prints rather than being named
  after Roman Cancel.
- Fixed: Yusuke's Enhance offering a Spirit card from your discard pile, and
  All For One's offering a card from your momentum, offered nothing. Both cost
  a commit and then removed the attack you were enhancing instead.
- Fixed: a card played out of your discard pile or momentum that way is removed
  when it leaves your card pool, rather than going to momentum.
- Fixed: "flip 1 rival foundation" committed it instead. Flipping turns a card
  face down, which blanks its abilities and leaves it ready; committing turns it
  90 degrees and does the opposite of both. 23 abilities across 21 cards.
- Fixed: "flip 1 rival foundation with difficulty 2 or less" could flip any
  foundation, the cap was dropped.
- Fixed: Reiner Braun's "commit or flip" and Isla's "seal or flip" did both
  halves instead of asking which.
- Fixed: Chu's "commit and flip 1 rival foundation" only committed.
- Fixed: Ursine Might's "flip 1 rival asset or foundation", Tetsutetsu Fury's
  "if your rival has 8 or more foundations, flip 1 of them" and the commit and
  flip steps of Colossus Titan's Destructive Power were not read at all.
- Fixed: Outwit abilities were playable at any time off a face up card, which is
  the one place the rules do not allow, and were never playable off the face down
  card that is the only place they are. They now also pay their inherent cost of
  unflipping and committing the card, so they cost something and are not
  repeatable. 11 abilities.
- Fixed: three flips that limit which rival foundation they may reach ignored the
  limit and could flip any of them. Destructive Heat Ray reaches a difficulty
  below the number of Power tokens in your stage, Beckett Mariner one matching
  the foundation you just unflipped, and William Anderson III one matching the
  foundation his cost moved to your hand. Where the card the limit names does not
  exist, nothing is a legal target.
- Fixed: Power tokens were counted in the stage rather than the token pile they
  are held in, and by the wrong card number, so the count was always zero. Anguirus
  Ball's difficulty reduction and Crushing Impact's speed both scaled off nothing.
- Fixed: freezing a rival foundation also committed it. Freezing only denies the
  card its owner's next Ready Step, so the commit was a second punishment no card
  granted.
- Fixed: four cards print "commit and freeze" or "commit and seal" and only the
  second half was read. Phantom Sway, Dance of the Phoenix, Rapid-Fire Prism
  Beams and Frenzied Dive now commit as well.
- Fixed: Shackling the Attack Titan did nothing at all beyond its condition.
- Fixed: nine cards name which rival foundation a freeze or a seal may reach and
  the restriction was dropped. Chronically Dehydrated reaches a ready foundation
  only, and eight others reach only a named element.
- Fixed: Ky Kiske offers "commit or freeze" and always committed, without
  asking.
- Fixed: a freeze or a seal with one legal target asked which one anyway.
- Fixed: "look at the top card of your deck, you may discard it" never offered
  the discard. Yelena's Machinations, Luke Sullivan and Get the Scoop only
  looked, and Sword Advantage's reveal did the same.
- Fixed: Toru Hagakure (II) looked at your rival's deck and did nothing else.
- Fixed: "reveal the top N and discard the rest" left every card revealed on top
  of the deck. Offensive to Retake Wall Maria, Unit Commander and Wild Wild
  Pussycats drew nothing and discarded nothing; Golden Death kept its cards but
  not the discard.
- Fixed: Master's Touch readied foundations and never froze them.
- Fixed: three seals were never read. White Angel of Death and Xangô print
  "seal this card", and Power of the Monsters seals a card in your rival's
  stage.
- Fixed: "add it to your hand" meant this card wherever the sentence named
  another one first, so fifteen abilities bounced themselves.
  - Resurrected Titans, Colossal Confrontation, Zeke Yeager, Xilien Agent and
    Yoshimitsu searched a card into hand and then added themselves as well.
  - Smarts over Strength, Mikasa Ackerman, Persuasive Talent and Genkai kept the
    attack instead of the card they revealed.
  - Massive Abnormal Titan and The Manipulations of Zeke Yeager kept the attack
    instead of the card they milled.
  - Painful Experiment and Female Titan Attacks! kept the attack instead of the
    card chosen from your discard pile.
  - Teamwork Attack returned the attack and left the chosen backup in your
    stage, so the damage it grants counted nothing.
  - Seize the Opportunity looked at four cards, took none of them and left all
    four on top of the deck.
- Fixed: Annie Leonhart and Rose Whip Barrage built themselves instead of
  searching. Rose Whip Barrage also searches the removed from game pile, which
  nothing reached.
- Fixed: a recall naming two keywords ("1 Ranged or Titan card") matched no card
  at all.
- Fixed: Insubordination, Fighting for Control, SpaceGodzilla Bio-Quartz
  Monster, The Power of SpaceGodzilla, Godzilla vs SpaceGodzilla, Twisted
  Reflection and Mollywhop ended your rival's Combat Phase when the check they
  penalise failed. Each of them prints that it does not.
- Fixed: A Promised Toast, Queen of Compassion, Combined Perfect Form,
  Diverting Energy, Drawing Power and Reiner Braun applied their fallback
  number on top of the number you paid for rather than in place of it. A Promised
  Toast gave +6 speed rather than +4, Drawing Power drew 3 rather than 2.
- Fixed: Reiner Braun, Jaws of Life, Combined Perfect Form and Drawing Power
  offered a price and never charged it. The foundation, the counter and the
  Power tokens all stayed where they were.
- Fixed: Jaws of Life could be paid with any foundation. It asks for difficulty
  2 or greater.
- Fixed: Giving in to Rage gave +6 damage. It prints +4 or +2 depending on
  whether the card you discarded was the harder of the two, and that gate was
  never read.
- Fixed: Colossus Swat and Lightning Rod kept the foundations they build for
  good. Both print that you give them up at the end of the turn.
- Fixed: Everlight's Grace milled and added nothing to your hand. Story Pizza
  milled and gained health but never took the foundation.
- Fixed: Limited Entry added nothing to your hand unless you held a Heat token.
- Fixed: Replicator Enthusiast built any foundation from your discard pile
  rather than one named by the card you chose, and never let your rival build.
- Fixed: Historia's Declaration placed no Wall counters, and gave its damage
  bonus whether or not the chosen card carried one.
- Fixed: Twins' Bond cleared nothing from either card pool, and gave its speed
  and damage whether or not the two cards shared a type.
- Fixed: Cabal's Ruin milled nobody when you removed five or more counters.
- Fixed: Clash with the Bloodred revealed nothing, so it always took the
  winning branch.
- Fixed: Dorian Storm, Charming Minstrel revealed the top card of your deck and
  then did nothing with it.
- Fixed: Net Launcher never had your rival build the card you chose.
- Fixed: Secretary of Defense sealed once instead of twice. The second seal is
  at the start of the next turn.
- Fixed: Jin Kazama gave the damage half of its Devil Gene bonus and not the
  speed penalty on rival attacks.
- Fixed: G Corp Soldier's stamina-for-health trade did nothing at all.
- Fixed: Restore Ally gained no health.
- Fixed: Catching a Meteor milled until it found an attack and then did not
  play it.
- Fixed: Idun Box left the attack in the zone it had been moved to, and left it
  unblockable.
- Fixed: Koenma's Task searched your own deck twice and never your rival's.
- Fixed: Engage the Monster always took two Power tokens. Below the printed
  threshold it takes one.
- Fixed: Weight of Responsibility never asked you to spend momentum, so the
  health it takes off your rival was always zero.
- Fixed: Vox Machina had neither player spend momentum, and gave a flat +1
  where the printed bonus counts each player who spent.
- Fixed: Okey Dokey! gave the attack no keyword from the discarded card.
- Fixed: Strategic Maneuver never let you choose an asset, and never built it.
- Fixed: To You, 2,000 Years From Now and Dolores, Hidden Wisdom looked at the
  top of your deck and then did nothing with what they found.
- Fixed: Tomura Shigaraki, All For One's Successor did not offer to play a card
  it removed, and drew no cards for them.
- Fixed: Nick Ragan readied any foundation instead of one named like a card it
  removed.
- Fixed: Power of Youko took a card from your own hand rather than your rival's
  card pool.
- Fixed: Guerreiro Explosivo's second option did not freeze, and did not check
  for a Heat token.
- Fixed: Badgey, Vengeful Pal and Kinoko Komori print an ability either player
  may play, and the rival was offered nothing.
- Fixed: an ability either player may play could be played once by each of them
  in the same Enhance Step.
- Fixed: Nick Ragan offered no enhance from the attack cards it removed on your
  own turn.
- Fixed: Kuwabara, Spirited Warrior and Spirit Sword Ultimate print an enhance
  playable any number of times per Enhance Step, and it could be played once.
- Fixed: Stomp of the Female Titan doubled every bonus an attack received, with
  no limit; it is playable 3 times per attack.
- Fixed: War Hammer Titan and War Hammer Strike gave their full +6 at any
  health, instead of losing 1 for every 5 health you have.
- Fixed: Heidern, Hard-Boiled Assassin and Heidern End revealed the rival's hand
  and then discarded nothing from it.
- Fixed: Heidern End made the rival draw 1 card rather than 1 for each attack
  discarded.
- Fixed: Jester Lavorre, Prankster Priestess did not add either player's top
  card to their momentum.
- Fixed: Izuku Midoriya, Quirks Unleashed did not skip the Enhance Step of the
  attack it slowed.
- Fixed: World's Weakest Hunter never offered the foundation removal that its
  draw counts.
- Fixed: Dance of the Phoenix froze nothing unless the rival had 10 or more
  foundations.
- Fixed: The Intensity of Mikasa Ackerman and This Is My Chance!! never applied
  their bonus. Both ask about the only attack in your card pool, and neither is
  an attack itself.
- Fixed: The Intensity of Mikasa Ackerman gave no damage. Its bonus equals the
  attack's printed speed, up to 6.
- Fixed: Ocean Buddies gave your rival no card at all unless you had played a
  Roman Cancel ability. The Roman Cancel only turns their card face down.
- Fixed: April O'Neil, High School Reporter let you pick the branch. The milled
  card's check value picks it.
- Fixed: April O'Neil, High School Reporter drew a card without the review it
  charges for.
- Fixed: Coup de Chevalier offered its whole menu on every commit, so one attack
  could take the same branch three times.
- Fixed: Robert never offered the hand discard that stands in for momentum on
  its Powerful ability.
- Fixed: Commander's Rage took a Wall counter whether or not you used it to pay
  for Powerful. It is an offer, not an order.
- Fixed: Wingnut, Mechanical Genius gave the sealed foundation straight back. It
  seals it again at the beginning of your rival's turn.
- Fixed: Secretary of Defense re-sealed every foundation sealed that turn rather
  than the one it named.
- Fixed: Acceptable Losses and Pact of Wrath never charged the health they offer
  to lose, so the bonus counting it was always zero.
- Fixed: Pact of Wrath made your rival spend momentum whether or not you lost the
  health that pays for it.
- Fixed: Cull the Weak drained the backup being attacked rather than the one you
  chose.
- Fixed: Shinobi Prodigy never slowed the next attack.
- Fixed: Keg never took the attack aimed at another backup.
- Fixed: Heaven or Hell turned no card over, and offered your whole discard pile
  instead of a copy of the card revealed.
- Fixed: Cammy, Covert Chameleon never made its check, so it never flipped and
  committed after being attacked.
- Fixed: Memory Upgrade gave you nothing. You now take the first Enhance of the
  attack it responds to.
- Fixed: A Gift Returned offered your whole discard pile rather than cards with a
  check value of 6.
- Fixed: Around the World offered your whole discard pile rather than the two
  cards it names.
- Fixed: Uraotogi Expertise offered any foundation rather than one sharing three
  symbols with your character.
- Fixed: Canister Creation Strike offered any foundation rather than one at the
  printed difficulty it works out.
- Fixed: Leatherhead, Eager Expat added two cards to your rival's card pool
  whether or not they had ten foundations.
- Fixed: Caleb Widogast, Fiery Transmuter offered your whole discard pile. It
  returns a Spell card with the same difficulty as the one you discarded to pay
  for it.
- Fixed: Shroom-Shooter put both Mushroom counters on itself instead of the two
  foundations you choose.
- Fixed: Splitgill Lung Strike put its counter on itself rather than on the card
  you pick in either player's stage.
- Fixed: Gunslinger's Focus let you block with any card in hand, but that block
  was worth nothing. It now carries the +2 mid block modifier it prints.
- Fixed: Itsuka Kendo's hand size was cleared before your own draw step, so it
  never lasted until the end of your next turn.
- Fixed: an empty window stopped auto-passing when priority arrived before your
  rival's board had finished loading.
- Fixed: a card rebuilt to keep the two boards in step was counted by a zone
  that never drew it, so it was invisible on your side.
- Fixed: leaving a game while a mill was still on screen left the milled card
  out of the discard pile shown to you.
- Fixed: "cancel it" did nothing. Forty-two cards print it, and the ability they
  answered went on to resolve in full. High-Speed Dodge, Drive Parry, "Strange
  Energies" and the rest are now offered the moment your rival plays an ability,
  before its effects happen.
- Fixed: Lock and Load's Blitz never cancelled the first enhance your rival
  played during the attack.
- Fixed: a response written "after your rival plays a Blitz ability" or "after
  your rival plays an enhance ability" was offered to the wrong player during
  your rival's attack.
- A cancelled ability has still been played, so its cost stays paid and it
  still counts against what can be played this step.
- Fixed: Dexterous Assault and Vagrant Truthseeker never let you change the
  block zone of the card you had just played as a block. You were never asked,
  and the block was scored against the zone printed on the card.
- Fixed: Invisible Infiltration gave the removed foundation back one attack
  late, and not at all if the turn ended first. A dropped attack does not
  resolve, so it no longer gives it back at all.
- Fixed: Weathered Fury's delayed health loss was paid at the same wrong moment.
- Fixed: The Apathy of Annie Leonhart committed itself and bought nothing. Click
  it during the Block Step to block with it.
- Fixed: blocking with a backup from your stage left your rival's screen showing
  the card in two places.
- Fixed: Twin Twains never made your rival add a second option to their
  Diplomacy card's ability.
- Fixed: Dragon of the Darkness Flame's discard from hand paid the Powerful cost
  but counted for none of the damage, and only ever spent one card of the three
  it prints.
- Fixed: an attack keyword with an alternative cost was hidden entirely when
  your momentum was empty, which is the board those cards are printed for.
- Fixed: Rock'n Roll Circus did nothing at all. It never offered to change its
  own block zone, and its damage bonus counted no block zones, so it was always
  +0. Changing the zone is what adds a zone to your card pool for it to count.
- Fixed: Ling Xiaoyu's Enhance counted no block zones either, so it added no
  damage.
- Fixed: the middle block zone counted as two zones, because some cards print
  it as "middle" and others as "mid". Ling Xiaoyu's draw could be taken with
  only two real zones in your card pool.
- Fixed: a face down card in your card pool counted as a block zone. A face
  down card has no printed properties.
- Fixed: nineteen abilities that print what to sacrifice took the card they are
  printed on instead. Bite and Claw and Horseback Charge spent the attack
  itself, and William Anderson III spent the character.
- Fixed: a Power token price now spends a Power token. Thirteen abilities read
  it as sacrificing themselves, Cybertronic Weaponry among them.
- Fixed: "Sacrifice 1 ready foundation" no longer accepts a committed one, and
  the face up and face down prices each check the facing of the card you pick.
- Fixed: "Sacrifice 1 Titan backup" now requires a Titan.
- Abilities whose price cannot be paid are no longer offered.
- Fixed: "after this attack receives a speed bonus of 3 or greater" now reads
  the bonus it was given rather than the total the attack is carrying. Fa Jin
  Flurry fired on three separate +1s, and Third Wielder: Fa Jin never fired at
  all.
- Fixed: Shin Hashogeki's damage threshold was dropped entirely, so it fired on
  a bonus of +1.
- Fixed: Predatory Bite healed 0. It reads the sacrificed backup's remaining
  stamina, which was never recorded.
- Fixed: Destoroyah Emerges and Standing Tall sacrificed no Power tokens and
  ignored "with difficulty X", so they could destroy or build any foundation.
  You are now asked what X is and the target must match it exactly.
- Fixed: Izuku Midoriya, On the Move's second Form committed the character
  instead of X foundations. X is 3 minus the face down cards in your card pool.
- Fixed: Tinker's Touch always granted Powerful, and at rating 2. It offers
  EX: 2, Powerful: 3 or Stun: 1, and you now pick.
- Fixed: Desperate Plea always built face up. You are now asked face up or face
  down.
- Fixed: Merciless Lead always removed from both decks. You now choose which
  players it hits, including neither.
- Fixed: Healing Spell gave the stamina to the first backup in your stage. You
  now choose the backup.
- Fixed: Horn Dash Hammer added its counter to the first card carrying one. You
  now choose the card, in either stage.
- Fixed: Soothing Grog's Rage treated your rival's character as a target at any
  counter count, and preferred it over every other card. The printed threshold
  of 4 is now enforced and you choose the card.
- Fixed: Jet Uppercut took the first 4 cards in your discard pile. It is "up to
  4" of your choice, and its damage bonus counts the non-attacks you picked.
- Fixed: cards that pick from your rival's discard pile showed you your own pile
  instead. Devour Your Power, Sins of the Past, Joining the Fight, Invite Hell,
  Malicious Assault, Vanishing Storm and Disintegration removed nothing at all
  whenever your rival's pile held more than one card they could take.
- Fixed: Jet Haymaker and Immense Showdown always used your own discard pile.
  They read "a player's", so you now choose whose, and they no longer ask how
  many: the count is printed.
- Fixed: Krista Lenz only put a card back from your own discard pile, and picked
  it for you. It reaches both piles now, and you choose the card in each.
- Fixed: Special Report offered your rival's discard pile only when your own was
  empty. You now choose the pile and the card.
- Fixed: Trickster's Blessing took the last card of your own discard pile, and
  your rival's screen never saw the move at all.
- Fixed: Decompose removed cards from your rival's discard pile on your screen
  only. Your rival kept holding them.

- Fixed: Disciplined Maneuver and Eren Yeager removed nothing at all unless
  your discard pile held the whole count they name. They now remove what is
  there, and Disciplined Maneuver's damage counts the cards that moved.
- Fixed: Bladed Uppercut never raised its own EX rating, and Gargantuan Grapple
  raised nothing. Raising every keyword rating reached Powerful and Stun only.
- Fixed: a keyword rating printed at 0 was read as no keyword, so Gargantuan
  Grapple's Breaker 0 and Stun 0 could not be raised.
- Fixed: Training Todoroki's damage read four of the six rated keywords and
  ignored any rating another card had raised.
- Fixed: a raise to Powerful, Stun or EX was dropped, so Gas Propellant and
  Appendage Onslaught did less than they printed.

- Fixed: searching your deck laid the results out past the top and bottom of
  the window with no way to scroll, so the first and last rows could not be
  read or clicked. The results scroll now and the panel fits the window.
- Fixed: Sacrifice for the Cause discarded the card and added no damage. Its
  "X equals the block modifier of the discarded card" read the cost's cards
  after they had already been handed on, so X was always 0. Dash toward
  Disaster, Genkai and Borrowed Energy read the discarded card the same way.

- Fixed: 409 cards carried none of their printed keywords. Cards that print
  their keywords in the stat line rather than the keyword list had no Fury, no
  Punch and no Weapon as far as the game was concerned, so blocking
  restrictions, triggers and "for each Fury attack" all answered off the wrong
  half of the card.
- Fixed: a keyword a card only grants under a condition was read as a keyword
  it prints. On 51 cards, including Blizzard Rush and Kamuriyuki, the granted
  rating applied unconditionally.
- Fixed: Bakugo's Gauntlet raised every one of its keyword ratings instead of
  the one you pick, and never asked. It prints "1 of".
- Fixed: the keyword rating prompt offered Powerful, Stun and EX only, and
  skipped any keyword the attack prints at 0. Bakugo's Gauntlet was offered two
  keywords it does not carry and neither of the two it does.
- Fixed: Nature's Tempest chose your foundations for you, keeping the first of
  each name, and flipped only your own board. You now pick which copies stay
  face up and how many, and both players see the flips.
- Fixed: Jet Jaguar built the first foundation in each discard pile rather than
  one you name, and the rival half took a card off the top of their deck
  instead.
- Fixed: a bonus printed with a condition on it was given off any board at all.
  Annie Leonhart, Awakened, The Curiosity of Armin Arlert, Nott's Flask, Evil
  Aura and Jin Kazama.
- Fixed: eleven abilities that print an "If ..." and then a payoff paid the
  payoff regardless of the board. Among them Welcome To Space Land counting
  face down foundations, Xilien Agent asking whether your rival is at Deadlock,
  Megalomania counting sealed cards, "Big Sister" of 1-B comparing hand sizes
  and Master of Wind asking whether it is your only attack.
- Fixed: Rifle Arm added both of the speed changes it offers instead of one.
- Fixed: Positional Advantage checked whether it was your only attack and then
  did nothing. Its payoff, your rival returning a foundation to their hand, was
  never carried out.
- Fixed: face down foundations were not counted as foundations. Nineteen checks
  were affected, Deadlock among them, so a stage built face down was invisible
  to all of them.
- Fixed: sacrificing a face down foundation did not count as sacrificing a
  foundation, so nothing waiting on a sacrifice was paid.
- Fixed: Thunder Spear trimming its own third copy was announced as a sacrifice.
  It is destroyed, and the sacrifice paid every ability waiting on one.
- Fixed: counts of printed difficulty on foundations read the hidden face of
  face down cards.
- Fixed: "build it" built the card printing the ability instead of the card you
  had just played, blocked with or checked. Rapid Rescue, Creative Counter,
  Nejire Hado (II), Size Specialist, Bishop, Donatello, Izuku Midoriya,
  Younger Toguro, Beast Titan and Radiant Pegasus Bomb.
- Fixed: gates that count what has already happened counted nothing, so the
  reward was handed over on any board. Jean Kirstein counting cleared cards,
  War Hammer Titan counting sacrifices, Change of Plans counting blocks,
  Lethal Slash and Smoke-Screened Ambush counting cards played, Tempest Demon
  God Fist counting momentum spent, Rooftop Rumble and Rinku counting commits,
  Hange's Thunder Spear Strike and Rabbit Finesse counting destroyed
  foundations, and Cornered Dagger Master watching the discard pile.
- Fixed: "If you did" paid out whether or not you did it. Armin Arlert,
  Scared Strategist and Vex, Siren now pay on either half of the choice they
  offer, and Meeting Hange, Battle for Dominance, Wielding One For All and
  Midnight (II) read what the operation actually touched.
- Fixed: rewards waiting on a check that had not been made yet were paid
  immediately. SpaceGodzilla and Twisted Reflection now wait for your rival's
  check, and Funky Breath waits for your block to fail.
- Fixed: "destroyed by a rival effect" paid out for a foundation you destroyed
  yourself. Bright-Eyed Dreams, Marco's Potential, Binding Mr. Aizawa, Threat
  Neutralized and Armored Car Hercules, the last of which never fired at all.
- Fixed: Hange Zoe's +2 speed for committing a backup was never applied.
- Fixed: Titan Swarm was 3 cheaper on every copy, not only the second try.
- Fixed: Sky Dominance cleared whatever attack it found. It now waits for your
  next high attack to deal damage and offers the clear.
- Fixed: Mystic Recovery did not return the 3 cards it prints.
- Fixed: Rule Acquisition #111 never offered to put the card on the bottom of
  your rival's deck, and April's Investigation reordered your own deck rather
  than theirs. Both now show you the cards you looked at.
- Fixed: Clearing the Way was discarded when cleared during your Combat Phase
  instead of being built face down committed.
- Fixed: "X, or Y instead" applied both halves. Scanlan Shorthalt, Terraforming
  Cannon, Scouting Skirmish and Rabbit Finesse each paid the base and the
  replacement together.
- Fixed: Mei Hatsume (II) discarded and drew even when you took the speed bonus.
- Fixed: Best Served Cold recovered the top card of your deck instead of the
  foundation your rival had just committed.
- Fixed: "put the rest back in any order" put them back in the order they came
  off the deck. Willy Tybur's Sacrifice and United Front now let you name it.
- Fixed: face down cards in a stage counted as copies of a named card. Ice Sword
  Execution committed them, and Momo Yaoyorozu (III) refused to build a card the
  stage already held face down.
- Fixed: Wide Awake unsealed itself and sealed itself straight back, so it did
  nothing. It now unseals one of the cards your rival sealed.
- Fixed: "commit 1 of them" offered every rival foundation instead of the ones
  the ability named. Affects Secretary of Defense and Mai Fighting Style, whose
  commit and freeze can no longer land on two different foundations.
- Fixed: Secretary of Defense's second ability could never trigger, because
  committing a rival's foundation raised no event to respond to.
- Fixed: responses to your rival committing foundations, discarding in combat or
  spending momentum were never offered. Affects Brad Boimler, Marshall Law,
  Stun-Baton Thrust, Shock-Baton Jab, Rokuyukai Huddle, Aerial Recon and Pact of
  Wrath.
- Fixed: "due to your effect" and "due to this attack's Stun ability" fired when
  your rival committed foundations to pay their own costs. The cause is now
  checked, so Stun-Baton Thrust and Shock-Baton Jab size their bonus from the
  foundations their own Stun took.
- Fixed: Acrobatic Style responded to your own flips and commits and never to a
  rival foundation committed by your effect.
- Fixed: responses to one of your own foundations being committed by a rival
  effect were offered to your rival instead of you. Affects Battle Aura, Battle
  Plan, Break the Spell, Busy Eating, Counselor of Plants, Dungeoneering Armor,
  Hidden Motives, Holding Out Hope, Seasoned in Hardship, Stealth and Cunning
  and Warden's Protection.
- Fixed: responses to your rival gaining or losing health were offered to your
  rival. Affects Spring into Action, Harness Undeath, Ready to Go and Survival
  of the Fittest.
- Fixed: responses that name your own board fired on your rival's instead.
  Affects Alisa Bosconovitch, Lars Alexandersson, Rebellion, Yggdrasil Rebel
  Leader, Blood Talon, Phoenix Stance, Jaguar Sprint, Nina Williams and
  Outmaneuver.
- Fixed: Survey Mission, Hopelessness, Asuka Kazama and Jaw Titan Attacks!
  answered their event on the wrong side of the board.
- Fixed: Best Served Cold answered your rival committing their own foundations
  rather than yours being committed by their effect.
- Fixed: Own Free Will fired on foundations you destroyed or spent yourself.
- Fixed: building a card opened the response window on both players at once,
  which could stall the End Phase. Affects Anti-Mutant Neutralizer, Fungus Among
  Us, Kindhearted and Nott's Flask.
- Fixed: abilities that answer your rival's Ready Step were offered to the wrong
  player. Affects Chu and Imprisoned.
- Fixed: an instruction printed "after this attack resolves" ran the moment the
  ability was played instead. Colossal Detonation destroyed every foundation in
  both stages at the Blitz Step, Propelled Kick, Inverted Cut and Sniper's Combo
  cleared the attack out of the pool it was still resolving from, Gator Roll
  flipped the attack mid-sequence, Electric Moth readied your character early,
  and Trinket returned itself to your hand early.
- Fixed: those instructions no longer fire at all when the attack is dropped.
- Fixed: an instruction printed at a phase boundary ran the moment the ability
  was played instead. Extra Rations discarded the 2 cards it had just drawn,
  Cute Host Koto drew its 3 cards a whole Combat Phase early, Rushing Intercept
  was cleared from the card pool before it could build itself out of it, and
  Cage of Hell moved itself to your momentum twice.
- Fixed: Loot Box took back the wrong card. "That card" is the one it built, and
  it was read as the card that triggered the ability, which an Enhance has none
  of, so nothing came back at all.
- Fixed: Happy Chaos never offered the card it looked at. It now shows the top
  card of your deck once the attack deals damage, and offers your hand, your
  momentum or neither.
- Fixed: seven cards printed "you may" over an action the game took for you
  anyway. This Is My Chance!! cleared the attack the rest of the card was
  buffing, Armin Arlert, Power of the Colossus discarded from your hand for its
  draw, and Electric Shock flipped your attack over. Each now asks, in the
  card's own words.
- Fixed: twelve cards lost the ceiling printed on their own count. "(max. 5)"
  was cut off with the sentence, so Breach the Perimeter scaled with your whole
  momentum pile, Hitch Dreyse and Battle Aura Release with your whole stage, and
  Pizza Party with everything in play. Revelatory Speech and Storm Bringer
  healed 1 instead of up to 4.
- Fixed: This is Freedom paid nothing. Its X counted the foundations it had just
  committed, and the count was refused before it was read.
- Fixed: Suzuki Flurry's cap now comes from the card rather than the engine, so
  the exemption for a Suzuki character still lifts it.
- Fixed: seven cards printed "for each" and acted once whatever the board held.
  Armored Titan, Finale gave +1 damage rather than one per card type in your
  stage; Rebuilt Forces took 1 off your rival's check rather than one per backup;
  Mt. Lady (III) and Mechanical Legion scaled with nothing.
- Fixed: Heartbeat Surround and Spirit Charged Kick count a property of an attack
  that has not been played yet, so the bonus now waits for the attack and is
  worked out when it arrives.
- Fixed: Upward Rai-Kou Ken clears one card per momentum spent on Powerful, up to
  three, rather than exactly one.
- Fixed: three cards that buy an ability by committing Power tokens committed
  themselves instead. Brutal Bite, Corona Beam and Defiant Roar now spend the
  tokens, and Brutal Bite and Corona Beam pay out per token spent rather than
  once.
- Fixed: a committed Power token stayed committed for the rest of the game. It
  readies with the rest of your cards.
- Fixed: Mollymauk Tealeaf, Carnival Hooligan sealed 1 rival foundation however
  many cards it revealed.
- Fixed: "each player commits 1 foundation" turned your own foundation face down
  instead of committing it, on four cards. A face down foundation loses its
  abilities and symbols; a committed one readies again next turn.
- Fixed: "for every N" paid once per card instead of once per group of N, on
  four cards.
- Fixed: three cards that commit rival foundations for each attack in your card
  pool committed exactly 1, whatever the pool held. King, The Beautiful Kick's
  Illusion, Nejire Flood and Over the Shoulder Reverse.
- Fixed: Covert Black-Ops Arms landed its bonus on the attack in flight, for any
  attack. It now waits for your next Ally or Weapon attack and counts your
  rival's foundations.
- Fixed: Toru Hagakure (II) gave its rival's block modifier the flat +1 and not
  the extra +1 per 4 foundations.
- Fixed: attacks in your card pool, Kick and Punch cards in it, and cards in
  your discard pile were counted as none.
- Fixed: "non-Throw attack" applied to Throw attacks as well on six cards. Armin
  Arlert, Power of the Colossus; Lady Kima of Vord; Endlessly Doting; "An
  Embarrassment of Dooplers"; Kick Start My Heart; and Levi Ackerman, Humanity's
  Strongest Soldier.
- Fixed: an attack granted Throw now counts as a Throw for those cards.
- Fixed: Lady Kima of Vord read the size of your card pool instead of half the
  preceding attack's printed difficulty.
- Fixed: Yasha Nydoorin, Orphanmaker paid +0 damage whatever its Rage counters
  said.
- Fixed: "your non-Tech, non-Weapon attack" only checked the second exclusion, so
  a Tech attack took the bonus on Ryu, World Warrior and Baek Yoonho.
- Fixed: the printed "non-Unique" exclusion was dropped on Zeke, Beast Titan;
  The Beast Titan's Rock Barrage; Death Rattle; Momo Yaoyorozu (III); and Jet
  Somersault Kick, so each could reach the one card the card rules out.
- Fixed: "build 1 foundation from your hand" ignored the printed type and
  offered attacks and actions as well, on twenty cards.
- Fixed: a printed type in front of the build was dropped, so Armored All Might,
  Armored Car Hercules, Curious Tea Preparation, Enchanted Weapon Attack, Quest
  Board, Hunter's Ally and Wingnut, Mechanical Genius built any card instead of
  the Armor, Party, Weapon, Ally or Tech card printed.
- Fixed: a build printed "committed" came in ready on Disciplinary Action,
  Threat Neutralized, Own Free Will, Jet Somersault Kick and Shun'ei, Amped-Up
  Illusionist, so the cost was never paid.
- Fixed: Kuwabara, Spirited Warrior built any foundation instead of one sharing
  2 or more symbols with your character.
- Fixed: The Attack Titan Emerges built any card in the discard pile instead of
  one cheaper than the card its cost sacrificed.
- Fixed: Replicator Enthusiast built twice.
- Fixed: 30 abilities that name a ready, committed, face up or face down card
  ignored the word and could take any card in the zone.
- Fixed: Recall from your card pool and recall from a stage to hand never
  received their printed restriction at all.
- Fixed: Cancel offers that charge a face up sacrifice let the rival pay with a
  face down foundation, and counted prices they could not pay.
- Fixed: "1 ready face up foundation" kept only the first of the two words.
- Fixed: Two spellings of face down, so No-Mercy Percy let the rival sacrifice
  a face up foundation.
- Fixed: 9 abilities that ready, commit, seal or search for a card of a named
  difficulty ignored the number and could take any card in the zone.
- Fixed: 6 abilities printed for an attack or card of a named difficulty
  applied to every attack, including Strong Windup and Hange Zoe.
- Fixed: Beast Summoning could ready a foundation it had already readied that
  Combat Phase.
- Fixed: Desperate Sabotage added every milled card to hand instead of only
  the backups.
- Fixed: 5 abilities printed for an attack of a named speed or printed damage
  applied to every attack, including Chase Down, Dual Handguns and Exploit
  Weakness.
- Fixed: Creative Counter and Blueflame Surge ignored the keyword their trigger
  asks for and fired on any block.
- Fixed: Where All Paths Converge never asked for a keyword and added every
  milled card to hand.
- Fixed: Time for Rest named no keyword and its -2 speed reached no attack.
- Fixed: Horseback Charge, Sen-Siss Hou and Lars Alexandersson promised to build
  the next foundation you play and built nothing when its check failed.
- Fixed: Rebellion never changed the zone of the next attack.
- Fixed: Aerial Kikosho never replayed itself from your card pool, and its -2
  difficulty was not applied to the check that play makes.
- Fixed: prompts aimed at a card pool highlighted no cards, so there was nothing
  to click.
- Fixed: an attack played from outside your hand was turned face down afterwards
  as though it had Echo.
- Fixed: Mischievous Doodler, "I Would Like to Rage!", Hates Lectures, Kamuriyuki
  and Frightening Calm granted their keyword without its rating, which is the
  same as granting nothing.
- Fixed: Thoughtful Classmate, Shortcake Admirer and Big Fist Bash offered your
  whole card pool instead of the middle or high attack they name.
- Fixed: Weapon at the Ready, Sasha Blouse, Revive Ally, Nejire Hado (II),
  Mutant Mash-Up and Gifts from Splinter offered your whole discard pile
  instead of the card type and difficulty they name.
- Fixed: Arrogant Smirk recalled any card from your card pool rather than a
  Fury attack.
- Fixed: Demon Plants let any card in your card pool skip progressive
  difficulty rather than an Ally attack.
- Fixed: Anti-Titan Artillery took stamina off any backup rather than a Titan
  one.
- Fixed: 80% Power built your rival's cards ready instead of committed, and
  Audio Reverberation let them give up any foundation rather than the committed
  or ready one it names.
- Fixed: Godzilla, Titan of Terror, Oxygen Destroyer and Sung Jinwoo armed a
  flashback with no restriction at all, so the top of your discard pile was
  playable whatever it was.
- Fixed: twelve attacks that buff themselves were played at their printed
  numbers whatever the board said. Timely Counterattack, War Hammer Titan's
  Bolt, Hange's Thunder Spear Strike, Combination Blast, Demonic Catastrophe,
  Desperate Slash and six more now pay what they print.
- Fixed: thirty-two conditions that count a card type in a zone could never be
  true, so the cards read as gated and played with the sentence deleted. Brave
  Volunteers, Izuku Midoriya, Deku, Raphael's Sai, Let's Stay Out and Caduceus
  Clay are among them.
- Fixed: Sleepyhead gave its first +1 damage even after your rival had lost
  health.
- Fixed: Suggestive Spell drew a card off any attack in your rival's discard
  pile rather than ten.
- Fixed: Treasure Hunting made you discard even with your rival's discard pile
  fifteen deep.
- Fixed: Mighty Blitz asked for a high or middle attack in your card pool and
  counted neither.
- Fixed: Brad Boimler, Acting Captain committed a foundation from each player
  with no attacks in either card pool.
- Fixed: Behemoth Typhoon took two of your rival's foundations for any check,
  not one you paid three cards to pass.
- Fixed: Tuning In gave +3 damage without six keywords in your card pool.
- Fixed: Aizen Festival Swing made you discard while you held a Heat token.
- Fixed: Scaling Heights gave +1 damage to attacks of any printed speed.
- Fixed: Chorus of a Thousand Skulls gave +2 to the check on the first copy.
- Fixed: Partners in Crime looked at the top of your deck after any attack, not
  one sharing two symbols with your character.
- Fixed: a keyword grant printed at the tail of a longer sentence granted
  nothing. Draw Your Swords, Nott the Brave, Mollymauk Tealeaf, Titanstone
  Knuckles, Itsuka Kendo, Big Fist Fury, Net Launcher, Sword of the Darkness
  Flame and Deleterious Bomb all print a rated Stun they never gave.
- Fixed: Benimaru and D'Vana Tendi each print a choice between two effects and
  always took the first. Both arms are now offered.
- Fixed: Besiege could be blocked by any card, ignoring its printed block
  modifier of 3 or greater.
- Fixed: Grenadier Blast and Bui destroyed themselves instead of the ready
  foundation the player chooses.
- Fixed: Night on the Town accepted a backup of any difficulty for a price that
  names 3 or less.
- Fixed: Net Launcher committed one card instead of three face up foundations
  that do not share a name.
- Fixed: Xilien Invasion and Xilien Agent asked for nothing. Each prints
  removing a second copy of itself, from your hand or from your stage, on top
  of removing the card you play, and that second copy was never asked for.
- Fixed: a price that names a card could be paid with the card printing it.
  Demonic Catastrophe removed itself for a price that names another copy.
- Fixed: a face down foundation could pay a price that names a card. Face down
  it prints no name to match.
- Fixed: Heat Tackle and Stop and Dash never sealed themselves. Sealing the card
  is what each one charges for answering, so both could answer again and again
  for nothing.
- Fixed: Antidepressant Scale changed the zone of its attack without sealing one
  of your face up foundations, which is the price it prints.
- Fixed: Military Airship committed but never froze itself, so it readied at the
  start of your next turn and could be used again a turn early, every turn.
- Fixed: Stun-Baton Thrust's blitz never readied a rival foundation. Neither
  player saw anything happen, and you were never asked which one to ready.
- Fixed: Heaven-Piercing Ice Wall's enhance drew you a card for free. It is
  paid for by readying one of your rival's foundations, which never happened.
- Fixed: Consuming Their Own's enhance gave its attack +4 damage without any
  backup losing the 2 stamina it charges. You now choose which backup pays.
- Fixed: Lady Nagant cancelled a rival enhance for a commit alone. The response
  also charges the top card of your deck, which stayed on your deck instead of
  going to your card pool.
- Fixed: Strategic Meeting never turned over the top card of your deck, and
  offered to put itself into your momentum rather than the card it revealed.
  Adding the revealed card to your hand, which needs 3 or more keywords on it,
  could not be taken on any board.
- Fixed: Nejire Hado (II) took a Ranged attack back out of your discard pile for
  free. It charges 3 off your maximum health for the rest of the game, and that
  is now taken.
- Fixed: Reiner Braun, Warrior and King Ghidorah, Emperor of the Cosmos both
  print a way to survive losing the game and return to maximum health. Neither
  worked, and reaching that point ended the game instead.
- Fixed: the seven cards that take a keyword off an attack recorded the loss and
  then went on treating the attack as though it still had it. Fortitude of the
  Armored Titan, Last-Second Dodge, Raise Walls, Overdrive Uppercut, Wild Wild
  Pussycats, Double Fists of the Mortal Flame and A Son's Love now all take what
  they print.
- Fixed: a keyword given to an attack after that attack had lost its keywords was
  thrown away instead of being handed back.
- Fixed: Deflect never worked at all. Adding the card to your card pool is the
  price of playing it, and that price could not be paid, so no card printing
  Deflect could play it and the damage it takes off a rival attack never came
  off.
- Fixed: an ability printed as [Hand] could only be played off an Action card.
  Spirit Lollipop, Aerial Kikosho and Cyborg Slap each print one and none of
  them is an Action, so theirs could never be played, and every card printing
  Deflect was held back by the same rule on top of its price.
- Fixed: Beauregard Lionett, Expositor and Not Now, I'm Gaming paid their prices
  on your screen and not on your rival's. The attack Beauregard discards stayed
  in your hand over there, and neither the commit nor the flip Not Now, I'm
  Gaming pays showed up at all.
- Fixed: an ability printed as [Card Pool] could only be played off the attack
  you were in the middle of. Potato, Gear Shift, Scanlan's Hand, Slow but
  Strong and Faultless Defense each print one on a card that is never an
  attack, so theirs could never be played at all.
- Fixed: a response printed as [Discard Pile] could never be played. Yeagerist
  Takeover, Combined Firepower, Phoenix Stance, Twist Reality and Devil's
  Instincts each print one, and clicking the card where it lay only opened the
  pile to read it.
- Fixed: a form printed as [Discard Pile] or [Card Pool] could never be played.
  Short Work, Demonic Catastrophe, Predator Bardiche, Channel Chaos and Oxygen
  Destroyer each print one, and a form was only ever offered on a card in your
  stage or on your character.
- Fixed: a card that lets you play an attack out of your discard pile offered
  the whole pile, and then took the card at the bottom of it whatever you
  clicked. Oxygen Destroyer names the attack it was played off, Godzilla, Titan
  of Terror a printed difficulty, Shadow Monarch Skill Tree a Shadow Shift
  attack, Fjord, the Sea's Champion a card by name, and Elder Toguro any attack
  in the pile. None of them could be taken up at all, because clicking a card
  in the pile only opened it to read.
- Fixed: Sword Toss and Hiding Out counted toward progressive difficulty. Both
  print that they do not, as the last thing their sentence says, and only the
  speed and the damage they print alongside it were being applied.
- Fixed: Ibara Shiozaki's second ability exempts your next middle attack from
  progressive difficulty, and a middle attack was never recognised as one, so
  the exemption sat there and could never be spent.
- Fixed: a card that raises one type of your attacks raised nothing. Zeke,
  Beast Titan gives your Ranged attacks +2 speed and +2 damage, The Prowess of
  the Survey Corps gives your Weapon attacks +1 speed, and Harlowe, The
  Gravitar, Sam Rutherford, Devron Racer, Spire of Conflux, Recipro Turbo and
  Chain Punch: Sheath each name another type. No attack was ever recognised as
  the type printed, so all of them paid out nothing.
- Fixed: the same kind of card written against a printed difficulty rather than
  a type paid nothing either. Godzilla, King of the Monsters, Anguirus, Fierce
  Dragon and Repay a Debt raise your attacks with printed difficulty 5 or
  greater, and Sword Skills raises those with printed difficulty 3 or less.
- Fixed: Faith's Shield gave its damage to neither of the two attack types it
  names, and Rokuyukai Huddle added nothing to your hand from the cards it
  milled.
- Fixed: Vex'ahlia, Resourceful Hunter exempts your next Ranged Weapon attack
  from progressive difficulty, and only the damage printed alongside it was
  ever given. An attack named by two printed types now has to be both of them,
  not either one.
- Fixed: a price that names which card it takes would take any card in your
  stage. A cost printed as flipping a foundation could be paid by picking one
  that was already face down, turning nothing over, and a price for two cards
  could be paid with the same card twice. 135 cards print a price of this
  kind, among them Reiner Braun, Warrior and Colossal Confrontation.
- Fixed: a price asking for an asset could not be paid at all. An asset is
  neither a foundation nor a backup, and those were the only cards the board
  would let you pick.
- Fixed: Falling Heel Strike's enhance was free. It prints a price of unflipping
  one of your foundations, which was never read, so the +2 speed was given away
  and could be taken with nothing face down in your stage to turn over.
- Fixed: a foundation you had already committed could not pay a price that flips
  a foundation. Which way up a card is and whether it has been spent are
  separate things, and the same price printed on the card itself never asked, so
  the board offered the ability and then the click did nothing. 29 abilities
  choose a card for a price of this kind.
- Fixed: counters spent from a card came off your board only. Counters are put
  on by an ability, which both players replay, but paying one away is a price,
  which travels a different way and had no handler, so your rival went on seeing
  a card carrying counters it had already spent. Affects Charged counters on
  Cabal's Ruin and Devil Gene counters on Kazuya Mishima.
- Fixed: spending a Power token left it sitting in your token pile. The token
  pays for its own +2 damage by being sacrificed, and a sacrifice moved the card
  to the discard pile without taking it out of the pile it was in, so one token
  went on paying that price for the rest of the game. Your rival's tokens
  behaved the same way on your screen.
- Fixed: spending a Roman Cancel token left it in the pile on your rival's
  screen and took a card out of your hand there instead. All four of its
  colours are paid for by removing the token, and the token pile was the one
  zone the other player's copy of the board never looked in.
- Fixed: an ability played from your card pool that pays by flipping the card
  face down left it face up on your rival's screen, so their board still
  offered a card that had already been spent. Seven cards print this price,
  among them Response [Card Pool] Flip abilities.
- Fixed: an attack or block of yours that your rival sealed stayed sealed on
  your screen after the attack resolved, so you went without that card's
  abilities for the rest of the turn while your rival's board had already given
  them back.
- Fixed: paying a keyword's cost with something other than momentum changed
  your own board and nothing else. Scrap Cannon's asset, the counters spent by
  Grog's Rage and Commander's Rage, the Spell flipped by Spellstorm and Second
  Wielder sacrificing itself all stayed exactly where they were on your rival's
  screen, so the price looked unpaid there and their board went on offering
  cards you had already spent.
- Fixed: Robert and Dragon of the Darkness Flame pay a Powerful cost with two
  or three cards from your hand, and the attack's bonus counts every card paid
  with. Your rival's screen counted one card however many you spent, so the
  attack did a different amount of damage on each of the two boards.

- Fixed: a card lying face down in a stage is a blank foundation, so it is
  neither a backup nor an asset. It was still treated as whatever it is printed
  as: a face down backup could be attacked as a backup, committed as one though
  a foundation, counted toward abilities that ask how many backups you have,
  and spent to pay a price that names one. A face down asset paid a price
  naming an asset the same way.
- Fixed: a backup lying face down in a stage still showed its green stamina
  heart, so its number could be read off a card whose face neither player was
  meant to see.
- Fixed: "ready 1 foundation" would not ready a face down card. A stage grows
  face down, so the cards most likely to be committed were the ones these
  abilities refused, and a card that names a face down foundation outright only
  worked when the hidden side happened to print Foundation.
- Fixed: sacrificing a foundation passed over every face down one, so an ability
  asking for one could find nothing to take, or take a card without letting you
  choose. A face down card has no printed difficulty, so it can no longer be
  given up for a price that names a number.
- Fixed: the count of foundations committed to play an attack left out the face
  down ones, and your rival's screen counted them a different way again, so the
  two of you could see the same attack at different speeds.
- Fixed: a card lying face down in a card pool was still counted as a foundation
  there. It is a blank card.
- Fixed: a card lying face down in your card pool could be spent to pay a price
  that names a type, such as "remove 1 Fury attack from your card pool". A face
  down card there prints no type at all. Prices that name a face down card, or
  simply a card, still reach it as before.
- Fixed: the same card could be picked by abilities that name a type in the card
  pool, could be copied by an attack that takes the printed speed and damage of
  another attack there, and could give your attack a type it does not print.
- Fixed: a card that cannot be played while a named card sits in your card pool
  was reading that name off face down cards, which print none.
- Fixed: a face down card in your rival's stage could be destroyed by an
  ability that names a card type or a difficulty, and was spared by one that
  passes over unique cards. A face down card in a stage is a blank
  foundation, so it prints none of those. An ability that simply destroys a
  foundation still reaches it.
- Fixed: clearing from your card pool read the hidden face of your face down
  cards. One could be cleared as an AIR card, as a kick card or as another
  attack, and was passed over by a clear that asks for a non-attack. A face
  down card there is a blank card, so it is a non-attack and nothing else.
  Clears that name a card, or a face down card, still reach it.
- Fixed: readying, committing or sealing a foundation of a named difficulty
  read the hidden face of a face down one. Absorbing Pollution, Switch to
  Vertical Maneuvering!, Keyleth of Air Ashari and Beast Summoning could ready
  one of yours, and Sand Blast, Utgard Castle Stands and Killing Intent could
  reach across at one of your rival's. A face down foundation prints no
  difficulty, so none of these reach it. A price that names no number, like
  "ready 1 foundation", still does.
- Fixed: counting cards of a named type or symbol in a stage or card pool read
  the hidden front of a face down card. Brave Volunteers, A Trinket for Vex,
  Izuku Midoriya, Let's Stay Out, Caduceus Clay, A Day for Relaxing, Fenthras,
  Defensive Preparations, Strategy Meeting and Brad Boimler each counted one as
  whatever it turned out to be on the other side. A face down card prints no
  type and no symbol, so none of them count it. A face down card in a stage is
  still a foundation, and anything counting foundations there still counts it.

- Fixed: gates that pair two card types, and everything that counts by NAME,
  read the hidden front of a face down card in a stage or card pool. Skirmish
  Line and Hunter's Arrow counted one as an asset or a backup, Ancestral Curse
  read a printed difficulty off it, Evoking the Wielders and All Might's
  Armored Punch counted it as a differently named card, Zero Gravity Shot as a
  high attack, "An Embarrassment of Dooplers" as a Doopler, Sung Jinwoo, E Rank
  Hunter as a Shadow card, and Kuro Momotaro, May, Zero Satellites and Spirit
  Uppercut each matched it against a name. A face down card shows no name to be
  matched and no type to be paired, so none of them count it now.

- Fixed: picking one card out of a zone by where it lies, and then asking it a
  printed question anyway. Mikasa's Unrelenting Assault and Lady Kima of Vord
  read the speed and the difficulty of "the preceding attack" off a face down
  card, King treated one as the Throw attack it follows, Wielding One For All
  counted blank foundations as differently named Vestiges, an attached
  character was recognised by name through the back of a card, and a card lying
  face down in the pool still excused itself from progressive difficulty. The
  preceding ATTACK is now the nearest one that is showing, and the preceding
  CARD is still whatever lies in that slot, which face down is no Throw.

- Fixed: a card built face down still handed out the rules it prints. Jarett
  Howarth made your character a Warrior, Little Mister milled an extra card,
  Demon's Shaft took 1 off your rival's checks to play non-attack cards, and
  "I Would Like to Rage!" excused its own first copy from progressive
  difficulty, all while lying face down with nothing printed showing.
- Fixed: Jack-8's face down foundations could be frozen and destroyed by your
  rival. The rule is printed on the character, and only the stage was searched
  for it.

- Fixed: a card lying face down still answered response windows. The game
  stopped to offer a window for a blank foundation's printed response, and
  waited on a face down card as though your rival were holding a cancel.
- Fixed: an Outwit ability was offered off a card that had been turned face
  up. Outwit is played only while the card is face down, which is also why a
  face down card still answers with one.
- Fixed: an offer you had no way of paying for was still put to you, and
  taking it handed over the reward for nothing. Reiner Braun got its bigger
  damage swing with no foundation in your stage to sacrifice, Toothy Bite took
  2 health off your rival on an empty momentum bar, and Drawing Power drew the
  extra cards without the Power tokens it charges.
- Fixed: a price you could only part pay was taken anyway. Dolores, Hidden
  Wisdom asks for 3 foundations, and with one in your stage she took that one
  and readied herself regardless. A price is paid in full or the offer is not
  made at all, and on the cards that print an "Otherwise" that branch now runs
  instead.
- Fixed: an offer that came up while another prompt was already on screen
  answered yes in your name and paid the price for you. It declines now.
- Fixed: an "If" printed in front of a "you may" was read as a condition on the
  price alone, so the offer came up even when the card said it should not, and
  the reward it buys arrived either way. Strategic Maneuver built an asset of
  any difficulty without discarding for it, and Porco Galliard and Zeke Yeager
  offered a transformation that had not been earned.
- Fixed: Strategic Maneuver's "Otherwise" was gated on the same difficulty it
  is the alternative to, so turning down the discard left you with neither the
  built card nor the chosen card in your hand.
- Fixed: Godzilla, Shin Godzilla's Enhance made your rival sacrifice a
  foundation whether or not the attack dealt damage, and asked you to commit
  the card before anyone could know whether it had. The offer now waits for
  the damage it is printed behind, and the sacrifice only follows if you take
  it.
- Fixed: six cards printing "seal it" sealed themselves rather than the card
  they name. Porco Galliard sealed your own character when your rival played a
  block, Filled with Doubt, Nonagon, Allura Vysoren and Spirit Detective sealed
  themselves instead of the attack they answer, and Xango sealed itself instead
  of the card each player had just added to their card pool. White Angel of
  Death prints "seal this card" and is the one that really did mean itself.
- Fixed: Pristine Swordplay and One For All: Full Cowling 8% Falling Roundhouse
  could ready a foundation they had already readied this Combat Phase. Both
  print that they only reach a card that has not been readied yet, and the
  other twenty-seven cards printing the same restriction were keeping to it.
- Fixed: Call of the Reaper readied every foundation in your stage that had
  not been readied yet. It gives back the cards you committed to pass the
  check to play the attack, and nothing else.
- Fixed: Breakin', A Holo Escape, Alone Infection, Recipro Turbo, Monsters of
  the Deep and Rapid Speed Slash each did both halves of a choice they print as
  one or the other. You are now asked which one you want.
- Fixed: Tornado Fist never offered the choice it prints. It always added the
  top card of your deck to your momentum, and discarding it from your card pool
  was not on the table at all.
- Fixed: Queen of the Monsters only drew you a card. It also adds a foundation
  from your discard pile back to your card pool, which is the larger half of
  what it prints.
- Fixed: Strategic Maneuver, Secluded Training Ground, Gifts from Splinter and
  Collecting Scraps offered you nothing. Each asks for an asset in your discard
  pile, and an asset was being looked for in the wrong place on the card, so no
  card ever answered.
- Fixed: five cards printed two instructions joined by "and" and only carried
  out one of them. Swift Execution drew a card without banking itself, Holding
  Out Hope never readied your foundation, Driven by Retribution left your
  rival's stage alone, Resurrected Titans revealed two cards and discarded
  neither, and Doty the Automaton could ready itself when it prints "other".
- Fixed: three cards printed a choice of where a card goes and never offered
  it. Godzilla vs Gigan always came back to your hand when it also offers the
  top of your deck, I'm Old, Yusuke put the card in your hand rather than the
  momentum or deck top it names, and Dagger, Dagger, Dagger could not reach a
  card sitting in your momentum at all.
- Fixed: a card asked for by name searched the whole zone instead. Bellow of
  Rage offered any card in your discard pile rather than the ones with "Rage"
  in their name.
- Fixed: Tri Gravity Beam destroyed one of your own foundations to pay for a
  look at your rival's hand, and then left the hand alone. It prints a card
  removed from it, and now takes one.
- Fixed: every attack that destroys a rival asset or backup destroyed nothing
  at all. Armor Rush, Collateral Damage, Upward Disarming Swing, Luna Ring,
  Massive Optimal Punch, Titanstone Knuckles, Jaw-Some Solution, Nape Strike,
  Devastating Loss and To the Grave each name the type they take, and the card
  they were allowed to take had to be a foundation at the same moment, which no
  asset or backup ever is.
- Fixed: To the Grave may only destroy a backup with 4 or less stamina. The cap
  it prints was not read, so it reached any backup in the stage.
- Fixed: Destoroyah, Perfect Lifeform destroys 2 rival non-character cards, and
  could only reach their foundations.
- Fixed: Unyielding Heat and Heartbeat Surround did nothing at all while they
  sat in your card pool. Each prints what it does in front of the moment it
  happens, and only the other word order was being read, so neither one ever
  had a moment to happen in.
- Fixed: Besiege and Hedrium Ray turned away the only blockers they allow.
  Both say they can only be blocked by a card with a printed block modifier of
  3 or greater, and they refused exactly those cards while letting every
  smaller block through.
- Fixed: Nullifying Force did not hold the damage it freezes. It says an
  attack's damage cannot be modified, and it only stopped the number being
  reduced, so any bonus still raised it.
- Fixed: Floch Forster, Yeagerist Leader never doubled anything. The card
  prints a choice between doubling an attack's damage and reducing it to 0, and
  both halves were being carried out in that order, so the doubling was always
  thrown away and the attack landed at 0 either way. You are now asked which
  one you want.
- Fixed: an enhance that names which attack it buffs could be played on any
  attack at all. Titan Training reads "Your Fury or Titan attack gets +2
  damage" and paid out on a Kick attack just as happily, and forty abilities
  named a type this way without ever checking it, Solo Pro's Ferocity and Right
  Flamingo among them. The same sentence written "This Fury or Titan attack"
  was already checked.
- Fixed: a damage bonus that names two attack types was paid twice. The Beast
  Titan reads "This Ranged or Titan attack gets +2 damage" and handed out +4,
  and Breaking Step added a flat +1 on top of the +1 for each attack in your
  card pool it prints. Faith's Shield, which reads the same way with a minus,
  now takes the 2 it prints off in one place.
- Fixed: The Roar of the Spark always stunned the attack. It prints a choice,
  "This attack gains Stun: 1 or gets -2 speed", and the second half was never
  offered. The same choice printed the other way round was already a choice.
- Fixed: Mark Tyner's response reads "that check gets +2 or -2" as one
  choice again. Both halves were being applied, so choosing the penalty left
  the check where it started and choosing the bonus paid double.
- Fixed: Mitchell Cimino moves a keyword rating as well as speed. The card
  prints "+1 or -2 speed and +1 or -1 to one of its keyword ratings" and only
  the speed half was applied, so a committed foundation bought half of it.
- Fixed: Cute Baby #202 raises every keyword rating the attack carries. It
  moved Powerful and Stun alone, so an attack rated in Breaker or EX gained
  nothing while two ratings it does not have moved instead.
- Fixed: Chivalrous Charge handed you the card it prints for your rival. It
  reads "if your rival has no cards in their hand, they draw 1 card", which is
  what the attack pays for its +3 damage, and you were drawing it instead while
  their hand stayed empty.
- Fixed: Elegant Palace handed its +1 speed and +1 damage to both players. The
  arena rewards whoever crossed 6 damage this turn, and their rival's next
  attack was picking up the same bonus.
- Fixed: Botan's Coaching left your rival out. It reads "both players discard 1
  card and draw 1 card", and only you were discarding and drawing.
- Fixed: Sakyo's Gamble could never pay the second +3 damage it prints. Only
  you milled, so the card compared one milled card against nothing, and the
  types it asks about can only differ once both players have milled.
- Fixed: Hostile Introduction took a health off your rival the moment it was
  played. It only prints that loss for when the card reaches your discard pile,
  which is the moment the ten other cards printing the same sentence wait for.
- Fixed: Bagpipe Cacophony turned no cards over. Revealing the top 3 cards of
  your deck is the price of its Blitz, and it was never charged, so the card it
  then asks you to put back on top had nothing to choose from. Your rival also
  sees all three cards now rather than one.
- Fixed: attacks that print a keyword behind Deadlock, like Support from Female
  Titan's "Deadlock Stun: 2", worked on any board. Deadlock is a play
  restriction, so those keywords only do anything while your rival has 11 or
  more foundations in their stage. 26 cards print one.
- Fixed: abilities printed behind a character trait or a character name, like a
  "Thief Enhance" or Knife Edge Death-Match's "Chu Enhance", could be played by
  anyone. That word ahead of the timing is a play restriction: only a character
  with that trait, or with that name, may play the ability. 63 abilities print
  one, and Knife Edge Death-Match wins the game outright.
- Fixed: attacks printing a keyword rating behind a restriction, like
  Decapitating Swing's "Brute Powerful: 3" or Swift Execution's "Deadlock EX: 4",
  paid out for any character on any board. Powerful and EX apply the moment the
  attack is played rather than being played themselves, so the restriction ahead
  of them went unread. 11 attacks print one.

- Fixed: Survey Corps Elite and Sword Advantage could be played for nothing in
  every Enhance Step, over and over. Both print a reveal from your hand as the
  moment they answer, the game never announced one, and so they waited for
  nothing at all. Revealing a card out of your hand is now a moment cards can
  answer, and both wait for it.

- Fixed: Standard-Issue Sidearm gave its attack the +2 speed it prints but never
  the Ranged, so the attack could still be blocked by cards that Ranged keeps
  out. Every keyword the game knows can now be handed over by a card that
  prints it.

- Fixed: Violent Animus Shot removed a backup and drew you a card, but the
  attack never gained the Flash it prints, so your rival still got an Enhance
  Step to answer it. The keyword is handed over now, and only when a backup
  was actually removed.

- Fixed: cards printing "up to" a number took the whole number for you. Vertical
  Training cleared both cards out of your card pool, Absorbing Pollution readied
  two foundations whether or not you wanted the second, and Master's Touch froze
  two of your own when freezing is the part you pay for. You now pick how many,
  up to what the card prints.

- Fixed: Hidden Motives and Loop the Loop could answer themselves. Hidden
  Motives readied the very foundation that had just been committed, and Loop the
  Loop handed itself back from your card pool to your hand. Both print "other",
  and both now leave their own card out of the choice.

- Fixed: Ryo's second enhance did nothing at all. It reads "if your Punch
  attack is completely blocked, your rival loses health equal to its printed
  damage", and the damage it counts was never worked out, so it took no
  health. It was also being offered on attacks it does not name, and would
  have paid out whether or not the attack was blocked.

- Fixed: Whirling Slash never took its -3 difficulty off anything. The discount
  is for your next Air attack, and an attack's symbol was the one thing the
  discount could not read, so it waited in place for the rest of the game.

- Fixed: Resurrected Titans discounted only the Shift attacks that list Shift
  among their types. A card printing the keyword in its stat line instead was
  charged the full difficulty.
- Fixed: Dimension Sword never asked which foundation it was about. The
  speed bonus counts the symbols one foundation in your stage shares with
  your character, and with nothing to ask, it counted whatever cards the
  attack had last touched: usually none at all.
- Fixed: a keyword printed partway along a stat line ignored the restriction
  printed in front of it. Swarmed by Titans stunned on any board rather than
  waiting for a deadlock, and Ogre Boulder stunned for a character of any team.
  A keyword spelled out after the first one was not recorded at all, on 29
  attacks.
- Fixed: Tyrant Rave, Deal with the Devil and Devil Jin sat out their own
  response. Each of them answers a check that turns up an attack, and because
  the sentence names no type of attack, the game read the word "an" as the
  type and went looking for a kind of attack no card is.
- Fixed: cards that count Rage, Mushroom and Devil Gene counters could not see
  the counters they were counting. Decapitating Swing, Rip Apart, Unyielding
  Rage and Grog's Rage never reached the Rage counts they print, Kinoko Komori
  and Splitgill Lung Strike never reached their Mushroom count, and Hand of
  Ambition took the 3 health anyway while a Devil Gene counter sat on your
  character. Mishima Bloodline lost its Tenacious the same way. A counter is
  filed under the name printed on the card, and these sentences asked for it
  in lower case, so the two never met.
- Fixed: True 100% Unleashed counted committed foundations as ready ones, and
  Attack Titan's Wide-Swinging Blow counted face down foundations that were
  committed rather than the ready ones it prints.
- Fixed: Spike, Bounty Hunter and Battle Aura Release counted every foundation
  in your stage instead of the face down ones, and Tangled Grasp counted every
  card in your card pool instead of the face down ones.
- Fixed: Connie's Sword Strike, Vax'ildan, Cunning Thief, Frenzied Dash,
  Charged Alien Sploof, You Can't Catch Me! and Robert counted the card
  printing the sentence as one of the other cards in your card pool.
- Fixed: Mr. Dolphin, Great Yamada Attack, Frenzied Dash, Charged Alien Sploof
  and You Can't Catch Me! counted every attack in your card pool rather than the
  Ally, Fury, Tech or Weapon ones they print, and Titanpile counted every backup
  in your stage rather than the Titan ones.
- Fixed: Zeke Yeager, Warchief and Ursine Might counted the cards in a zone and
  then ignored the number printed after the count, so each one paid one less
  than it reads.
- Fixed: Wielding One For All offered twice the choices it prints. A count
  printed as "half the number of ... rounded down" was read in full, because
  the half of the engine that answered it did no arithmetic at all.
- Fixed: Wielding One For All counted only the foundations in your stage while
  it prints "cards", so a Vestige asset standing there was never one of them.
  The card offered fewer choices than it reads.
- Fixed: Thunderous Roar counted your own face down foundations rather than
  your rival's, because it prints the possessive in front of the noun and the
  rival reading only knew the other word order.
- Fixed: Catching a Meteor played the attack it milled, and nothing counted it
  as a play. Smoke-Screened Ambush, Connie's Incapacitating Strike and Lethal
  Slash never saw a card being played, the turn's tallies of attacks and of
  non-action cards skipped it, and the battle log never said it had been
  played. It also read as played from your hand when it had come off your
  discard pile, which is the opposite of what Woman asks.
- Fixed: Concealing Power's stronger half could never apply. It gives your
  rival's next check -2, or -4 if you have played a card from anywhere other
  than your hand, and which one it was got decided on the peer making the
  check, the one board that was never told about those plays. Jean Kirstein,
  Dependable Competitor went wrong the same way, showing your rival a smaller
  damage bonus than the one you were getting while they decided whether to
  block.

- Fixed: Tempest Demon God Fist and Catching a Meteor only ever noticed
  momentum spent to pay a price. Cards that instruct a player to spend
  momentum, Rallied Assault on your own side and Bullet Kick on your rival's,
  moved the cards to the discard pile without any of it counting as spending,
  so the attack that builds itself back after two momentum and the counters
  Catching a Meteor collects never arrived.
- Fixed: The Traveler's Favorite noticed only one of the ways a card comes back.
  Your attack gets +1 damage if a card has been added to your hand from your
  discard pile, and only recalling one said so. Symbolic Shot and Unrelenting
  Advance adding a card they milled, Kyoka Jiro (III) adding the card she
  checked, Combination Salvo and Stockpiled Quirks taking back a card they spent,
  and a search that finds the named card in the discard pile rather than the deck
  all took a card out of that pile and none of them counted.
- Fixed: being made to sacrifice a foundation did not count as sacrificing one.
  When a card such as Destructive Fire says your rival sacrifices a foundation,
  the rival picks it on their own machine, and that was the one path that wrote
  nothing down. Abrupt Loss, Crossing Enemy Lines, Disrupting Plans and The War
  Hammer Titan all read that you had sacrificed nothing straight after you had
  been made to give one up, and abilities that answer your own sacrifices never
  fired. Marco Bott, which names the card instead of counting, went the same way.
  Being made to destroy a foundation went unrecorded too, and is still counted
  apart from sacrificing, which is what the rules print.
- Fixed: a mill your rival called for was not treated as a mill. When a card
  such as Invite Hell says your rival mills, the mill happens on the rival's own
  machine, and that path kept no record of which cards came off, opened none of
  the windows a mill opens, and ignored a card in the stage that reads "if you
  would mill 1 or more cards, mill that many plus 1 instead". Unbreakable Cheer
  and Leonardo were never offered after it. Milling until you hit an attack,
  which Stabbing Dagger and Yeagerist Takeover print, opened no window either.
- Fixed: being ruined was not recorded as sacrificing. Ruin makes the ruined
  player sacrifice face down foundations, but the cards it took were moved out
  of the stage by hand instead, so on the machine of the player who lost them
  nothing had happened. Abrupt Loss and The War Hammer Titan read zero straight
  after their controller had been made to give three foundations up, abilities
  answering "after you sacrifice 1 or more foundations" were never offered, and
  a frozen card ruined out of the stage stayed listed as frozen.
- Fixed: removing a card only counted when it paid for something. Cards removed
  by an ability's effect, out of your discard pile, your card pool or your hand,
  were not recorded as removed, so Kazuya Mishima never reached "if you have
  removed 4 or more cards this turn" and the cards answering "after you remove 1
  or more cards" were never offered. The two reasons are told apart now as well:
  an ability that asks for a removal made to pay a cost no longer fires on one
  that paid for nothing, which the printed text has always distinguished.
- Fixed: five cards that print "from your hand" were reading a different moment.
  Golden Destruction and Grinding Overtime answered a removal out of any zone, so
  clearing your own discard pile paid them. Improving Skills, Item Menu and Timely
  Recovery were watching the discard pile instead: they fired when the card was
  discarded and stayed silent when it was actually removed from your hand, which
  includes removing it to pay a cost.
- Fixed: a card you removed from your rival's zones counted for nothing. Devour
  Your Power, Vanishing Storm, Joining the Fight and Malicious Assault remove a
  card from their discard pile, Driven by Retribution from their card pool, and
  Spireling Fetch and Earwig Pincer off the top of their deck. None of it reached
  Kazuya Mishima's "if you have removed 4 or more cards this turn", and none of it
  offered Inspired Design or No-Mercy Percy, which ask only that you removed a
  card and not who owned it.
- Fixed: an ability printing two moments only ever answered the first. Prelude to
  Destruction and Pizza Delivery say check or mill, and neither answered a mill.
  Attitude Selector says discard or remove and never answered a removal.
  Short-Range Shot says a foundation destroyed or a card discarded and never
  answered a discard. Erwin Smith, 13th Commander of the Survey Corps says a
  sacrifice or your attack dealing damage and took no Wall counter for the
  damage. "Strange Energies" never answered your rival's Enhance ability.
- Fixed: cards that print where they came from, or when, answered every trip
  to the discard pile. Extra Cheese built itself committed off a foundation
  destroyed outside combat and Brotherly Love sped up an attack the same way,
  when both ask for a card from your hand or deck during an attack. Banana,
  Hot gained you health off a card cleared from your card pool, when it asks
  for your hand or your stage. Wolf's Ferocity, I'm With You, Loss of
  Consciousness, Eren's Trial, Hostile Introduction, Cycle of Violence,
  Avoiding Conflict and Unabashed Manner all print "during the Enhance Step"
  and answered a discard in any step.
- Fixed: blocking makes a check, so the cards that answer a check finally
  reach one. Prepared for an Ambush and True 100% Unleashed print "after you
  make a check to block" and had no moment to fire in at all, and the sixteen
  that answer any check, Annie's Gamble among them, were offered only on a
  check to play something.
- Fixed: cards that pay for a check to play something no longer pay for any
  check at all. Deadly Research wanted a backup or a Shift attack, Isla,
  Dreaming Brilliance an Ally, Incoming Smash Kick itself and Mark Tyner
  anything but a foundation, and all four paid out whatever was checked.
  Devil's Instincts, Essek Thelyss and Strong Windup answer a check to play
  a card, and would otherwise have started answering blocks as well. Fourth
  Wielder: Danger Sense now asks that the card being played as a block is
  the card it is printed on.
- Fixed: Insubordination, Fighting for Control and Improvised Riposte paid out
  on any check your rival made. Each prints the kind of card the rival is
  checking to play, and now waits for that check instead of the next one.
- Fixed: SpaceGodzilla, Bio-Quartz Monster made the whole ability, not just the
  -3, wait on your rival checking to play a non-foundation card.
- Fixed: The Power of SpaceGodzilla missed your rival's check when they blocked
  on your turn. Their block makes a check like any other.
- Fixed: a check your rival makes to block no longer counts as a check to play
  a card, so cards that answer the rival's play check stay quiet during a block.
- Fixed: Essek Thelyss, Expert Dunamancer and Mark Tyner answer a check either
  player makes, and were offered only on checks you made yourself. Mark Tyner
  also could not see what your rival was checking to play, so it paid nothing
  on their half of the checks it prints about.
- Fixed: Survival of the Fittest, Harness Undeath and Ready to Go paid out
  whenever your rival GAINED health. They answer your rival losing health, and
  now they wait for it.
- Fixed: Spring into Action never saw your rival gain health when it was their
  own card that healed them.
- Fixed: Serving Shade, Feast, Same Old Field Rations, Moment of Peace,
  Recuperation Time, False Visage and Unyielding Enthusiasm stayed quiet when it
  was your rival's effect that moved your health. Your own health changing is
  your moment, whoever caused it.
- Fixed: Serving Shade, Survival of the Fittest, Harness Undeath and Emergency
  Treatment never answered an attack. Damage is health lost, and combat was
  taking it without telling the cards that wait for it.
- Fixed: Ready to Go asks for health lost to an effect, and the words "due to an
  effect" were being ignored. It stays down now when an attack took the health.
- Fixed: Levi's Overhead Strike, Ferocious Attacker, Sleepyhead, Pepperbox Fire,
  Perceived Weakness, Wine Opener, Syndicate Skills and Sadistic Tormentor read
  "has lost health this turn" as no for a player who had just been hit.
- Fixed: A Son's Love never took anything from your rival. It offers them the
  top card of their deck for your second card, and accepting left their deck
  and their momentum untouched while you drew all the same.
- Fixed: Jaw Titan, Flying Form's EX 2 was not recognised as EX. The rating
  was recorded, but anything that asked whether your attacks had the keyword,
  including effects that raise every keyword rating you have, answered no.
- Fixed: Don't Use That Word let you name eight keywords and only four of them
  could be shut off. Powerful, EX, Breaker and Deflect, the ones most worth
  naming, were not on the list at all, and Ruin is not a keyword.
- Fixed: naming a keyword offered seven of them, so a deck built on Fury,
  Kick, Ally or Spell could not name what it runs. Every keyword a legal card
  prints can be named now, and a long list of options scrolls instead of
  pushing the buttons off the screen.
- Fixed: an attack that prints a minimum could be driven under it. Good and
  Evil reads "-1 speed and -1 damage, to a minimum of 1 damage", but only the
  bracketed form of a minimum was understood, so a 1 damage attack went to 0.

- Fixed: a card that searches for something with two printed requirements now
  asks for both. "1 Titan backup card with printed difficulty 4" would take a
  Titan backup of any difficulty, and "1 backup or Shift attack with printed
  difficulty 7 or less" would take any card at all inside that difficulty.
- Fixed: "Ready 1 card with a Mushroom counter on it" now readies only a card
  the ability marked. It readied any committed foundation, so the enhance spent
  marking two of them bought nothing.
- Fixed: a keyword an ability grants is no longer refused by the restriction
  printed against the card's own copy of that keyword. Elemental Orb's
  Electricity mode gave Swarmed by Titans Stun: 1 and it still waited for a
  deadlock, and a block that Tsuyu Asui granted Breaker got nothing if it
  printed a Breaker of its own behind a character you were not playing.
- Fixed: a Breaker granted to your block is now worth what the grant says.
  Brace for Impact prints a Breaker of 2 that only applies at deadlock, so
  blocking with it after Fateful Decision granted Breaker: 1 took 2 off your
  rival's next check instead of 1.
- Fixed: "If you have removed a card this turn" now reads the record of the
  player the card names. The count was kept once for the table rather than
  once per player, so on your rival's screen their card read YOUR removals:
  the same attack could show +2 damage on one board and nothing on the other.
- Fixed: "If this is the second time you played this ability this turn" now
  counts the plays made by the player the card names. The count was kept only
  by the peer doing the playing, so on your screen a rival's second or third
  play committed nothing: their character was committed, sealed, flipped or
  transformed on their board and untouched on yours.


## 0.0.1

- First alpha build.
