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

## 0.0.1

- First alpha build.
