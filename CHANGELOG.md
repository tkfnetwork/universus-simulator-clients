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

## 0.0.1

- First alpha build.
