# Changelog

What changed in each build of the Universus Simulator client, newest first.

The version you are running is written across the bottom of the home screen, in the middle.

## 0.0.2

### 2026-09-26

- Fixed an issue where blocking with Brick Wall froze the End Phase on the blocker's screen. Brick Wall says attacks it blocks cannot be added to momentum this turn, and only the attacking player's game was told so. At the end of the turn the attacker skipped asking about momentum for that attack and discarded it, while the blocker's game was still waiting to be told an answer that was never coming, so the turn never ended for them and the game had to be restarted. It was easy to run into: Brick Wall blocks 3, so anything bigger still deals damage, and only an attack that dealt damage can go to momentum. Both players now work the ban out for themselves from the card on the table, so the turn ends for both of them and the attack goes to the discard pile.
- Fixed an issue where a Jack-8 player could not commit a face down foundation to pass a check by 1. Jack-8 says each of your face down foundations counts as 2 foundations when committing to pass a check, and you cannot normally commit more than you need, so the game refused every click: if all your ready foundations were face down and you were 1 short, the only button left was Fail. The rules make that exact case the exception, since if you only need to add 1 you may commit a card that counts as more than 1. You can now commit it, the Commit button lights up for it, and the press goes through. Committing more than you need is still refused everywhere else, and a Stun still takes a set number of cards whatever they are worth.
- Fixed an issue where a second Deflect could be played against the same attack and do nothing. Only 1 Deflect ability can be played per attack, and the game enforced that by quietly skipping the damage reduction rather than by refusing the play. Playing a Deflect costs you the card, which moves from your hand into your card pool, so a second one took the card, left the damage exactly where it was, and added to the progressive difficulty of everything you played afterwards. Deflect cards such as Unstoppable Force, Battle Priest, Ashido's Acid Dive and Titanstone Knuckles now stop being offered once one has been played against the attack, so you cannot spend a card on nothing.
- Fixed an issue where a card your rival had locked could still be played as a block. Divine Dominance of Annihilation, Farewell Between Friends and Psychic Spirit Glass all stop you playing copies of a card they name, and the game asked that question everywhere a card can be played except when you play one as a block. That was the one place the lock could still matter, since it is set on your rival's turn and blocking is most of what you do on their turn. Playing a block is still playing a card, so a locked card is now refused there too, as are cards printed for a character other than yours and Gravity-Beam Volley while there is a copy of it in your card pool. The refusal also tells you which of those it was, instead of saying you cannot block with that. Blocking with an attack is still allowed on the first turn of the game and while an effect stops you playing attacks, because blocking with an attack is not playing an attack.
- Fixed an issue where some Combo abilities could never be played at all. A Combo asks for the cards played just before it, and six of the things it can ask for were not understood: a block zone, a zone on anything other than an attack, an amount of damage, and a symbol. So Prova=di=Servo wanted a mid block, Facepalm Takedown a high block, Double Grounder Beta a mid Weapon, Cobra Twist a high Throw, Samba a mid Kick, Piercing Barrage a 3 damage attack and Kien Zan a Void attack, and no card could satisfy any of them. All of them can be met now.
- Fixed an issue where a keyword printed next to something else did not count. When a keyword shares its line with a character's name, a second keyword, an errata tag or its own rating, the game read the whole line as one unknown word and saw no keyword at all. Backspin Slash was not a Reversal, Sakura's Hadoken was neither Ranged nor a Reversal, The Haunting of Hitoshi Shinso had no Echo, Ira-Spinta was not a Throw and Ibis Minuet did not print Breaker, so nothing that looks for those keywords, or counts how many a card has, could find them. All 20 such cards now read properly. The character's name on those lines is also a play restriction now, so Christie's Fruit Picker needs Christie, the same as any card printed for one character.
- Fixed an issue where a Combo ability could be played with nothing in front of it. A Combo only works if the cards played just before it in your card pool match what the Combo asks for, and the game only recognised one of the four ways that requirement is printed. On 66 cards, including The Scourge, Turbo Charge, Precise Blow, Tama Yose, Fruit Picker and Alshain Najm, the requirement was read as if there were none, so the ability was offered off an empty card pool. All four spellings are now read, so the Combo asks for what it prints.
- Fixed an issue where any character could play a card printed for one named character. 154 cards carry a name before their type, such as Shinku Hadoken and Ryu's Ashura Senku for Ryu, Double Typhoon for T. Hawk, Soryuju for Maxi and Team Japan for Benimaru, Goro or Kyo, and none of them checked who your character was. They are now refused unless your character has that name, including when your character transforms into it, and a card still in your deck or hand is unaffected, so nothing you have already built is now illegal.
- Fixed an issue where Sixth Wielder: Smokescreen chose the card for you. Its Enhance adds a card from your hand to your card pool face down, and the game took whichever card you had drawn most recently. You are now asked which one.
- Fixed an issue where Tomura Shigaraki, All For One's Successor demanded two cards for an Enhance that says "up to 2". With one card in hand the ability was refused outright, and with two it took both without asking. You are now asked how many to remove, none included, and then which, and the card draw and the card you may try to play both follow the number you actually removed.
- Fixed an issue where the game chose which card left your hand to pay a price. King Ghidorah, Emperor of the Cosmos, Focused Gravity Beam, Rupture Driver, King Ghidorah, Three-Headed Monster and Tomura Shigaraki, All For One's Successor all remove cards from your hand to enhance, and your most recently drawn cards were taken without asking. You are now asked which card, one at a time, and only cards the price names can be picked. It matters most on Tomura Shigaraki, which then offers to let you play a card removed this way.
- Fixed an issue where Micro-Oxygen Beam's Blitz could never be played. It says to remove up to 2 counters from your character, and the price was read as a demand for exactly 2 counters of a kind that does not exist, so the ability was refused however many counters you had. You can now play it with two counters, with one, or with none, and you choose how many to remove, which is what the attack's +2 damage for each counter removed then scales off.

- Fixed an issue where cards that remove counters and then count them counted nothing. Cabal's Ruin gets +2 damage for each counter removed this way and mills both players 10 if you removed 5 or more, Micro-Oxygen Beam gets +2 damage for each counter removed from your character, and Fortify Walls gets -1 speed for each Wall counter it removes. All three took the counters off and then read a total that had already been cleared, so you paid the price and got no bonus at all. The counters are now counted however they were removed, whether as the price of the ability or as part of what it does.

- Fixed an issue where revealing from an empty deck or an empty hand acted on the last cards you revealed rather than on nothing. Cards that say to reveal and then do something with what was revealed, such as Size Advantage, Unit Commander, Offensive to Retake Wall Maria and Battle Suit HUD, kept a record of the reveal for the rest of the sentence to read, and a reveal that turned over no cards left the previous reveal in that record. So an empty deck could hand you a card from your discard pile that this card never revealed. Heart of the Band was worse: it asks both players whether the revealed card matched the type you named, and only your opponent's side knew nothing had been revealed, so the two could disagree and the game would sit waiting on an answer that never came.

- Fixed an issue where Interdiction's response removed your face down cards and then did nothing with them. It says to remove all face down cards from your card pool and that your rival loses 1 health for each card removed this way, and the count was reading a different record from the one the removal wrote, so you paid the Drive and your rival lost no health at all. If a card had been removed earlier in the game, it counted that one instead, so the response could also take health for cards it never touched. The same record was never cleared between abilities, which is why Tomura Shigaraki, All For One's Successor could offer you a card an earlier attack had removed rather than the card his price just took out of your hand.

- Fixed an issue where three Street Fighter 6 cards answered a check they were never printed for. M. Bison, Writhing Evil, JP, Regal Businessman and Unlimited Psycho Crusher all say "after you mill" a card, and milling is something an effect does, while a check is made to play or block with a card. All three were offered every time a check turned up a matching card, so JP and Unlimited Psycho Crusher could buff an attack off your own difficulty check and M. Bison could take a checked Psycho card into your hand. They now wait for a real mill. Prelude to Destruction and Pizza Delivery, which say "check or mill", still answer both. JP's limit of twice per Enhance Step is also read off the card properly now.
- Fixed an issue where Nothing But a Squawking Crow paid out for the wrong thing. It says that after it is milled during the Enhance Step you may remove it to put a card from your discard pile on top of your deck, and milling means off the top of your deck. It was offered whenever the card reached your discard pile during the Enhance Step, so discarding it out of your hand to pay for something let you use it as well. It now waits for a real mill. The seven cards that say "enters your discard pile" instead are unchanged and still take any way in.
- Fixed an issue where two responses charged you a real price and then did nothing at all. Analytical Observation lets you flip it to flip the card your rival blocked your attack with, and Prelude to Destruction lets you sacrifice it to add an attack you just checked or milled to your hand. Neither could find the card it was talking about: the blocker stayed face up, the attack stayed in your discard pile, and you had already paid the flip or thrown the foundation away. Both now act on the right card, and when a mill turns up more than one attack you pick which one you take.
- Fixed an issue where Hadir took your momentum and did nothing. Hadir waits in your card pool and says that after another attack resolves you may spend 1 momentum to add that attack to the top of its owner's deck. It never found the attack it was supposed to move, so the momentum was gone and the attack stayed exactly where it was. Hadir is an attack itself, and it could not tell another attack from itself either, so it offered to answer its own resolution. The attack now goes to the top of the deck belonging to whoever played it, which is usually your rival's, and Hadir no longer offers to bounce itself.
- Fixed an issue where two cards that ask what came before them in your card pool only ever looked one slot back. Sniper's Combo clears itself away after it resolves if it is preceded by a Ranged attack or face down card, and any card to its left counts for that, but it only paid out when the Ranged attack or face down card happened to be the very last thing you had played. Jaguar Sprint ignores progressive difficulty if the preceding face up card in your pool is a Throw, and it read the slot next door whatever was in it, so a face down card sitting there made it fail outright even with your Throw right behind that. Both now read back along the pool the way they are written. Hate Fish, which says immediately preceded, still asks only about the slot before it.
- Fixed an issue where a discount your rival paid for was handed to you instead. Uwabami lets your rival remove 3 cards from their discard pile to make their next printed 3 damage attack cheaper and harder hitting, and Keiko's Support lets them commit it to make their next card that shares symbols with their character cheaper to play or better at blocking. Both are enhance abilities, so your rival can play one while defending against your attack, and both grants were kept once for the table rather than per player: the next matching card you played in that same combat phase took the discount they had bought, and theirs arrived at full price. Each player's grant now waits for that player's own next card, and counts symbols against their own character.
- Fixed an issue where a card removed out of a hand went into the removed pile face down, so nobody could see what had gone. Monster Zero, Yasha Nydoorin, Orphanmaker, Violent Animus Shot and Malicious Assault all make your rival remove a card from their hand, and G Corp CEO removes one from your own. The removed pile is public, but these put the card in hidden, and a card lying face down there does not count as yours: nothing printed on it could be read any more, and the cards that let you play out of your removed pile could not see it. Your rival's screen had the same pile wrong a second way, showing whichever card happened to sit at the front of your hand instead of the one you actually removed. Both screens now show the card that really left, face up.
- Fixed an issue where Leonardo, The Leader always banked his +1 damage on an attack you had not played yet. His second response says this attack or your next attack gets +1 damage after you mill, and only the second half of that was read: the bonus went to your next attack every time. On the turn his own first response mills for you, with an attack already blocked and sitting in front of you, the +1 that could have pushed damage through that block instead waited for an attack the turn might never reach. You are now asked which attack takes it whenever there is one in flight, and with no attack in flight it goes to your next one as before.
- Fixed an issue where Michelangelo, The Wild Card let your rival choose which of their foundations went back to their hand. Its enhance adds 1 ready foundation from each player's stage to their hand, and you do the adding, so both cards are yours to pick. Your rival was asked instead and handed back whichever ready foundation they most wanted to play again, while the one you were aiming at stayed standing in their stage paying for their checks. You now pick out of their stage yourself, and only their ready foundations are offered. Positional Advantage, Saihasho and Sliding Firecracker are unaffected: those say your rival adds, or each player adds, so there the choice really is theirs.
- Fixed an issue where Driven by Retribution and Yeetus Deletus let your rival choose which of their foundations left the stage. Both tell you to add a card from your rival's stage to their card pool, and both handed the pick over to your rival on their own screen: they chose, and on your screen the card never moved at all, so the foundation you meant to take was still standing there paying their checks. Yeetus Deletus also ignored its printed difficulty 4 or less cap, because a card your rival picks is not a card you may reach for. You now pick out of their stage yourself, the cap limits what you may take, Yeetus Deletus lands the card face down, and the card moves on both screens. Grape-Pinky Combo Mineta Bounce is unaffected: it says your rival adds the card, so that one is still theirs to choose.
- Fixed an issue where Concealing Power removed a card your rival chose, and only on their screen. Its response removes 1 of the cards your rival built during the Combat Phase, and your rival's board took whatever it had built most recently while yours did nothing at all: you spent the card and went on seeing that foundation standing in their stage for the rest of the game, which is what either of you pay checks with. You now pick which of the cards they built goes, and it leaves on both screens.
- Fixed an issue where Garett Brett let your rival choose the card. Its enhance adds 1 card from your rival's discard pile to their card pool, and picking it was handed to your rival, who chose which of their own cards your ability put there. The card keeps its type while it sits in their pool, so which one it is decides what anything reading that pool sees, and choosing it is the reason to play the ability at all. You now pick from their pile yourself, and the card moves on both screens. Ocean Buddies and Xangô are unaffected: those say each player adds a card from their own pile, so there you each still pick your own.
- Fixed an issue where a card moved from a discard pile to a card pool only moved on one screen. Ocean Buddies and Xangô have each player add a card from their own discard pile to their own card pool. Each player picks out of their own pile, and that choice was never reported to the other player: whoever chose saw the card move and the other went on seeing it lying in the discard. Since a card pool is what you pay checks from, the two screens disagreed about what either of you could afford. Ocean Buddies' face down rider and Xangô's seal now show on both screens too.
- Fixed an issue where a card you searched out of your deck never appeared on your rival's board. Twenty one cards search a deck, from Armin Arlert, Brilliant Mind building the card it finds face down to Superfly Stomp sending one to the discard pile, and the card only arrived on the other screen when your rival's copy of your deck happened to be holding that card at the time: otherwise the search moved nothing over there, leaving your board without it and your deck a card too full for the rest of the game. A card searched out of your discard or removed pile is now taken from that pile rather than out of your deck.
- Fixed an issue where a card you sent from your deck to your discard pile stayed in your deck on your rival's screen. The Unending Path and Resurrected Titans both look at the top of your deck and put a card in the discard pile, and your rival could end up seeing your discard short a card and your deck one card too many, which decides when you run out of cards. Seize the Opportunity had the same problem with the attack it hands you.
- Fixed an issue where Emerge Victorious built a Titan your rival could not see. Sacrificing a backup digs through your deck for a Shift Titan attack or a Titan backup and builds it, and the foundation appeared on your board alone: your rival's screen showed your stage without it and your deck one card too full, for the rest of the game. A Shift attack now also shows its foundation side on their screen, not its attack side.
- Fixed an issue where a card that makes your rival build from their deck showed you nothing. Hexing Spell Bolt, Cheerleader, Younger Toguro and 80% Power all send the top card or cards of your rival's deck into their stage, and their board built it while yours did not, so for the rest of the game your screen showed them one or two foundations short of what they actually had. Since foundation counts decide what either of you can pay for, and Cheerleader only plays when your rival has 8 or fewer foundations, the two boards could disagree about what was legal. A copy of a Unique foundation built off the top of a deck is now cleared away too, the way it already was for every other way of building one.
- Fixed an issue where Scanlan's Hand committed two rival cards instead of one. Its form says commit 1 rival non-character card, and that you may spend 1 momentum to commit your rival's character instead. The non-character commit happened before you were offered the momentum, so paying got you both commits, and on a turn where you had already spent momentum for something else it could skip the first commit entirely and take their character without asking. You are now offered the momentum first, and exactly one of the two commits happens.
- Fixed an issue where Beckett Mariner, Chaotic Ensign, T88 and Buffer Time read the wrong player's mill. All three say your rival mills 1 and then ask what they milled: a foundation for the first two, an attack for Buffer Time, with a different bonus either way. The question was being asked about your own milling instead, and nothing clears that record between abilities, so the answer came from whatever you had milled earlier in the turn. The same board could pay either bonus depending on what you had done before, and on a turn where you had milled nothing it always paid the Otherwise. All three now read what your rival actually milled.
- Fixed an issue where a counter you put on or took off one of your rival's cards did not show up on their screen. Horn Dash Hammer lets you choose a card in either stage and add a counter to it, and Soothing Grog's Rage takes one off a rival card, including their character. Whichever card you chose, the change was only ever drawn on your own side, so your rival went on watching the count they had before and the two of you disagreed about the board until something else redrew it. Both now tell the other player which card the counter landed on.

### 2026-09-25

- Fixed an issue where Horn Dash Hammer and Soothing Grog's Rage picked the counter for you. Horn Dash Hammer says choose a card and add 1 counter of the type already on it, and Soothing Grog's Rage takes 1 counter off a rival card, and both let you choose the card and then decided for themselves which counter it was. On a card carrying two kinds of counter that is the whole decision. You are now asked which one, and on a card carrying only one it still happens without a prompt.
- Fixed an issue where Double-Bladed Spin took milled cards into your hand without asking. Its blitz says add up to 1 Weapon attack and up to 1 Weapon foundation milled this way to your hand, and both halves were read as a demand: if the mill turned up a match it went to your hand whether you wanted it there or not. Cards in your discard pile are not spent, and other cards read them, so that is a real choice and you now get to make it, including taking neither.
- Fixed an issue where the drawback printed on Skillful Maneuvers and Bring Change to the World did nothing at all. Both say you cannot play copies of them for the rest of the turn, and both are actions, which you play by playing an ability rather than by dragging them into your card pool. Every restriction on playing a card was only ever checked on the drag, so an action was never checked against any of them and you could play copy after copy. The same restrictions are now checked wherever a card is played: a copy of a locked card is refused, "you cannot play attacks for the rest of this turn" also stops a retaliate and an Echo replay, and a card you try to play out of your discard pile is refused for the same reasons a card in your hand would be. Refused plays are also turned down before you pay for them now, so a drag that is going to bounce back no longer sacrifices a Heat token on the way out.
- Fixed an issue where Horn Dash Hammer's response added no damage. It says your attack gets +1 damage for each card you just discarded from your hand, and it was counting a list that only ever held cards discarded to pay a price, and even then only while the price was still being paid. By the time you could play the response the list was empty, so the bonus was always nothing. Discarding from your hand now counts however it happened, whether an effect asked for it, a cost took it, or you discarded for playing no form.
- Fixed an issue where Wall Maria's Might never drew you a card. It says add 1 Wall counter to a card in your stage, then draw 1 card for every 2 Wall counters on that card, and it was counting the Wall counters on the attack itself rather than on the card you had just put one on. An attack is never in your stage, so it never found a single counter and the draw was always nothing. It now counts the card you chose, so a card already holding 3 counters draws you 2 once the fourth goes on.
- Fixed an issue where the bonus on Execute Orders! and Teamwork Attack was measured off the wrong card. Both say the attack gets +X, where X is the difficulty of the foundation you just added to your hand, and neither was looking at that foundation at all: they read whichever card an earlier effect had last sealed or destroyed, and if nothing had, the bonus was nothing at all. The attack now gets exactly what the foundation you took is worth.
- Fixed an issue where Execute Orders! took a foundation out of your stage whether you wanted it or not. It says add up to 1 foundation from your stage to your hand, and the prompt would not let you leave without handing one over. You can now decline, in which case the attack gets no speed bonus, which is the trade the card is offering.
- Fixed an issue where Jin Kazama's second enhance built two foundations out of your hand whether you wanted them or not. It says build up to 2 foundations with difficulty 3 or less, and it was reading that as build 2, with no way to stop once the first card had been asked for. It now asks how many first, so you can build one, or none at all, and keep the rest of your hand to play.
- Fixed an issue where Burning Godzilla's enhance removed cards from both card pools without asking anyone anything. It says remove up to 2 cards from each player's card pool, and it always took exactly 2, always the last 2 played, which are usually the attack in flight and whatever went with it. Removed cards are out of the game, so that is not a small difference. You now pick the cards yourself, from your own pool and then your rival's, and you can take one or none instead of two.
- Fixed an issue where Inconvenient Duplication built the top card of both players' decks whether either of you wanted it or not. The card says each player may build, and building takes a card neither of you has seen out of the deck for good and puts it in your stage. Both of you are now asked, and either can say no independently.
- Fixed an issue where milling a card counted as discarding one for Shoot Style: Knee Smash and Final Test. Both ask whether you have discarded a card, and neither names a zone, which in this game means from your hand. Milling puts a card straight from the top of your deck into your discard pile without your hand ever being involved, so paying a mill cost was handing you 3 health or a free card you had not earned. Both now read your hand, and paying an ordinary discard cost still answers them.

- Fixed an issue where eight cards that say "you may" did the thing for you whether you wanted it or not. Attack Titan's Wide-Swinging Blow and May turned one of your own foundations face down, taking every ability printed on it with it, and there was no way to say no. Yeagerist Takeover, Scanlan Shorthalt, Reiner Braun, All For One and Persuasive Talent moved a card out of your discard pile or momentum without asking, and Pieck Finger searched your deck and built a card you may not have had room for. Each of these ends in a picker that wants an exact number of cards behind a confirm button, so once it opened you were committed. All eight now ask first, in the card's own words, and declining leaves the board exactly as it was.
- Fixed an issue where paying a Drive cost out of your momentum put the wrong card in your discard pile on your rival's screen. A Drive is paid by committing foundations or spending momentum in any combination, and Rising Uppercut, Feng Shui Engine, Cammy, Killer Bee and nineteen other cards print one. Your momentum is face down to your rival, so their copy of the game is told which card you spent; for the momentum half it ignored that and discarded whichever card happened to be on top of your bar instead. The discard pile is public, and cards count and name what is in it, so the two of you were reading different piles. The card you actually spent is now the card they see.
- Fixed an issue where Waylay did nothing when you blocked with it, and gave back the momentum it took to the wrong player. The card empties your rival's momentum for the rest of the Combat Phase, and that was carried by a shortcut wired to the ways you play an attack on your own turn: blocking with Waylay is still playing it, so it went off for nothing. When the cards were handed back, the game worked out whose bar they belonged in from whose turn it was rather than from where they came, so a Waylay played as a block moved your rival's momentum into yours. The cards now go back to the player they were taken from, however the card was played.
- Fixed an issue where Emergency Treatment paid the progressive difficulty its only sentence says it ignores. Playing an action for its ability works out the difficulty while the card is still in your hand, and a card only had its own continuous text read once it was on the board, so the exemption arrived a moment too late to count. Anything printing "this card ignores progressive difficulty" or "this card gets -N difficulty" is now read off the card you are playing, wherever you are playing it from.
- Fixed an issue where Stealing Quirks took your rival's momentum without asking them. The card lets you have your rival spend a momentum card to pay for your keyword ability, and it pulled one off the top of their bar: they never chose which card went, it landed face down in a discard pile both of you are meant to be able to read, their own cards that answer a momentum card reaching the discard pile never fired, and your screen went on showing them momentum they no longer had. Your rival is now asked which card goes, exactly as they are for every other card that empties their momentum.
- Fixed an issue where a card revealed off a deck was never shown to the other player. The player doing the revealing saw the real card turned over and held up; their rival was sent its name as a line of text while their copy of it stayed face down on the deck. A name is not a card, and several of these abilities ask you to decide something on the difficulty, type or text of what was turned over. Both players now see the card itself, and it goes back exactly as it was.
- Fixed an issue where Reina, King Ghidorah and Reiner lost a game they print a way out of. All three replace the loss when your health is reduced below 1, and the replacement was only ever offered when an attack dealt the killing blow or when you did it to yourself. Health taken below 1 by your rival's effect ended the game without your character being asked, and the game is now called only after the board that can refuse it has answered. Reina's survival is spent by that route as well, so it is still the first time only, and a loss you survive no longer reaches your rival as a second hit that showed them a victory in a game you were still playing.
- Fixed an issue where Little Mister left the commonest mill in the game alone. It mills one extra card whenever you would mill, and most cards that mill do so as the price of their own ability, which was taken straight off your deck without asking your stage. Both cards now count as milled that way, so a clause that pays you back for "1 card milled this way" can reach the extra one, and an ability is only refused for want of deck if the enlarged mill is the one that cannot be paid.
- Fixed an issue where Little Mister gave you nothing for the stamina it costs. It pays a keyword ability you spent momentum on as though you had spent 1 more, and Powerful and EX both pay out per momentum spent, but the extra was being added to the keyword's rating at the moment the keyword was handed to an attack. A keyword printed on the attack is never handed to it, so the usual case got nothing, and the rating is the wrong number in any case: at Powerful 2 with 3 momentum spent it is worth 2 more damage, not 3.
- Fixed an issue where cards that answer something you did on your rival's turn did nothing. Leo's Katana builds itself after you mill it and Yeagerist Takeover rewards the same mill, but a mill your rival called for, or one from a check to play a block, counted as nobody's. Attitude Selector missed a card discarded from your hand to pay for a block, even though it already saw one removed that way. Erwin Smith, 13th Commander of the Survey Corps missed a foundation sacrificed to pay for a block.
- Fixed an issue where a card that answers its own payment did nothing when you paid on your rival's turn. Nature Calls readies itself after it is committed to pass a check to play a block, and a block check is only ever made on your rival's turn, so it never fired once. Strength in Diligence, Bison . . . Who Is That? and Assume the Worst answer being committed for a Drive cost, which Rising Uppercut, Exilio and Countersnipe all pay while blocking. Forceful Negotiator, Defiant Stance, Double Sword Style and the two Wielders answer being committed for any cost at all. Each of them asked whose turn it was rather than who paid, so they were dead off-turn, and your rival's copy was the one being offered instead.
- Fixed an issue where a card that debuffed your rival's check let them off a second failed check as well. Bison . . . Who Is That?, Psycho Power, Insubordination, Mollywhop and five others take a chunk off your rival's check and print "failing that check will not end the Combat Phase" alongside it. The second half was only ever spent when a check actually failed, so a rival who took the debuff and passed anyway kept the exemption standing, and the next check they failed that Combat Phase did not end their phase either.
- Fixed an issue where a retaliating attack left two things unfinished. Rising Uppercut, Exilio and Countersnipe play themselves back as an attack after they completely block one, and that attack can be blocked in turn, which opened no window for anything answering "after your blocked attack resolves". It can also carry Echo, and paying Echo's momentum on a retaliate bought nothing: the replay was never offered, and the offer was still owed when your next attack came around, which handed a free extra form play to a card that had no Echo at all.
- Fixed an issue where Waylay did nothing when it was replayed. Waylay makes your rival remove their momentum for the rest of the Combat Phase, and that is carried by a step only a card played out of your hand ever reached, so an Echo replay or a retaliation played it for nothing.
- Fixed an issue where the check made by an Echo replay or a retaliation was not recorded as a check. Lucky Break and Freaking Out ask about the card you checked to play the attack, and Corona Beam and Jet Uppercut ask whether that check was modified. After a replay they were all answered about the previous check instead. The battle log missed it too: the card was written down as played with no check above it, and a replay passed by committing foundations now reports the value it actually ended on.
- Fixed an issue where an Echo replay that was dropped mid-sequence locked up your side of the board. If the replayed attack left your card pool or was turned face down while it was resolving, your card pool and hand stayed locked and the Ready button stayed greyed out, with nothing left to release them.
- Fixed an issue where an Echo replay or a retaliation never settled what the attack left owed. Inverted Cut and Propelled Kick clear themselves from your card pool after they resolve, Big Freakin' Explosion costs you health equal to half its damage, Focused Gravity Beam removes itself, a foundation removed for the length of an attack is built back when it ends, and a rider held for "your next attack this turn" is spent by the attack that matches it. None of that happened when the attack was replayed by Echo or played back as a retaliation, and some of it was left sitting to fire behind whatever attacked next instead.
- Fixed an issue where nothing could respond to an Echo replay or a retaliation being played. A response window opens when you play a card, and it is the window Show of Strength, Arrow Kick, Nullifying Force and Reiner Braun, Marley's Shield all answer, along with roughly a hundred other cards that read "after you play an attack" or "after an attack is played". Only a card played out of your hand opened it, so an attack replayed by Echo or played back as a retaliation was a play nothing in either card pool could answer. All three ways of playing a card now open the same window.
- Fixed an issue where an Echo replay was invisible to your opponent's side of the table. Echo lets you play the attack again as your next form, and your opponent was never told the replayed attack had begun, so their board kept the previous attack bound with its speed and damage still applied, and the cost of blocking the replay was worked out from those numbers instead. Their side now picks the replay up the same way it picks up an attack off the attack stack.
- Fixed an issue where an Echo replay did not count as an attack played this turn. Playing the card again as a form is playing an attack, so "after you play your second attack this turn" and "your last attack this turn" should both see it, and neither did.
- Fixed an issue where an attack never remembered being played from anywhere other than your hand. Combination Blast gets +1 speed and +2 damage, Demonic Catastrophe +2 and +2, Demon Lord's Blast -1 difficulty and +3 damage, Adaptive Stabbing gains Throw and makes your rival flip a foundation, Appendage Onslaught gets +1 to its Stun rating, Shapeshifting Impalement costs your rival 1 health, and Overdrive Uppercut loses Powerful. Where a card was played from is worked out as it reaches your card pool, and it was then wiped a moment later when the check passed, so every one of those cards read "from your hand" no matter where it actually came from. Demonic Catastrophe's own ability plays it out of your discard pile, and even that did not count. They now all read the zone the card really came from.
- Fixed an issue where playing a card that was already on the table never counted as played from anywhere other than your hand. An Echo replaying itself from your card pool, a card lifted out of your discard pile or deck by an ability, and Aerial Kikosho replaying the card it just blocked with, all ran their own check outside the usual route and so were recorded as though you had played them from your hand. They are now recorded for what they are, which also means Concealing Power's "if you have played a card from anywhere other than your hand this turn" finally counts them.
- Fixed an issue where your rival's check to play an ability on an action card was answered about the wrong card. Insubordination, Fighting for Control and SpaceGodzilla, Bio-Quartz Monster all answer your rival making a check to play a card, and your side of the table only learns which card a check is for once that card has left their hand. An action's ability is checked while the card is still in their hand, so all three read whatever your rival last played and charged the check for that instead. Your rival's side now names the card it is checking to play, so those three see the action itself and answer the check they are printed for.
- Fixed an issue where Violet Suit and Machine Mayhem had never worked. Violet Suit lets you commit it as though it were a foundation to pass a check to play an asset or Weapon card, and Machine Mayhem lets you commit assets as foundations to pass the check to play it. Both are read only while the commit window is open, and the game forgot which card the check was for just before opening it, so both were asked and both said no. Both now count.
- Fixed an issue where cards that answer a check to play a card ignored an Echo card's second check and a check to play an ability on an action card. Devil's Instincts gives your check +1 after you make a check to play a card, Isla, Dreaming Brilliance gives +3 for an Ally card and Strong Windup +3 for a printed difficulty of 6 or greater, and none of them could see either of those two checks. They now can, and so can the cards that answer your rival's.
- Fixed an issue where most failed checks were not announced, so the cards that watch for one never fired. The Joker lets you ready your character or remove the top card of a deck after you fail a check, and Fortune's Favor and Mark Tyner answer your rival's. None of them names a kind of check, and the game only said so when you failed a check to play a form. Fail a block, fail an Echo card's second check, or fail a check to play an ability on an action card, and all three sat silent. They now fire on any of the four. Fortune's Favor's other half, which keeps your Combat Phase running after a failed check to play a non-attack card, counts a failed action's ability but not a failed block: blocking is not playing the card as the non-attack it prints.
- Fixed an issue where a bonus you won on an Echo card's second check was not added to it. Strong Windup and the cards like it are played after a check is made and give that check a bonus, and the Echo check let you play them and then compared the original number anyway. Worse, the bonus stayed banked and was handed to whatever check you made next, so a card you spent on an Echo turned up on an unrelated check later in the turn. It now counts on the check it was played on, and the number on screen updates before you are asked to cover the gap.
- Fixed an issue where a check to play an ability on an action card never offered you the chance to commit. Every other check in the game asks: when the number you check falls short, you may commit foundations and your character to cover the gap. This one compared the two numbers and failed the card on the spot, with the foundations that would have paid for it standing untapped in your stage. It now asks, the same as a check to play a card from your hand and a check to block.
- Fixed an issue where nothing could answer the card you milled for a check to play an ability on an action card. The mill opens a window at every other check, and this one opened none, so nothing that watches for a card being milled ever saw it, and a card that improves the check you just made could not be played on it. Strong Windup gives +3 to a check to play a card with printed difficulty 6 or greater, and playing an ability on an action card is a check to play that card, but there was no moment in which to play it.
- Fixed an issue where playing an ability on an action card ignored every discount to that card's difficulty. Playing the ability plays the card too, so the check is a check to play it, but the difficulty was set at the card's printed number plus progressive difficulty and nothing else. Kick Start My Heart's own "this card gets -1 difficulty if you've played a Roman Cancel ability this turn" was worked out and then left out of the total. Reiner Braun, Marley's Shield gives your non-attack cards -1 difficulty and never reached one, though an action is a non-attack card. A discount waiting for the next card you play, such as the one Resurrected Titans leaves behind, was neither taken off nor used up, so you paid full price and it sat armed for something you had not bought it for. All of them now count, the same as when you play the card on its own.
- Fixed an issue where a bonus to your checks that lasts the turn only counted on the check to play a card from your hand. Blocking makes a check, and so do an Echo card's second check, an action played for its ability, and a check you make outside of playing anything. None of them were looking at the bonus, so a form you had just paid for bought you nothing on the block that came next, and the bonus quietly expired at the end of the turn. All of them now count it. A bonus that names what you are playing, such as "your checks to play attacks", still asks what you played: blocking with an attack is playing it as a block, so a block gets the part of the bonus that names no card.
- Fixed an issue where the standing check bonus printed on a character only reached the check to play a card from your hand. April O'Neil, High School Reporter gives your checks to play Ally attack cards +1 and Victor Chevalier gives your checks to play asset cards +1, and both were skipped by every other check in the game.

### 2026-09-24

- Fixed an issue where A Life of Danger and Family Secret watched the wrong number on the card you checked. Both say that after you check a low number your check gets +1, and the number a check is named for is the blue one in the card's lower right. Both were reading the orange difficulty in the top left instead, so the +1 turned up on a strong check that happened to be cheap to play and stayed away from the weak check it is printed to rescue. Both now read the number you actually checked. Bishop, Robotics Engineer says "an asset with printed difficulty 3 or less" and is the one card of the three that means the difficulty, so it is unchanged.
- Fixed an issue where Colossus's Steam Barrier and Young and Free stopped your own cards from lowering your attack. Both say your attack's speed or damage cannot be reduced below printed by rival effects, and the three words at the end were being dropped, so the floor was held against everyone including you. Anything you played to lower your own attack was refused while one of these was up: reducing your damage to pay for something else, or slowing your own attack to set up a card that reads its speed. Both now turn away only your rival's reductions, and your rival can still take back a bonus you added and is stopped at the printed number. Determined Advance, Reiner's Toughness and Double Tornado Fist name nobody and still hold against every reduction, including their own controller's.
- Fixed an issue where Kenny Ackerman, The Ripper and Cart Titan ignored the choice printed on them. Kenny says you draw 2 cards or your rival loses 3 health and discards 1 card, and was doing all three at once. Cart Titan says the next foundation you try to play ignores progressive difficulty or your rival commits 1 foundation, and was committing the foundation every time while the exemption was dropped entirely, so the half of the card you were most likely to want could never be used. Both now ask you which one you want, and Cart Titan's exemption waits for the next foundation you play rather than being spent on whatever you play next.
- Fixed an issue where Nullifying Force and Nameless Man reduced the attack they were supposed to freeze. Both say an attack's damage cannot be modified, and both were holding it at the damage printed on the card instead of the damage it had. Everything an attacker banks for an attack lands before either card can be played: "your next attack gets +2 damage", the bonuses your foundations give attacks of a type or zone, and the attack's own printed bonuses. So an attack built up to 12 was not frozen at 12, it was knocked back to 4, and the card that forbids modification was performing the biggest reduction in the game. Both now hold the attack at whatever its damage was when they resolved, and still refuse every bonus and penalty after that.
- Fixed an issue where Guardian Angel of Chinatown and Soaring Anvil Smasher gave an attack far less protection than they promise. Both say your attack's damage cannot be reduced by rival effects, but both were only stopping it from falling below the damage printed on the attack. An attack printed at 4 damage that you had enhanced to 12 still lost every point of that work to a rival's reduction, which is exactly the attack you spend these cards on: Guardian Angel flips itself to answer a rival who has just reduced your damage, and Soaring Anvil Smasher spends a Heat token. Rival reductions are now turned away outright, whether they arrive as a damage penalty, as "reduce its damage to", as Deflect, or as an effect setting the damage lower. Your own cards can still lower your attack's damage, and the cards that say "below printed", such as Determined Advance, Colossus's Steam Barrier, Reiner's Toughness and Young and Free, are unchanged.
- Fixed an issue where cards that ask what an attack's speed or damage is read a number the attack no longer had. Each of them added the printed value to the bonuses on top of it and stopped there, so every reduction, cap and floor applied since was invisible to them. Double Tornado Fist, Wind Barrier, High Octane Rush, Rushing Forward and Hang Ten all pay out once an attack reaches a speed, and paid out on attacks a defender had already slowed below it, while Luke Sullivan, Gym Coach checked for a speed of exactly 5 the same way. On the damage side, Potemkin, Heihachi Mishima, Head of the Mishima Clan and Rose Whip Barrage fired on damage that had already been reduced away, Creeping Vine Eruption missed its "less than 5 damage" reading for the opposite reason, Pact of Wrath protected an attack whose damage was no longer 8, and Burning Fist's "damage cannot be greater than its printed damage" was ignored by every one of them. Worst of the set was Doty the Automaton, which returns an attack to its printed damage when that damage would be lethal: it fired against attacks your other cards had already made survivable, and handed the damage straight back. All of them now read the speed and damage the attack actually has.
- Fixed an issue where cards that reduce an attack's speed or damage could raise it instead. "Reduce" was being read as "set to", so the number was moved to whatever the card named from either direction. Rising Uppercut, Size Reduction, Soar Above and Acidic Clutches all reduce the speed of the attack you are blocking, and against a slower attack they sped it up, making the block they were played for harder rather than easier. Izuku Midoriya, Quirks Unleashed, Assassin Skill Tree and Childlike Appearance did the same to an attack another card had already slowed. On the damage side, Reiner, Armored Titan, Carnival Barker and Natural Cover reduce an attack to 1 damage and handed damage back to an attack already held below it, while Reiner's Toughness, Body Memorization, Invincible Body and Floch Forster, Yeagerist Leader could undo a larger reduction the same way. All of them now only ever lower the number, and the cards that say "change" a speed or damage to a value, such as Roman Cancel, Referee Juri, Substitute Member and My Fists Solve My Problems, still set it from either direction.
- Fixed an issue where Porco Galliard and Hiei, Dragon Within answered a block on the wrong side of the table. Both say "after your rival plays a block" and both punish being blocked, Porco Galliard by sealing the block and Hiei by sealing it, discarding it, cancelling the block outright and handing your attack back its printed speed and damage. Each was only ever offered to the player who had just played the block, who has no rival block to answer, so neither could be used. They now come up for the player whose attack was blocked, and "after a block is played", which names nobody, still answers for both players.
- Fixed an issue where nothing that reduces incoming damage was offered to the player taking it. Redirect Power to Shields, Potemkin, Impenetrable Defense and Toughest Punk in Junior High all say "before you take damage from an attack", and Grog Strongjaw, Mighty Half-Giant, Roman Cancel and Ryukyu (II) say the same of an unblocked attack. All seven were being offered to the player swinging instead, who takes no damage and has nothing to reduce, so none of them could ever be used for what they are printed to do. They now come up for the player about to be hit.
- Fixed an issue where the two cards that answer damage by naming who took it were each offered to the wrong player. Colossus's Thermal Blast ruins 13 "after this attack deals damage to your rival", and was only ever offered to the player being hit, who does not hold the attack, so the ruin never happened once. Plate of the Dawnmartyr costs the attacking player 5 health after an attack deals damage to your character, and was offered only to the player swinging, where it took the health off the person they had just hit. Both now go to the side whose character the damage landed on, and the many cards that say only "after this attack deals damage", or that name a character or a backup rather than an owner, are unchanged.
- Fixed an issue where cards that answer a destruction never checked whose card was destroyed. Cleaving Swipe gains Echo "after a rival backup is destroyed" and never once did, because the only ways a rival backup dies are your attack and your effect, and both were being treated as the other player's business. Cheerful Teen missed the same way, drawing you a card only if your rival destroyed their own foundation and not when you destroyed it for them. The mistake ran both ways, so Marco's Potential, Death Rattle and Bound by Blood, which watch your own stage, sat quiet when a rival effect took one of your cards, while Students of Tung Fu Rue gained you health for a foundation leaving a stage that was not yours. All six now read who owned the card rather than who caused it, and the ones that name no owner, such as Erwin Smith, Strategic Mastermind and The List, still answer either side.
- Fixed an issue where Beast Titan drew two cards for one backup leaving. It draws after a Titan backup enters or leaves your stage, and counted a sacrificed backup as leaving twice now that sacrificing also counts as destroying. One backup leaving is one card again.
- Fixed an issue where Concerned for Annie sped up your attack for almost anything. It says "after this card is discarded or sacrificed", and answered every way a card can reach your discard pile instead: milled off your deck, cleared out of your card pool, spent as momentum or destroyed by an ability. It now answers the two ways it prints, and only those.
- Fixed an issue where sacrificing a card did not count as destroying it. Sacrificing means choosing a card in your stage and destroying it, so every card that answers a destruction is owed a sacrifice too, and none of them ever saw one. Students of Tung Fu Rue says "after 1 or more foundations leave your stage, gain 1 health" and sat quiet through the commonest way a foundation leaves one. Erwin Smith, Strategic Mastermind, The Greater Goal, Sakyo's Gamble, The List and Death Rattle never counted a sacrifice, and cards that answer their own destruction, such as Smiling Death, Mechazoid, Enormous Axe and Arrogant Fighter, never fired when they were the card you gave up. Sacrificing now opens the destroy response windows as well, and cards that name a rival effect as the cause still only answer one.
- Fixed an issue where Reinforcements built a card off any sacrifice. It says "after this foundation is sacrificed to pay a cost", and the price was never checked, so a foundation an ability sacrificed paid out the same as one you spent. It now only answers a sacrifice you made to pay for something.
- Fixed an issue where spending momentum did not count as the cards reaching your discard pile. Spent momentum goes to your discard pile, but nothing said so, and cards that answer entering your discard pile during the Enhance Step, such as Unabashed Manner, Avoiding Conflict, Cycle of Violence and Nothing But a Squawking Crow, never saw the ordinary way an Enhance Step gets paid for. Burning Fist says it removes itself when it enters your discard pile from your card pool or momentum, and the momentum half had never once happened. Spending momentum now opens the same response window as any other way into the discard pile.
- Fixed an issue where cards that name the place they came from answered from anywhere. Leo's Katana and Yeagerist Takeover say "after you mill this card", and fired for any trip to the discard pile: Leo's Katana is an asset, so sacrificing it out of your stage called that a mill and built it straight back into the stage you had just paid it out of. Demon's Shaft and Burning Fist say "from your card pool" and removed themselves after being discarded from anywhere. All four now only answer the zone they print.
- Fixed an issue where a foundation destroyed to pay for an ability never noticed it had gone to the discard pile. Cards that respond after entering your discard pile, such as Unabashed Manner, Avoiding Conflict, Banana, Hot and Concerned for Annie, answered when they were sacrificed or when an ability destroyed them, but not when they were the foundation you gave up for an "Enhance Destroy 1 foundation" price. Destroying a card to pay now opens the same response window as any other way of destroying it.
- Fixed an issue where paying for an ability by milling did not count as milling. Cards that respond after you mill, such as JP, Regal Businessman, Unlimited Psycho Crusher, Unbreakable Cheer and Leonardo, The Leader, only saw mills that came from an ability's text, so an enhance priced at "Mill 1" never gave you the chance to answer it. Milling to pay a price now opens the same response window as any other mill, and cards that respond to a card entering the discard pile see those cards too.
- Fixed an issue where Cammy, Killer Bee's Response was free. It costs a commit and clearing 1 card other than the attack from your card pool, and the clear was never charged, so after paying any Drive cost you could pull a non-Ranged attack back out of your discard pile for the commit alone. It now clears a card as well, and is not offered when your card pool holds nothing but the attack.
- Fixed an issue where Bridget's Enhance could flip the attack it was boosting. It flips 1 other card in your card pool, and the attack you are enhancing was being offered as a target, which turns it face down and blanks it. It now only offers the other cards in your pool.
- Fixed an issue where Kevin Broberg's revealed cards were hidden again straight away. His Form says the 5 cards you reveal stay revealed for the rest of the turn, and they were turned back over after the usual look like every other reveal. They now stay face up on both boards until the next Start Phase.
- Fixed an issue where Mollymauk Tealeaf, Carnival Hooligan sealed nothing. His Response reveals up to 2 cards from your hand and seals 1 rival foundation for each card revealed, but the reveal could never find your hand, so it turned over nothing and sealed nothing while still using up your once per turn. It now reveals the cards you pick and seals a foundation for each one.
- Fixed an issue where half of Kevin Broberg did nothing. His Form reveals 5 cards from your hand and prints two rewards under opposite conditions: one if all of them share a keyword, and one if none of them share a printed difficulty. Only the first was ever read, so when the cards you revealed all had different difficulties the Form cost you a commit and paid out nothing. The second reward now works: all checks get +1 or -1, your choice, until your next Start Phase.
- Fixed an issue where Ramlethal's Greatswords could never be cancelled. It names a block zone, and your rival may reveal a card from their hand matching that zone to cancel it. A cancel has to be offered before the ability it would stop, and the offer was being made before the zone was named, so there was no zone for a card to match and the offer was never made at all. The zone is now named first, and your rival gets the choice the card prints.
- Fixed an issue where JP, Regal Businessman and Xilien Invasion made you take what they found. Both say "up to", which is a ceiling you are allowed to come in under, not an amount you owe. JP searches for up to 1 copy of Departure and put it in your discard pile whether you wanted it there or not, without ever opening the search for you to look at. Xilien Invasion searches for up to 3 copies of a card you name and added all three to your hand. JP now offers the card and lets you take nothing, and Xilien Invasion asks how many copies you want.
- Fixed an issue where Disarming Glance shut off every ability in the game. It stops players from playing abilities that add cards to their hand during the attack, and it was being read as a bar on abilities full stop, so for the rest of that attack neither player could play a block's ability, a damage reduction or any response at all. It now only stops the abilities that put a card in your hand.

### 2026-09-23

- Fixed an issue where Reverse Narcissus never left your card pool. It says it does not clear during the End Phase, which buys it one turn so its "[Card Pool] Your rival's attacks get -2 speed" is still up while your rival takes theirs. The exemption was never spent, so the card stayed in your pool for the whole game and every copy you played stacked another permanent -2 speed. It now survives one End Phase and clears at the next.
- Fixed an issue where Nullifying Force and Nameless Man froze an attack's damage forever. Both say an attack's damage cannot be modified, meaning the attack they are played against. The freeze was recorded against the card rather than the attack, so if that same card was ever played again its damage was still stuck at printed. Burning Fist, which caps its own damage, is unchanged.
- Fixed an issue where permission to play a card from your removed pile or discard pile never ran out. Spewing Vitriol, Hotheaded Opener, Dream About Fighting and Enough Talk all remove cards and let you try to play them this turn, Flying Elbow Drop and King Ghidorah Unleashed let you play themselves out of the removed pile, and Forbidden Exorcism, King Ghidorah, Emperor of the Cosmos, Kazuya Mishima, Nina Williams and Yusuke, Team Leader do the same from one pile or the other. Every one of them says "this turn", and the permission was never taken back, so a card you declined to play on your first turn was still sitting there playable on your ninth. It now ends when the turn does.
- Fixed an issue where health you gain for blocking arrived too late to save you. Clasp Membership and Makeshift Repair give health for partially blocking, and Faultless Defense, Grasp for Survival, Scouting Skirmish, Help or Harm and Sacred Guardian give it for blocking at all. A partially blocked attack still deals half its damage, and the game ends the moment you reach 0, so a player who blocked to survive was finished before the health was ever offered. All seven now resolve while the block is still on the table, before the damage. Blocking responses that build or recall the blocker, such as Size Specialist, still resolve after the attack.
- Fixed an issue where an attack that gets extra damage for going unblocked never got it. Mikey's Nunchaku, Spinning Crescent Kick, I Am the Dragon and Leatherhead, Eager Expat all say an unblocked attack gets more damage, and Potemkin Buster says the same for an attack that was not completely blocked. All five were offered only after the damage had already been taken, so the bonus arrived too late to change anything. They now come up before the Damage Step. Unblocked responses that do something else, such as Flying Heel Kick granting Flash to your next attack, still resolve after the damage.
- Fixed an issue where an attack that says it still deals damage after being completely blocked dealt none. Steady Aim says a completely blocked attack deals 3 damage during the Damage Step, and Right Flamingo says your completely blocked Kick attack still deals 1. Both were offered only after the attack was over, which is after the Damage Step they name, and Steady Aim was setting a number a completely blocked attack never reads. Both now come up while the block is still on the table, and the damage lands. Cards that answer a completely blocked attack by drawing or discarding, such as Ryu, World Warrior, still resolve after the attack.
- Fixed an issue where Spirit-Weapon Whirl never let you choose where the attack went. It returns an attack from your discard pile to your card pool "in any position", and the game always put it on the end. Position is not decoration: cards that care what sits next to what in your card pool read that order. You are now asked where to place it.
- Fixed an issue where cards that pay you for blocking with a foundation paid you for blocking with anything. Nejire Hado (II), Izuku Midoriya, Deku, Creative Counter and Size Specialist all build the card you blocked with into your stage, and all four say it has to be a foundation. Blocking with an attack built that attack into your stage instead. Creative Counter now waits for a foundation with a keyword, and Size Specialist still refuses to build another Size Specialist. Cards that say only "after you block", such as Mikasa Defeats the Female Titan, still take any blocker.
- Fixed an issue where it did not matter whether an attack hit your rival's character or one of their backups. Swift Execution and Anti-Titan Artillery Shell pay you for damaging a backup, and were paying out for hitting the character instead. Bust In, Warrior Training, Jaw Titan's Trap, Swift Rescue, Kenny Ackerman, The Ripper, Mikasa Ackerman, Protective Friend, Levi's Relentless Spirit, Long-Range Support, The Viciousness of Kenny Ackerman, Colossus Titan's Destructive Power, Enraging Revelation, Bring Change to the World, Anti-Personnel Vertical Maneuvering Equipment, Plate of the Dawnmartyr, Harness Undeath, Fusion Chest Cannon and Knockout Punch all say they need damage to a character, and were firing when the attack went into a backup. Colossus's Thermal Blast says it needs damage to your rival, and likewise. Each now waits for what it asks for, and attacks that do not say which target still take either.
- Fixed an issue where playing a card as a block did not count as playing a card. Mechagodzilla, Kiryu, History's Greatest Monster, Godzilla, Titan of Terror and Display of Might all reward you for playing a card of a high enough difficulty, Gas Propellant rewards you for playing a card with a Breaker ability, and Caleb Widogast, Fiery Transmuter, Scanlan Shorthalt, Devious Troubadour, Choi Jong-In and Magic Trap reward you for playing an action card. None of them noticed a block, even though the rules say a block is still a card being played. They do now. Cards that instead say "after you play an action" or "after you play a foundation", such as Mean Intentions and Rapid Rescue, correctly still ignore blocks.
- Fixed an issue where nothing a card said about being destroyed, discarded, removed or cleared ever happened. Fifty-four abilities describe the moment a card leaves your board, and every one of them was refused, because by the time that moment arrived the card was lying in your discard or removed pile and the game did not treat either as somewhere a card can still speak from. Demon Energy Manipulation, Arrogant Fighter, Enormous Axe, Confronting the MLA, Smiling Death, Bright-Eyed Dreams and Mechazoid did nothing when destroyed. Questioning Yourself, The Intensity of Mikasa Ackerman and Reinforcements did nothing when sacrificed. Betraying Friends, Intense Heat Blast, Makeshift Maneuver, Wish Hard, Feral Shriek, Mikasa's Admission, Pilfered Provisions, Let's Rock!, Raphael's Sai, Flying Elbow Drop and Steel Muscle Explosion! did nothing when discarded. I'm With You, Loss of Consciousness, Eren's Trial, Hostile Introduction, Cycle of Violence, Nothing But a Squawking Crow, Avoiding Conflict, Unabashed Manner, Wolf's Ferocity, Brotherly Love, Extra Cheese, Banana, Hot, Concerned for Annie and Leo's Katana did nothing on reaching your discard pile. Supersonic Flight, Tinker Shot, Resounding Screech, Godzilla vs Gigan, Forbidden Exorcism, King Ghidorah Unleashed, Grinding Overtime, Improving Skills, Item Menu and Timely Recovery did nothing when removed. Cannon-Fire Barrage, Connie's Sword Strike, Venomous Dagger Slash, Hundred Lightning Kicks, Departure, Shoot Style: Knee Smash, Spirit Slash and Chomp did nothing on leaving your card pool. All of them now do what they say.
- Fixed an issue where a card saying it can be played out of your discard pile could not be. Short Work, Combined Firepower, Departure, Oxygen Destroyer, Phoenix Stance, Twist Reality, Demonic Catastrophe, Predator Bardiche, Devil's Instincts and Yeagerist Takeover all print that permission, and the game was treating every card in your discard and removed piles as belonging to nobody, so it never read what they say. It does now. A card removed face down stays private.
- Fixed an issue where nothing a card said about blocking with it ever happened. Fifty-eight abilities on fifty-seven cards read "after you block with this card" or "when you try to block with this card", the largest group of response abilities in the game, and every one of them was silently skipped: the card you block with goes to your card pool, and the game was treating the pool as somewhere a card's abilities cannot be played from. Wall Maria's Might, Reactive Kick, Sacred Guardian and Bagpipe Cacophony never drew you anything, Scouting Skirmish, Grasp for Survival and Help or Harm never gained you health, Armored Titan Attacks!, A Titan (Small) and Spirit Beast Puu never built themselves, Protecting Yukina, Colossus's Steam Barrier, Faith's Shield, Protector of Life and Cross-Up Protection never stopped the damage they block, Redirecting Push, Disabling Jab, Virtuous Plans and Dimensional Sphere never touched the attack they blocked, Learned Technique, Undeterred, Belly Bump, Shell-Shocked!, Mollywhop and Concealing Power never slowed your rival down, and Acidic Clutches, Brace for Impact, Drift, Size Reduction, Soar Above and Rising Uppercut never took the speed off the attack they were checking against. Jin's Parry never ignored progressive difficulty, Anti-Air Rock Barrage never stopped counting toward it, and True 100% Unleashed never rescued the check it is printed to rescue. All of them now work.
- Fixed an issue where a card played as a block could not answer its own play. Forty-eight cards say "after you play this card" and then do something, and blocking with one is still playing it, but every one of them sat out the block. Reconsider never drew you a card, Ruthless Savagery and Good Deeds never gained you health, Soup, Badgey, Vengeful Pal, Numbers Advantage and Detachable Head never built themselves, Drive Parry never readied a foundation, Ignition Barrage and A Father's Sin never milled, Above the City and Dragonfly Blade never looked at your deck, and Tight Squeeze, Intimidating Glare, Wild Assault, Burnout, Biting Dagger, Thrash About and Off-the-Wall Kick never touched your rival's board. All of them now fire when you block with them. Inventor's Creation, which hands an attack every keyword printed on the card removed to pay for it, will not hand them to the attack you are blocking.
- Fixed an issue where setting an attack's damage locked the number for the rest of the attack. Reiner, Armored Titan, Reiner's Toughness, Carnival Barker, Natural Cover, Body Memorization, Invincible Body, Referee Juri and Roman Cancel's Yellow ability all change an attack's damage to a fixed number, and afterwards no damage bonus could move it again, so a +2 damage enhance played after one of them was simply thrown away. Setting the Standard and High Three were worse, because they set the number as the attack is played and every enhance for the rest of that attack was ignored. Splinter, Caring Father had the same problem when copying another attack's damage. All of them now set the damage the sentence names and let later abilities change it from there, which is already how the speed half of the same cards behaved.
- Fixed an issue where ten more cards that act on an attack as it is played did nothing. Sam Rutherford, Resourceful Engineer never switched a non-Throw attack's speed and damage, Nullifying Force and Nameless Man let a played attack's damage be modified anyway, Uplifting Bond never excused that attack from progressive difficulty, Sound Sensitivity and Armor-Clad Faith stripped no keywords, and Gargantuan Grapple, Mitchell Cimino and Mega Burst raised no keyword rating. Cute Baby #202 now adjusts the ratings of the card that was actually played, which on a block is the card you blocked with rather than your rival's attack.
- Fixed an issue where a card that clears itself out of your card pool stayed put. I Can't Forgive You, Jean's Provoking Stubbornness and Reconsider each say to clear the card from your card pool as you play it, and all three left it sitting there adding to the difficulty of everything you played afterwards. They now clear, and clearing one no longer calls off an attack that had nothing to do with it.
- Fixed an issue where cards that act on an attack the moment it is played did nothing at all. Thirteen cards say "after an attack is played" and then do something to it, and every one of them was reaching for the attack before the game had begun running it. Filled with Doubt, Allura Vysoren, Arcanist of Tal'Dorei, Nonagon and Spirit Detective all failed to seal it. Cardboard Crusader$ failed to seal your rival's first attack of the turn or hold it in their card pool. My Fists Solve My Problems and Izuku Midoriya, On the Move never changed its speed. Not Now, I'm Gaming and Toru Hagakure (II) never sent it back to its owner's hand, Kurama, Youko Unleashed never discarded it, Genkai's Guidance never removed it from the game, and Splinter never added it to your rival's momentum. Kaminari's Sharpshooting Gear never let you change the zone of a Charge attack you played. All thirteen now do what they say.
- Fixed an issue where a keyword granted the moment you played an attack was never granted at all. Tsukuyomi's Throw and Hates Lectures' Breaker: 2 are both handed out as the card is played, which is before the attack itself gets going, and the grant had nothing to attach to and quietly did nothing. Both now stick.
- Fixed an issue where blocking with a Kick, Ally or Diplomacy card did not pay out the cards that reward playing one. Hates Lectures, The Town Inside Me and Brad Boimler, By-the-Book Ensign all name a card type and a block is still playing a card of that type, so they now fire when you block with one.
- Fixed an issue where playing a block did not count as playing a card. Cute Baby #202, which adjusts the keyword ratings of any card that is played, and Percival de Rolo III, Vengeful Sharpshooter, which commits a foundation from each player after you play a card, both sat out every block in the game. Jaunty Trickster's discount for a non-attack card you play missed blocks for the same reason. All three now see a block, and blocking with an attack card still does not count as playing an attack.
- Fixed an issue where a card that excuses another card from progressive difficulty excused itself instead. Jaunty Trickster, Heidern, Hard-Boiled Assassin, Uplifting Bond, Bring Change to the World and Team Rival XV all say "that card" or "that attack" and mean the card you just played, but the discount landed on the card that said so. Heidern's went to a character, which is never in your card pool at all, so it did nothing whatsoever. They now discount the card they name.
- Fixed an issue where blocking was harder than it should be. Cards that say they do not count toward progressive difficulty, like Combined Firepower, Heroic Conviction and Trash City, were excused when you played a card but counted again the moment you blocked, so a busy card pool pushed every block out of reach. Jin's Parry, which says the block it makes ignores progressive difficulty entirely, was never consulted until the check was already over. Cards that discount your face down cards, like Loop Loop, Acid Screen, Growing Grasp, Biollante Arrives and Bullet Kick, were ignored on a block for the same reason, as was Hardware Hurl's discount on the next card you play. Blocks now work out progressive difficulty the same way every other check does.
- Fixed an issue where cards that slow an attack down as you block it did nothing. Acidic Clutches, Brace for Impact, Drift, Rising Uppercut, Soar Above and Size Reduction all read "when you try to block with this card", and the speed they take off the attack is the number your block checks against. They were being offered after the block was already over, so the check had been made at full speed and you had usually failed it. They now happen as you play the block, before the check, which is what they are for.
- Fixed an issue where a bonus promised to your next attack was spent on the attack you were already making. Dire Eclat, Acid Sprinkler, Team Stash, Leaping Tongue Lash, Cage of Hell and Michelangelo, The Wild Card each name the types that may claim the bonus, and naming more than one lost it: the speed and damage went to the attack in flight instead, and the Charge, Ranged, Slam, Weapon, Kick, Pizza or Punch attack you played next got nothing. The bonus now waits, and Michelangelo's waits for all three of the types he names rather than only Punch.
- Fixed an issue where "that attack deals no damage" came too late to stop anything. Faith's Shield, Protecting Yukina, Cross-Up Protection, Blueflame Surge, Protector Life, Colossus's Steam Barrier, Mikasa Defeats Female Titan, Nott the Brave and Adaptable Anatomy were all offered after the damage had already been dealt, so taking the option changed nothing and you lost the health anyway. They are now offered in the Block Step, before the damage, where they can actually stop it. Lightning Blast's damage bonus moved with them for the same reason.
- Fixed an issue where Deku's Swift Takedown and Radiant Pegasus Bomb acted a step too early. Both print "after it resolves", but the response they are offered in opens once damage has been dealt and before the attack has finished, so Deku's Swift Takedown flipped itself while it was still in flight and Radiant Pegasus Bomb built itself as a committed foundation out from under its own attack. They now wait until the attack has actually resolved.
- Fixed an issue where Breaker was offered at the wrong moment. It reads "after you block with this card", but the option also came up on your own attack once your rival had blocked it, and on Breaker cards that had not done the blocking, where choosing it did nothing. It now appears only on the card you actually blocked with.
- Fixed an issue where Ultimo Jaguar charged a Heat token whichever zone you played it from. It only asks for one "to play this attack from your hand", so flashing it back out of your removed pile or your momentum no longer costs you a token, and no longer refuses the play outright when you have none.
- Fixed an issue where Frenemies could never be played. It reads "you may try to play this card as a block from your stage", and a block window only ever offered cards from your hand, so the one thing the card does was unreachable. It now lights up in your stage while you are choosing a block, and clicking it plays it from there.
- Fixed an issue where Spire of Conflux only protected a Mage. It reads "if your character is a Mage or Warden", and a Warden character got none of the protection it prints for them.
- Fixed an issue where King Ghidorah Unleashed could never be played from your removed pile. After it was removed to pay a cost it asked whether you wanted to play it later, and answering yes did nothing: the permission it prints was never actually granted.
- Fixed an issue where Rodan, Fire Rodan could not seal a card in your rival's card pool. It reads "in your rival's card pool or stage", and only the stage was ever offered.
- Fixed an issue where cards reading "non-character card" could only reach your rival's foundations. Eight abilities that seal, commit or flip a non-character card in a rival's stage skipped past every face up asset and backup, so a rival holding assets was untouchable by them.
- Fixed an issue where Mikasa Ackerman, Hizuru's Hope paid her bonus damage twice. Her Enhance reveals a Weapon card and gives the attack +X damage, where X is that card's block modifier, and the bonus was added on twice: a revealed block modifier of 3 arrived as +6.
- Fixed an issue where All at Once!! cleared two cards from your card pool instead of one. It says to clear 1 other card, and you were asked to pick twice.
- Fixed an issue where Amplifier Jack Attack, Haraede Kannagi and Betraying Marco never paid out what they promise. Each counts something before it acts, and each count was asked in a way the game could not answer, so the reduced difficulty, the extra speed and damage, and the bonus for holding both a backup and an asset simply never arrived, however full your card pool or stage was.
- Fixed an issue where Frenzied Dive would not let you spend Power tokens on an EX ability. It says your attacks get +1 speed and you may sacrifice Power tokens as though you were spending momentum to pay for EX abilities, and only the speed arrived: the tokens were never offered, so an empty momentum bar meant no EX at all.
- Fixed an issue where Series of Strikes put your cards back in the order you chose. It says to add 3 non-attack cards from your discard pile to the bottom of your deck in a random order, and the order you picked them in was the order they went back, so the bottom of your deck was yours to stack.
- Fixed an issue where an offer you had nothing to pay for with still handed you the reward. Godzilla, Shin Godzilla says "you may commit this card. If you do, your rival sacrifices 1 foundation", and on a card already committed your rival lost the foundation anyway. Harley Quinn's version bought a card the same way, Reiner Braun's "commit or sacrifice 1 foundation, if you do, ruin 1" ruined with an empty stage, and Meteor Raid's "if you don't, this attack gets +5 damage" quietly gave the damage up when your rival held nothing to discard. The Titan cards also asked whether you wanted to transform a character you were not.
- Fixed an issue where an action card's Response never got a chance to fire from your hand. Actions are played out of your hand and 29 of them print a Response with no zone written on it, from Yeagerist Takeover's "after your rival plays a character ability" to the five that answer a block, but the moment they answer was only ever checked against cards on the table. The window simply never opened, so the ability was not refused so much as never asked about.
- Fixed an issue where you were never offered the chance to cancel your opponent's ability with a card in your hand. Drive Parry, High-Speed Dodge, Resolute End, Heroic Conviction, "Strange Energies", Psych Burst, Impenetrable Defense and Koenma's Task are all actions whose Response cancels something, and an action is played from your hand, but your hand was the one place the game never looked for one. Your opponent was not asked to wait for you either, so none of the eight could ever be played.
- Fixed an issue where a card played out of your removed pile stayed lying in it afterwards, so you had the same card in two places. Nick Ragan removes the top 8 cards of your deck and lets you play an Enhance off one of them, and an attack like Chivalrous Charge, whose Enhance is "add this card to your hand", ended up in your hand and in the removed pile at once. Enough Talk and Always Angry reach the pile the same way. Removing a card that was already removed listed it twice for the same reason, and none of it reached your opponent's screen at all.
- Fixed an issue where an ability your opponent played from their discard pile did nothing on your screen. Short Work and the nine other cards printing a "[Discard pile]" ability were mirrored without the card that played them, so a card that should have returned to their hand stayed sitting in their discard on your side of the board.
- Fixed an issue where a card you added to your momentum face up kept offering the abilities it prints for your stage. Only cards printing an ability bracketed [Momentum], such as Feeling Refreshed and Black Abyss, can be played from there; a foundation you committed to your momentum is set aside, not standing in a second stage.
- Fixed an issue where Stealing the Attack Titan's Blitz raised every check you made. "Your checks to play backups or Shift attacks get +3" was paying out on foundations, assets and every other attack as well, because it is the only card printing a check bonus that names two kinds of card at once and the second kind was being dropped.
- Fixed an issue where Hare Screech and Covert Black-Ops Arms did nothing when their attack was blocked. "If this attack is completely blocked, your rival loses 2 health" and "if this attack is blocked, your next Ally or Weapon attack gets +1 speed and +1 damage for every 4 foundations in your rival's stage" were never offered as Enhances, so neither ever paid out. Shoot Style: Mix-Up prints the same sentence and always worked.
- Fixed an issue where attacks that print conditional speed and damage never got them. "If you have fewer foundations than your rival, this attack gets +1 speed and +1 damage", "while you have 6 or more keywords in your card pool, this attack gets +3 damage" and twelve more like them were adding nothing. On the cards that print a difficulty discount in the same sentence, such as "if you have 15 or less health, this attack gets -1 difficulty and +1 speed", the discount was applied and the speed in the same breath was not.

- "After 1 or more of your cards is committed due to a rival effect, ready this card" and "after 1 of your foundations is committed due to a rival effect, ready 1 foundation" now answer for any of your cards, not only for themselves. Both were waiting for your rival to commit that exact card, so unless the rival happened to pick the one printing the ability, nothing happened.
- Cards that print a second thing to happen later now only do it if you played the ability that printed it. "This attack gets +2 damage. After it resolves, flip it", "play 1 foundation from your stage face down as a 2 difficulty Ranged attack. After it resolves, clear it or draw 1 card" and "remove 1 foundation from either player's stage. After this attack resolves, the owner builds it face up" were all handing out the second half to anyone with an attack resolving, whether or not the ability had ever been played. "Destroy 1 rival foundation with difficulty 2 or less. After this card leaves your card pool, remove it" was removing itself from the game off a card pool you had never used its Form on.

### 2026-09-22

- "Discard 1 card. Search your deck for 1 asset with difficulty equal to or less than the discarded card's difficulty" now respects the difficulty it names. The search was offering every asset in your deck no matter what you discarded for it.
- Branches of a "choose 1" that print their own condition now check it. Picking Acid on "Choose Acid, Cold, Electricity, or Fire" took a rival foundation straight away instead of waiting to see whether the attack dealt damage to a character, which made it the obvious pick every time. "Your rival discards 1 card if they have 3 or more cards in their hand" was taking the discard however few cards they were holding.
- "After an attack is blocked, look at the top card of your deck. You may commit this card" no longer asks you twice. The second prompt arrived after the card was already committed or not, and answering it did nothing either way.
- Cards that trigger off your board being wrecked "by a rival effect" now do. "After 1 of your foundations is destroyed by a rival effect, commit 1 rival foundation", "after a foundation leaves your stage due to a rival effect, build 1 foundation from your discard pile committed" and "after this card is destroyed by a rival effect, build the top card of your deck" were all being offered to the wrong player, so they never fired at all.
- Cards that name who did it now check who did it. "After 1 or more rival foundations are destroyed by your effect, gain 1 health and add 1 Power token to your stage" was paying out on any foundation leaving any stage, including the ones your rival gives up themselves to pay a cost, and the same the other way round.
- "After this backup is attacked, your rival loses 1 health" now only answers for the backup that was actually attacked. If you had two backups out, both were answering every hit on either of them.
- "After you play this foundation, gain 1 health" now only pays out when you play it. Once it was in your stage it was gaining you a health for every action, foundation and asset you played for the rest of the game.
- An attack that says "this attack" now means itself, and only while it is the attack being played. Attacks stay in your card pool once they resolve, so the second attack of a turn was setting off the first one all over again: "after this attack deals damage, destroy 1 rival foundation", "after this attack is blocked, mill cards from your deck until you mill an attack" and "after this attack resolves, clear this card from your card pool" were all paying out a second time off an attack you had already finished with. Close to 200 printed lines across every attack in the game are affected.
- Cards that say "during the Combat Phase" now wait for it. "After you build this asset during the Combat Phase, draw 1 card", "after this foundation is readied during the Combat Phase, draw 1 card" and "after you gain 1 or more momentum during the Combat Phase, ready this foundation" were all paying out on the ordinary build, ready and check you make every turn, a long way from the phase they name.
- The same was happening to your rival. "After your rival builds a foundation during the Combat Phase, flip and commit it" and "after 1 or more rival foundations are built or readied during the Combat Phase, commit and freeze 1 of them" were taking the foundation your rival builds in their Form Step every turn.
- "After your rival plays a response ability during your Combat Phase, cancel it" now only cancels on your own turn, and the one that reads "during this attack" now only answers the attack it is printed on. Both were answering any response ability at any point in the game.
- "After your rival commits 1 or more foundations during the Enhance Step, this attack gets +1 or -1 speed" no longer fires on foundations committed to pay for a block check, which is a different step and a different attack.
- "After you play an enhance during this attack, your rival commits 1 non-character card" now waits for your enhance and for that attack. It was firing on your rival's enhance abilities too, and on every attack in the turn rather than the one it is printed on, so it took cards off your rival that it was never owed.
- "After 1 of your foundations is flipped by a rival effect, unflip 1 foundation" now does something. Twenty-three cards can flip your foundations face down and none of them woke it, because it was waiting on your rival committing your cards instead, which is a different thing happening to a different card.
- Cards that buy the check to play themselves now do it while the check is still on. "After you make the check to play this attack, that check gets +2" was being paid out after the check had already been won, so it changed nothing, and "before you make a check to play this attack" was revealing two cards and discarding one before every check you made all game.
- Six cards that ask about a particular commit now check which one it was. "After you commit your character", "after this card is committed during an attack", "after you commit 1 or more foundations during the Enhance Step" and the two that count assets all paid out on any commit at all, so a single check that committed three foundations set off every one of them.
- Two cards reading "after your cards are committed by a rival effect" now fire when your rival commits them, instead of every time you committed a card yourself. They were exactly backwards: one readied a foundation and the other built a card every time you paid a cost or passed a check, and neither noticed your rival doing anything at all.
- Cards that name which card blocked now check it. "After your rival blocks with a non-foundation card" cost them a health for blocking with anything at all, "after you block with an asset with printed difficulty 4 or less" never fired once, and "after you play a high or low block" handed its Breaker to a mid block too.
- Cards reading "after you play this card as a block" now do something when you block with them. All three were waiting for a moment that only happens on your own turn, so two of them never changed the block zone they were played into and the third never cost you the health it prints.
- Cards that name what a price bought now check it. "After you commit this card to pay a Drive cost" (three cards) fired on any commit you made to pay for anything, "after this foundation is committed to pass a check to play a block" likewise, and "after you spend momentum to pay for a keyword ability" fired on every momentum spend, charging you a stamina each time for a bonus no keyword was there to collect.
- Cards reading "after you discard this card" now fire only when that card is the one discarded. Seven cards print it and all seven were reading the moment as "after you discard anything", so a card sitting in your discard pile paid out on every discard you made for the rest of the game, and the four that add "during the Combat Phase" paid out in every other phase too.
- Cards reading "after this card is discarded during the Combat Phase" now fire when you discard them to pay a cost. Paying a price was the one route to the discard pile that opened no window, which is the commonest way these eight cards reach the moment they name.
- Cards reading "after your rival plays an Enhance ability on a foundation" now check what the ability was actually played on. Seven cards print that moment and name four different things between them (a foundation, an attack, a non-character card, or nothing at all), and all seven fired on any Enhance your rival played, so five cancels went off against abilities they do not cover. The same reading now applies to the cards naming an action, an asset or foundation, or a card in your rival's card pool.
- Two cards reading "after your rival plays a response ability during your Combat Phase" (and "during this attack") no longer refuse to fire against your rival's character. They were sharing a restriction printed only on their siblings.
- Cards reading "after your rival plays a non-character ability that ..." no longer offer themselves against your rival's character. Nine cards print that exclusion and none of them checked it, so you could sacrifice or flip a card to cancel a character ability the card says it cannot touch. The three reading "... that reduces the damage of your attack" likewise stop offering during your rival's attack, where there is no attack of yours to reduce.
- Cards reading "before you take damage from an attack" are now playable against a partially blocked attack. The window they wait for only opened when nothing blocked, so seven cards, including the ones reading "before the Damage Step of your rival's attack", were dead at the one moment they name even though a partially blocked attack still deals half its damage. The three that print "unblocked" are unaffected.
- Six enhances that name an attack type in their subject now check it. "Your Kick, Punch, or Slam attack gets +2 speed and +2 damage" and its comma-separated siblings, plus the ones that print the subject behind a condition ("if your rival has lost health this turn, your Weapon attack gets ..."), were playable on any attack at all and paid out on it.
- The card whose bonus reads "your face up Kick, Punch, or Slam attack" now checks the facing. Its other ability stacks face down cards into your card pool as attacks carrying those exact keywords, so the bonus was paying out on the very attacks the card excludes.
- The card that removes the top of your deck face down and later looks at what it removed now looks at only its own cards. It read your whole removed-from-game pile, so it could take a card it never removed and turned every other face down card in there face up with it. Turning the rest face up also never reached your rival, and the cards you took never left their view of your removed pile.
- Cards that remove the top of your deck face up now show your rival the card that actually left. They saw a different card out of your deck, and then watched you play something else out of it.
- Two cards that print a facing on the move itself now use it. An attack that adds itself to your card pool "face down" arrived face up, so it still counted as an attack there instead of becoming a blank card; and the one card that banks the top of your deck to your momentum "face up" banked it face down, hiding a card your rival is meant to see.
- "Build 1 card from your card pool face up or face down" now asks you which. It always built the card face up, so you never got the face down half: a blank foundation you can flip later to pay for something.
- "Both players build the top card of their deck face down" now builds your rival's card face down as well. Only your own half was face down, so a card meant to hand you both a blank foundation gave your rival a working one with all its abilities.
- Cards reading "while this card is ready in your stage" now stop paying out once you commit them. Five of them kept granting their bonus after you had already spent them on a check or an ability cost, so you got both halves of a choice the card prints.
- Building a card out of your hand now lights only the cards the effect names. Cards asking for a backup, or a foundation with a printed difficulty of 3 or less, lit your whole hand, and clicking one they did not name built a different card of the game's choosing.
- Treasure Chest's "your checks made for this card's abilities get +1" now only pays for its own check. The +1 went to whatever check you made next instead, so it could be spent on an attack or a block while the check it was printed for got nothing. A second Treasure Chest keeps its own bonus rather than sharing one.
- A card your rival removes from the game, or bounces to their momentum, now leaves the pile it was sitting in on your screen too. Cards that remove themselves once they reach the discard pile left a copy behind there, so their discard pile counted a card that was no longer in it.
- When your rival searches their deck and builds what they find, your screen now shows it where they put it. A card they built face up showed on your board face down, a card built face down showed up in their hand rather than their stage, and a card they pulled out of their discard or removed pile did not move on your board at all: it sat in the pile while they played it from their stage.
- A card that pays off "if that check was made to play an attack" now checks what the check was for. It used to give the +3 speed to whatever attack was in flight, so checking one to block handed the bonus to your rival's attack.
- A character whose Form reveals 5 cards from your hand now pays out only when those cards actually share a keyword, and it adds the second card to the top of your deck the way it is printed. The reward used to arrive no matter what you revealed, and only half of it arrived.
- A card asking for "2 or more keywords" now counts the keywords printed under the card name, not just the ones listed with its types. Most attacks print theirs only in that line, so they counted as having no keywords at all and the reward was never offered on them.
- "Choose a backup. That backup loses 4 stamina" now drains one of your own backups, and you pick which. With no owner printed, an instruction means your own cards, and the two cards printing it were reaching across to your rival's board instead. Cards that do print "a rival backup" are unchanged. A backup destroyed this way also disappears on your rival's screen now, rather than only on yours.

- Cards that pay off "after this card leaves your card pool during the Combat Phase" now do so when something actually clears them mid-combat. They only ever fired during the End Phase, which is after the Combat Phase has ended, so sixteen cards went off at the one moment their own text rules out and never at the one it names. "Clear 1 card from your card pool" announced nothing at all, so nothing could answer it.

- A card reading "after this card leaves your card pool", with no phase printed, now pays off either way it goes: cleared mid-combat, or swept up at the end of the turn.

- Reviewing a card at the start of your turn did not show up on your rival's board: their copy of your hand kept the card you had discarded, and their copy of your discard pile never received it. The review is now mirrored when you press the button, so backing out with Ready still leaves nothing behind.

- Being told to commit foundations, by Stun or by any other card, no longer leaves the enhance glow on cards you cannot click. While the commit is open the board lights exactly the cards it will take, and the glow comes back when it closes.

- A prompt asking you to discard a card now lights the cards it will accept. "Discard 1 attack" lit nothing at all, so the only way to tell which cards paid it was to read them.

- A card you may play out of your discard or removed pile now glows there. The permission worked if you happened to click the card, but nothing on the board said it was available, and cards in the removed pile could never glow at all.

- Answers your rival sent about a card they revealed, peeked at, ordered or chose could be left lying around when the matching effect did not happen on your side, and the next card to ask a similar question would quietly use the old answer instead of asking. Twelve kinds of answer were affected; all of them are now dropped at the start of each attack, as the rest already were.

- If anything went wrong while a block was being played, the attacking player was never told how the block ended and both players sat waiting on each other for the rest of the game. The block now resolves as no block, and play carries on.

- Four crashes that could stop a game mid-turn are fixed: cancelling a prompt that asked you to commit foundations, a keyword question asked about a card that was not there, and two of the same shape on the watching player's side.

- "This attack's speed and damage cannot be reduced below printed" only ever protected the damage, so one card did nothing at all and two others protected half of what they say. Two more cards that name damage alone were quietly protecting their speed as well, and no longer are.

- Three cards make blocking an attack cost your rival something extra, a revealed block or a discarded card, and charged nothing. One of them made the attacker discard their own card instead. Both are fixed: the defender pays, and cannot block at all if they cannot.

- Three cards make your rival pay an extra foundation to play abilities during an attack, and charged nothing at all. The cost is now taken, and only on the abilities each card names.

- One card gives health back to "that player" after a player loses health, and always gave it to whoever played it. It now goes to the player who actually lost the health.

- One card offers "ready this character or remove the top card of a player's deck" and only ever readied the character: the second half of the choice was never offered. Both halves are now on the menu, and removing asks whose deck.

- Five cards that search your deck print "reveal it", and nothing was ever
  shown: your rival saw only that you had searched. The card found is now
  flashed to both players, as is the card name you announce when a search
  asks you to name one.

- Two cards that search your deck and put the card back on top were not
  shuffling it at all, so the rest of your deck stayed in an order you
  already knew. The shuffle now happens before the card is placed, which is
  the order the cards print.

- Seven cards that do something extra "the second time you have played this
  ability this turn" were counting the wrong ability. Playing anything else in
  between, including a card your rival plays in response, answered the question
  instead, so the card skipped the drawback it prints for repeating.

- "Build 1 Ally asset or Ally backup from your card pool. If you did and it is
  your turn, draw 1 card" now asks both questions. The draw used to happen
  whether or not there was anything to build, and on your rival's turn too.

- "Each player adds 1 foundation from their stage to their hand" now lets your
  rival choose which of their own foundations to take back. The attacker was
  picking it for them.

- "Your rival adds 1 foundation from their stage to their hand" now lets them
  choose it, for the same reason.

- "Flip 1 of your rival's foundations" is your pick again. Your rival was
  being asked which of their own foundations to turn over.

- "Choose a player. That player loses 1 health, draws 1 card, and discards 1
  random card" now does all three, to the player you chose. Only the discard
  happened before, and it always came out of your own hand.

### 2026-09-21

- Eight cards that reward you for playing their own Powerful, EX or Deflect
  ability paid out when the card was played instead. The reward arrived
  before the ability's cost had been paid, and arrived whether you ever
  played the ability or not.

- Sacrificing a face down foundation now only pays out when the card turned
  over is the one the ability asks for. The draw and the build were running
  whatever the sacrifice revealed.

- A bonus to your next check now waits for the check it names. Twelve cards
  buff the next check to play an attack, a block, a Shift attack or a card
  from your removed pile, and every one of them paid out on whatever check
  came next instead, including a foundation.

- A card searched out of your deck goes where the card says. Two cards spelled
  their destination in a way the reader missed: one put its named card in your
  hand instead of your discard pile, and the other searched your whole deck
  rather than for the name it prints, then put the wrong card in your momentum.

- Fixed: some attacks announced a Blitz step that then had nothing to
  offer. An attack whose blitz only readies a card opened the step even
  with nothing left to ready, which reads as the ability having fired.

- Fixed: cards that read the top of a discard pile looked at the bottom
  of it instead. Ten abilities asking whether the top card is an attack,
  or is named Tornado, were answered about the oldest card in the pile.

- Fixed: "add the top card of your rival's discard pile to their card
  pool" moved the card only on your rival's screen, and moved the wrong
  card.

- Fixed: readying one copy of a foundation marked every copy of it. With
  two of the same card in your stage, "ready 1 foundation that hasn't
  been readied this Combat Phase" refused the second for something the
  first did. 31 abilities print that restriction.

- Fixed: unflipping one copy of a foundation marked every copy of it,
  so "unflip 1 card in your stage that has not been unflipped this
  turn" refused the second copy for something the first did.

- Fixed: the discard you take for playing no form did not count as your
  rival discarding a card from their hand, so yyhdt-192's abilities
  stayed unplayable after it.

- Fixed: nor did a card you discarded out of your rival's revealed hand,
  or one they pitched from hand to pay a cost. Every way a card leaves
  their hand for their discard pile now counts.

- Fixed: a rival backup that ran out of stamina went into your discard pile
  and stayed listed in their stage, so the same backup could keep blocking
  and your pile grew a card you never owned. It also counted as you
  sacrificing a card.

- Fixed: "this attack gets +1 damage for each card that has been destroyed
  this turn" counted only your own foundations, so Luna Ring could not see
  the rival asset its own first ability had just destroyed.

- Fixed: "if a rival foundation was destroyed this turn" asked whether YOU
  had destroyed a foundation, of either owner. It now asks who owned the
  card that was destroyed.

- Fixed: a backup reduced to 0 stamina was recorded as a card you sacrificed
  rather than one that was destroyed, so "only playable if 2 or more rival
  cards have been destroyed this Combat Phase" never counted a backup.

- Fixed: "each rival backup loses 2 stamina" and "a rival backup loses 3
  stamina" changed nothing on your rival's own screen, so their backups
  stayed at full stamina there and any that died went on standing.

- Fixed: "build 1 momentum card face down" showed the card in your rival's
  stage on their screen while it was still counted in their momentum, so the
  same card was in two places at once.

- Fixed: "move all Wall counters from this card to another card" left the
  counters showing on the old card on your rival's screen.

- Fixed: destroying one of your own foundations to pay for an ability was
  recorded as a sacrifice. Cards answering "after a foundation is destroyed"
  stayed asleep, "if you have destroyed a foundation this turn" said no, and
  cards that trigger on a sacrifice woke up when nothing had been sacrificed.

- Fixed: spending a Power or Heat token opened the "after a foundation is
  destroyed" window, offering free triggers for something that never happened.

- Fixed: an Enhance reading "if your attack deals damage to a character" was
  asked before the attack had swung, so it always answered no and the reward it
  guards never paid out. Same for "if your non-Throw attack deals damage".

- Fixed: "if it deals damage to a Titan backup, that backup loses 1 stamina"
  asked you to choose a backup, and asked whenever the attack dealt damage to
  anything at all. It now drains the backup the attack actually hit, and only
  when that backup is a Titan.

- Fixed: "if this attack is not completely blocked" was asked before anyone had
  the chance to block, and an attack nobody has blocked is not completely
  blocked, so the reward was handed over every time.

- Fixed: "if this is the only card in your card pool" was answered by whether
  the attack had been blocked, which during your own Enhance Step is always no.
  All four cards printing it paid out regardless of how full your pool was.

- "Commit 1 rival asset" committed one of their foundations instead. Six cards
  reach past the foundations when they commit, and five of them name what they
  reach: an asset, a backup, or either of those or a foundation. The printed
  word is carried through now and the commit takes the card it names.

- Four more commits that name what they take. "Commit 1 rival foundation or
  asset" stopped reading at the first word, "your rival commits 1 asset or
  backup" took a foundation instead, and "your rival commits 1 foundation and
  asset" is two cards rather than one.

- Sealing, freezing, flipping and sacrificing now reach the card they name too.
  "Seal 1 rival asset", "flip 1 rival asset or foundation" and "sacrifice 1
  foundation or asset" all took a foundation whatever they printed.

- "Commit and freeze" and "commit and seal" now freeze or seal the card they
  just committed. They used to ask for a second, separate card, which let you
  freeze one you had not committed and lost the printed type a second time.

- "Commit and flip 1 rival foundation" flips the card it committed too.

- "After your rival plays an attack, remove it from the game" removes their
  attack. It used to remove the card the ability was printed on.

- "You may flip 1 foundation and ready it" readies the foundation it flipped
  rather than the attack that said so.

- "A player of your choice gains N health or a backup of your choice gains M
  stamina" reads both printed numbers instead of using one for both.

- "While there are N or more different keywords among cards in your card pool" now
  gates the bonus it is printed with. Only the "If there are" wording was read.

- "If there are N or more different keywords among the cards milled this way" is
  read at all now, so the offer that follows it is made only when it is earned.

- "Your attack with 1 or fewer abilities gets +2 speed and +2 damage" counts the
  abilities on the attack in flight. Every attack used to collect the bonus.

- "Your rival commits 1 card in their stage with no abilities" reaches the whole
  stage and skips the cards that print something. A keyword is an ability here.

- "Add 1 card with "Dagger" in its name not named "Dagger, Dagger, Dagger"" no
  longer hands back the card that said so. The exclusion was dropped.

- "After you block with a foundation not named "Size Specialist", build it" no
  longer fires when Size Specialist is the foundation that blocked.

- "Add 1 other card from your stage to the top of your deck" no longer sends
  away the card that committed itself to say it. "Add 1 other middle attack from
  your card pool to your momentum" no longer moves the attack in flight.

- "You may clear 1 other attack from your card pool" to pay an Echo cost no
  longer lets the attack pay for itself, and the offer is only made when the
  pool holds another attack that could cover it.

- "If you have another action or Spell in your card pool, this attack gains
  Stun: 2" no longer counts the attack asking, which is itself a Spell sitting
  in that pool. The Stun was unconditional.

- "After your rival plays an attack that shares a keyword with another attack in
  their card pool, skip this attack's Enhance Step" reads what the attack has to
  share. The response used to fire on any attack they played.

- A response that asks a rival to attack another backup is no longer offered by
  the backup the attack is already aimed at, where redirecting earned nothing
  and still cost a commit.

- Abilities whose trigger names the card it happened to can no longer be played
  when that card is the one excluded. Nineteen cards were offered, charged their
  cost and then did nothing.

- Setting the Standard's "the speed and damage values of each other attack you
  play this turn become 4" now applies to every attack you play after it. It
  used to be spent on the first one.

- Stomp of the Female Titan doubles a bonus once per time you play the response,
  up to the three it prints. The second and third plays used to buy nothing. It
  also no longer doubles a bonus the attack gave itself, which is not "another
  card's effect".

- Four more "up to N" effects are a ceiling rather than a demand: removing cards
  from a rival's discard pile, shuffling your discard pile into your deck,
  freezing foundations stunned during an attack and adding cards to the bottom
  of your deck. Each took the full count whenever the pile or stage held that
  many or fewer, so coming in under the printed number was never offered.

- "Add N cards from your discard pile to the bottom of your deck" no longer asks
  how many when the card does not print a ceiling. Asking made a flat instruction
  declinable.

- Six more cards reading "after you block an attack with this card" now check
  which card blocked. They fired off any block at all, so a foundation sitting in
  the stage could draw a card, slow the next attack or blank an attack it had
  taken no part in blocking. Two of them also answer only Throws, as printed.

- "Your rival removes 1 random card from their hand" no longer asks them to
  choose. The card they would least like to lose was the one they handed over.

- "Your rival draws 1 card and adds 1 random card from their hand to their card
  pool face down" now does both halves. The second clause shares its subject with
  the first, and only the draw was read.

- Cards reading "after you completely block an attack with this card" now check
  which card blocked. Ryu, Ken and their reprints could be played from hand off a
  block some other card made, and retaliate with a card that never blocked.

- "When you completely block with this card" no longer fires on a partial block.

- "After your attack is not completely blocked, build it face down committed" now
  reads the word "not". It used to fire after any attack resolved, including one
  that was completely blocked.

- "Freeze up to 2 foundations stunned during this attack" and "freeze 1 of them"
  now freeze only the foundations the attack's Stun ability committed. Both cards
  reached the whole rival stage instead, so either could freeze any foundation it
  liked whether Stun had touched it or not.

### 2026-09-20

- A stage stays one row however much you build on it. Past ten foundations the
  cards overlap the way your hand fans, so none of them is drawn smaller, all of
  them stay on the board, and you can still drag them into any order you like.

- Fixed: Loot Box never handed back the card it built. "That card" is the one
  it built, and it was read as the card that triggered the ability, which an
  Enhance has none of, so nothing came back at all. Named correctly, the card
  was then removed from the game at the end of the Combat Phase instead of
  being added to your hand.

- Fixed: Shoot the Moss left both players waiting on each other and neither able
  to go on. When a card puts the choice of option in your rival's hands, they
  are now asked for it directly.

- Fixed: the Pass button stayed live while you were being offered the chance to
  cancel an ability. Pressing it moved the window on in the middle of a play
  that had not finished, so it is held until the offer has been answered.

- Fixed: three cards that look at the top few cards of a deck and put them back
  in any order asked you to do it twice, and offered a single card the second
  time instead of the number the card prints.

- Fixed: healing could carry a character above the health printed on their card.
  Printed health is a maximum, so healing now stops there however it reaches
  them.

- Fixed: Moment of Normalcy prints a choice between returning an attack to its
  printed speed or its printed damage, and was taking both. Nine other cards
  that name only one of the two were throwing away the other as well.

- Fixed: Devil Jin put himself into the card pool. The card to add is the
  attack you just checked, and your rival's screen showed the board correctly
  while yours did not. His check bonus was also counted twice.

- Fixed: Heihachi Mishima's attacks never gained the Powerful 4 he prints,
  so the momentum you can spend on it was never offered.

- Fixed: a card could sit face up in your rival's hand, readable from across
  the board, if it reached the hand already face up.

- Fixed: In the Lead, and anything else that moves a card from your momentum
  to your hand, handed you a card instead of letting you pick one. Which card
  leaves your momentum is yours to choose.

- Fixed: card art looked pixelated on smaller screens. Cards are drawn much
  smaller than their artwork, and the artwork was being sampled at full size
  however small the card was on screen.

- Fixed: a card played out of your removed pile vanished from the board. It
  reached your card pool, but was still counted as being in your hand as
  well, so the next card you drew carried it off with the rest of the hand.

- Fixed: being told to sacrifice or destroy a foundation lit up foundations
  lying in your discard pile as if you could give one of those up. Only the
  cards in the stage the instruction is aimed at are offered now.

- Fixed: a deck carrying a second character started you as whichever of the two
  was listed first. The wrong one was seated, your hand was dealt up to its
  size rather than your own character's, and the character you meant to play
  was shuffled into the deck.

- Fixed: a bonus or penalty waiting on your next check stayed armed until you
  made one, however many turns later that was. It now expires with the turn it
  was played in.

- Fixed: "add a Wall counter to a card in your stage" never asked which card.
  The counter went onto the card printing the instruction, so played off an
  attack it landed outside your stage altogether and that same card's bonus
  for counters in your stage could never see it. "Remove a Wall counter from
  a rival card" took one off a card of your own instead of theirs.

- Fixed: the offer to flip a Spell card in your card pool to pay for a keyword
  ability was labelled with the engine's own shorthand instead of saying what
  it would cost you.

- Fixed: while the game was asking you to confirm a play, the banner still
  said you were waiting on your opponent and the Ready button relabelled
  itself to Pass over the top of the question. A question on screen now
  counts as what it is, one waiting on you.

- Fixed: "your rival freezes 1 committed foundation" froze whichever of their
  foundations the game happened to find first, and counted one that was
  already frozen, so the card often did nothing at all. Your rival now
  chooses which one, and the freeze shows up on both boards.

- Fixed: an ability printed "Twice per Enhance Step" was not limited at
  all. It could answer every card milled during the step rather than the
  first two, handing out its damage bonus again and again.

- Fixed: a blitz offering to clear an attack from your card pool instead of
  spending momentum on its Echo cost went ahead and cleared one anyway. It
  threw the card away and gave no discount. It now offers the choice.

- Fixed: a card that hands your rival a block bonus for the turn took it
  back the moment the next attack began. It now lasts the turn it was
  printed for.

- Fixed: War Hammer Titan had you choose an attack from your discard pile and
  pay health equal to its check value, then added itself to your hand rather
  than the card you chose and paid for.

- Fixed: a card added to your hand out of your discard pile was left lying in
  the pile as well, so it was in two places at once. Strategic Maneuver did
  this every time you took the chosen card.

- Fixed: Next-Gen Model and Crossing Enemy Lines both print "choose a
  player", and neither one asked. They landed on whoever played them, so
  Next-Gen Model milled you 2 and Crossing Enemy Lines aimed its own check
  modifier at you.

- Fixed: Resurrected Titans could only ever search out a backup. It prints "1
  backup or Shift attack card", and the Shift attack half was never offered.

- Fixed: an instruction naming a keyword missed every card printing that keyword
  in its stat line rather than its type list. Offensive to Retake Wall Maria and
  Unit Commander added no Ranged, Weapon or Ally card they revealed and then
  discarded it with the rest, Mikasa Ackerman and Rafa, The Exo-Soldier cleared
  no Weapon card from your card pool, and Hwoarang cleared no Kick card.

- Fixed: a price naming a keyword could not be paid with half the cards that
  print it. Chun-Li, Martial Arts Master and Inherited Will charge a Kick card,
  and any Kick card printing the keyword in its stat line rather than its type
  list was refused, along with the Weapon, Spell, Ally, XP, Tech and Vestige
  prices that Mikasa Ackerman, Caleb Widogast and Carnival Barker charge.

- Fixed: a gate asking what is in a zone missed every card printing the keyword
  in its stat line rather than its type list. Furious Charge checks your card
  pool for a Weapon before gaining Weapon itself and never found one, and
  Deadly Pitch, Toss Aside, Youko Form, Stars in Her Eyes, Throw Servant and
  Kazama-Style Traditional Martial Arts went the same way on Ranged, Titan,
  Ally, Charge and Punch. Descendant of Hizuru likewise let a Weapon card block
  for full value instead of setting the block modifier to +0.

- Fixed: more gates naming a keyword could not see it when the card printed it
  in its stat line. Eren's Message, The Best Detectives and The Manipulations of
  Zeke Yeager never saw the Titan, Spell or Ranged card they milled, and Juri
  Han, Thrill-Seeker, Misguided Big Brother, Beast Titan, Scouting Skirmish,
  Determined Seeker and Quiet Contemplation went the same way asking whether the
  attack was a Kick, Ally, Shift, Throw or Weapon. Mikasa Ackerman, Protective
  Friend missed a revealed Weapon, Evoking the Wielders missed your Vestige
  foundations, and Overwhelming Size misread a Titan rival character.

- Fixed: a card handing its keywords to your attack handed over nothing when it
  printed them in its stat line. Devour Your Power, Inventor's Creation and
  Okey Dokey! all granted an empty list, and the menu asking which keyword to
  strip off a rival attack was empty for the same reason.

- Fixed: a card that does not count toward progressive difficulty to play one
  type of card stopped counting toward every play that turn. Spirit Unicorns
  excuses itself only to play Spell cards, and once its first attack went in
  nothing else in your pool counted either, so the rest of the turn came out
  cheaper than it should have been.

- Fixed: Enough of This did nothing at all. It prints that it does not count
  toward progressive difficulty to play foundations, and nothing anywhere
  recorded that, so every foundation you played after it cost as much as if
  the card were still counting against you.

- Fixed: Hiei, Dragon Within let your rival answer the first block after all.
  The card says they may not play responses to playing the first block, and
  nothing anywhere read that sentence, so they still got a window to act in
  before Hiei sealed the block away.

- Fixed: a face down card in your stage counted as a copy of the card on its
  hidden front. Laying one beside a Unique foundation sacrificed the foundation
  for a duplicate neither player had been shown, and a face down card could be
  the one taken.

- Fixed: Mark Tyner never let you keep the 2 copies of a Unique foundation it
  protects. The protection was looked for in your stage, and the card granting
  it is a character, so the pair was sacrificed anyway.

- Fixed: a card that promises your next Weapon attack extra damage handed it to
  whatever you played next, and that attack spent it, so the Weapon attack it was
  meant for arrived with nothing. Your opponent's screen also showed less damage
  than you dealt, because only your own client had banked the bonus.

- Fixed: the card that has each player add a card from their discard pile to
  their card pool turned YOUR card face down as well as your opponent's, once
  you had played a Roman Cancel ability. It only says their card goes face
  down, and a face down card in the pool is a blank card, so the card you had
  just added was no longer one you could play.

- Fixed: twelve cards that name which card they want found nothing to choose
  from, so the ability was spent and nothing happened. "Add 1 face down card
  from your card pool to your hand", "add the top card of your discard pile to
  your hand", "seal 1 non-attack card in your card pool", "add 1 action from
  your discard pile to your hand", "add 1 other card from your card pool to
  your hand", and the card that puts one of your opponent's stage cards into
  their card pool face down.

- Fixed: every ability whose price is "Mill N" then asks about what it milled
  counted nothing, because paying the price kept no record of the cards it took.
  "Add 1 Fury or Titan card milled this way to your momentum" found nothing to
  add, and "+1 speed for each attack milled this way" added no speed. Psycho
  Power, which mills to pay for itself and then uses the effect matching that
  card's check, paid its price and did nothing at all. Your opponent's screen
  now learns which card the price milled, so both of you see the same result.

- Fixed: Electric Wind God Fist cannot be flipped while it is the fourth copy
  or fewer you have played this turn, and it read how many copies you had
  played instead of which copy it was. Playing a fifth copy left the first four
  open to being flipped, and a copy still lying in your card pool from an
  earlier turn could never be flipped at all.

- Fixed: Titan Swarm's discount for a second attempt never arrived. The card
  gets -3 difficulty when it is the second time you have tried to play one
  that turn, and every check was made at full difficulty instead. The
  discount now applies at the attempt, which is the moment the card names.

- Fixed: the foundation that lets you use its Deflect from your stage bought
  nothing. The ability was paid for and Deflect was still refused for not
  being in your hand. It is now playable from the stage, for the one attack
  the card gives it and for the one ability the card names.

- Fixed: Combined Firepower could never be played out of your discard pile.
  It says you may try to play it during an attack once you have removed a
  card to pay a cost, and the permission was being recorded somewhere that
  nothing deciding a play would ever look.

- Fixed: a hand size increase printed "this turn" was thrown away at the start
  of the Combat Phase, half way through the turn it was bought for. Short-Lived
  Promotion and Researching the Answer both grant one before your Draw Step, and
  every card that reads a hand size afterwards, "Big Sister" of 1-B and Alisa
  Bosconovitch among them, was answering with the number that had not been
  increased. It now lasts the turn out.

- Fixed: Massive Size counted the cards in your hand rather than your hand size,
  which are different numbers on almost every turn. It was worth the most with
  an empty hand, when the card means it to be worth the least.

- Fixed: Plate of the Dawnmartyr's health floor and G Corp Soldier's offer to
  take the hit on its own stamina never did anything about a rival's effect,
  which is the only thing either card protects against. Both were asked of the
  wrong player, and both got in the way of prices you had chosen to pay
  instead.

- Fixed: every effect that moved health applied it twice, on both boards. The
  peer watching a rival's play re-runs their effects, and a health change
  already reports itself over the wire, so "your rival loses 2 health" took 4
  from the character it named. Both boards were wrong by the same amount, so
  nothing ever looked out of step.

- Fixed: a Response printed for "2 or more" was offered after one. Two cards
  count what you just did, sacrificing foundations and spending momentum, and
  the count was dropped when their text was read, so each was playable at half
  the price it prints.

- Fixed: a Response printed for "after you check" was offered to whoever's turn it was. Blocking makes a check, and the player who blocks is the one whose turn it is not, so your own block check never offered these cards while the rival's block check on your turn answered as though you had made it. Twenty cards read the check that way, including the seven arena cards that print "when you play or check this card".

- Fixed: an attack that reads "after 1 or more foundations are destroyed or 1 or more cards are discarded" was refused the discard it sets up itself. The clause names no player, but it was answered by whoever's turn it was, so a rival discarding during your own Combat Phase, which is what the card's Blitz makes them do, did not count.

- Fixed: Rising Uppercut, Exilio and Countersnipe charged a Drive to try to
  play themselves back as an attack after completely blocking one, and then
  only printed a message. They now make the check and attack for real, on your
  rival's turn, and your rival gets to block it.

- Changed: the phase strip is drawn bigger on a small screen. Its chips were
  set at the board's own scale, so on the window a 1366x768 laptop opens they
  reached the screen at 8 pixels and the "REPEATS" caption at 5. The strip now
  grows to the same half-of-authored floor the battle log is held to, and
  stops at the band between the two card pools so it never covers a card.

- Fixed: pressing End Turn while the game was asking you to pick a card
  advanced the phase anyway. Paying a cost, and discarding for the no-form
  penalty, are both answered by clicking a card rather than a button, so End
  Turn kept the label it already had and stayed live, and pressing it moved
  the turn on underneath an ability that was still waiting to be paid for.
  The button is dead while a prompt is open now, and Cancel is still on the
  other one.

- Fixed: Mai Fighting Style did nothing when your rival readied foundations.
  It prints "built or readied" and only the build half was ever answered, so
  half of what the card offers could never happen.

- Fixed: cards reading "after you flip a foundation" answered every commit
  instead. A check commits foundations several times a turn, so four cards paid
  out constantly, and the ten that print a commit answered your flips.

- Fixed: "after this card is unflipped" listened to the flip and commit window,
  which carries neither an unflip nor the card it was about. Turning a card face
  up now opens its own moment.

- Fixed: "after you commit this card to pay a cost" and its relatives answered
  for every copy you had in play instead of the card the moment was about, so
  the wrong card readied itself, or went to momentum for a cost it never paid.

- Fixed: "after this card is committed during the Enhance Step" left the Enhance
  Step out, and answered a commit made at any point in the turn.

- Fixed: a card printing "Only playable if ..." on a form could be played
  whether or not the condition held. Godzilla, King of the Monsters destroyed every foundation
  in both stages without the ten foundations it asks for, and seven more cards
  ignored the line they print.

- Fixed: a sealed card still offered its form ability. A sealed card has no
  abilities until the end of the turn, forms included, and the same went for a
  card whose name had been silenced for the turn.

- Fixed: starting a form from your stage and then backing out of paying for
  it used up your Combat Phase's first form. A card printing "First Form" was
  refused for the rest of the phase, and your rival's game disagreed about
  whether it had been played at all.

### 2026-09-19

- Game codes are easier to read out to somebody: they no longer use characters
  that look like each other, and a code typed in lower case still joins.

- The client can be told to open as if it were on a smaller screen, with
  `--screen=1366x768`, to see how the game reads on one.

- Fixed: M. Bison, Writhing Evil, Unlimited Psycho Crusher and JP, Regal
  Businessman never noticed the cards you milled, so what they print was never
  offered to you.

- Fixed: Nothing But a Squawking Crow did nothing when it was milled during the
  Enhance Step.

- Fixed: Unlikely Duo did nothing when cards left your card pool during the
  Combat Phase.

- Fixed: Master of Taekwondo never came up before the Block Step, so it never
  returned the attack to its printed speed.

- Fixed: Fresh Cut Grass, Positive Reinforcement did nothing after a rival's
  unblocked attack resolved.

- Fixed: The Joker did nothing after you failed a check.

- Fixed: Jacob Johnson did nothing when you blocked with an action card.

- Fixed: Fast and with Finesse still counted toward progressive difficulty when
  you played Kick attacks.

- Fixed: Bison . . . Who Is That? and Assume the Worst did nothing when they
  were committed to pay a Drive cost.

- Fixed: Cammy, Killer Bee did nothing after you paid a Drive cost.

- Fixed: Unlikely Duo could not be committed as a foundation to pay a Drive
  cost, and offered to commit itself for nothing instead.

- Fixed: Mysterious Murderer could not remove itself to pay a Drive cost.

- Fixed: Juri Han, Thrill-Seeker could not sacrifice 2 foundations in place of
  a Drive cost.

- Fixed: Back to Ordinary never fired. It waited on you playing your third card
  of the turn, a moment the game was not reading.

- Fixed: Departure could not be played from your discard pile. The Form it
  prints there offered nothing.

- Fixed: Sekkan Kick did not hold either player to 1 enhance ability during
  its Enhance Step.

- Fixed: Front for My Operation cancelled a keyword ability and then took no
  health for it, whatever that ability was rated.

- Fixed: Knee Press Nightmare did nothing with the cards it milled. Its Blitz
  now offers to pay this attack's Echo cost with cards from your hand when
  the mill turns over an attack.

- Fixed: the Enhance Step reported no enhance to play while a card in your
  stage plainly printed one. An ability that reads "If something, effect" is
  playable whether or not the If holds, and only a card printed "Only playable
  if" is held back now.

- Fixed: playing an enhance was answered with "no enhance to play", on your
  screen and your rival's, because priority came back with the cost already
  spent.

- Fixed: a Shift attack built transformed showed its attack side on your
  rival's board, while your own showed the face you built. Both boards now
  build the same face.

- Fixed: Juri Han, Thrill-Seeker prints two bonuses, one for a Kick attack and
  one for any attack once you have played three attacks this turn. The Kick
  half was read as a rule about the whole enhance, so it could only ever be
  played on a Kick and the second bonus was out of reach.

- Fixed: Noble, Strong, and Beautiful discarded a card and drew one, but never gave the discarded
  card back when your rival had ten or more foundations. That whole half of
  the card was being ignored.

- Fixed: cards that search your deck for a copy of a card they name offered
  you the whole deck to pick from instead. "Cart Titan, Finale", "Vex'ahlia,
  Resourceful Hunter", "Torbalan" and "JP, Regal Businessman" now find only
  the card they print.

- Fixed: JP, Regal Businessman and Superfly Stomp also put their own card
  into your discard pile alongside the card they searched for.

- Fixed: a prompt with a short question, like the one asking whether to
  concede, was drawn as tall as the whole window. A menu is now only as tall as
  what it holds, and still scrolls once it holds more than fits on screen.

- Cards you rest the cursor on are blown up to the size the art was drawn at,
  so the rules text is readable on a laptop screen rather than shrinking along
  with the board. Nothing changes on a screen big enough to show the board at
  full size.

- Questions the game asks you, like choosing which ability to play, are drawn
  at their own size rather than the board's, so the options are readable on a
  laptop screen. A screen big enough to show the board at full size sees them
  exactly as before.

- When the game asks you to pick a card, the cards are drawn bigger on a small
  screen so you can tell them apart. A search that turns up more cards than fit
  still scrolls exactly as it did.

- Looking through your discard or removed pile draws the cards bigger on a
  small screen, spending width the grid was leaving empty. Deep piles scroll as
  they did, and a screen big enough to show the board at full size is unchanged.

- The battle log is drawn larger on a small screen so its lines can be read. It
  grows across rather than down, so it covers no more of the board from top to
  bottom than it did and the game behind it stays in view.

- Fixed: the battle log left out health that your rival's cards took or gave,
  so the total printed beside a line could disagree with the health showing on
  the board.

- Fixed: "sacrifice this foundation" left the card standing in your stage, so
  the price printed on it was never actually paid.

- Fixed: a card offering to be sacrificed in place of spending momentum on an
  EX ability never made the offer, so you always paid the momentum instead.

- Fixed: three cards that give your attacks a bonus for the rest of the turn
  handed out nothing at all, including one whose bonus is meant to reach every
  attack except the card printing it.

- Fixed: borrowing an enhance ability from a card you removed took every
  enhance ability sitting in your removed pile instead of the one you chose,
  and the loan never ended.

- Fixed: an attack meant to inherit the keywords printed on the card you
  removed to pay for it inherited nothing.

- Fixed: Arrogant Smirk never gave you back a Fury attack. It asks whether you
  have lost health during the Enhance Step, and nothing kept track of health
  lost over anything shorter than a whole turn, so the question was answered by
  asking whether you had spent health to pay a price instead. Its own price is
  a sacrifice, so the answer was always no.

- Fixed: Darkness Dragon Prowess granted no Stun at all. The rating it gives is
  the amount of health lost during the Enhance Step, and it was reading the
  health that paying for the ability had just cost. The ability is free, so that
  was always none.

- Fixed: For All Our Sakes sealed nothing at all, and the card it let off
  progressive difficulty was itself rather than the card you sealed. It
  prints one instruction across two sentences, and each sentence was being
  read on its own.

- Fixed: Arrow Kick gave its speed bonus to a committed character and its
  damage bonus to nobody at all. The card prints two bonuses in one sentence,
  one for a ready character and one for a committed one, and only the second
  of the two conditions was being read.

### 2026-09-18

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

- Fixed: on the watching side, the copies a card your rival had played this
  turn were counted off your own record. Panzer Unit Mounted Fire, Electric
  Wind God Fist, Titan Swarm and Mechanical Legion, and the attacks that lose
  their damage or get sealed on a repeated copy, answered the wrong player, so
  the two screens disagreed about the attack.

- Fixed: a card that gives your attacks +1 speed or +2 damage for the turn was
  not applied to your attacks on your rival's screen, so the two boards read
  different numbers and any response that asks how hard the attack hits was
  offered on one screen only. The half about your own attacks now reaches the
  other screen, like the half that slows your rival already did.

- Fixed: a card in your card pool that slows your rival's attacks did not
  slow them on your own screen. Your rival saw the attack at the lower speed
  and you saw it at its printed one, so the block offer, and anything else
  that reads how fast the attack is, answered differently on the two boards.

- Fixed: an attack that prints "this attack cannot be partially blocked" was
  still blocked in half. The line was read only on the attacking player's
  side, and it is the blocking player's side that works out whether a block
  was partial. The same attack printing that line as an Enhance always worked.

- Fixed: an attack that buffs itself from its own printed text, such as +3
  damage while you have a face down card in your card pool, showed the bonus
  only on the attacking player's screen.

- Fixed: Onyankopon's first enhance also stopped your rival from using their
  own Onyankopon for the turn. The line that closes the name binds only the
  player who played it.

- Fixed: a card whose abilities unlock once your rival has discarded from their
  hand stayed locked when you were the one who made them discard.

- Fixed: when your rival played a card that stops face down cards counting
  toward progressive difficulty, the discount was handed to you instead of to
  them.

- Fixed: a foundation your rival readied no longer counts as readied for
  your own copy of the same card, so "ready 1 foundation that has not been
  readied this Combat Phase" can still reach it.

- Fixed: an attack printing a Deadlock Blitz announced the Blitz step even when
  your rival was nowhere near deadlock. The step opened with nothing in it that
  you could play.

- Fixed: an action card printing "First Form" offered that ability as your
  second or later form of a Combat Phase. It is only playable as the first one
  you play.

- Fixed: replaying an attack as a form, and playing one out of your discard
  pile, fired every form ability printed on the card for free. The stamina and
  other costs went unpaid, and gates like "[Discard Pile]" were ignored.

### 2026-09-17

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

### 2026-09-16

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

### 2026-09-15

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

### 2026-09-14

- Fixed: Destoroyah Emerges and Standing Tall were not sacrificed on your
  rival's screen when you paid for them with Power tokens. They went on seeing
  the card sitting on your board after you had spent it.

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

### 2026-09-13

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

### 2026-09-08

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

### 2026-09-07

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

### 2026-09-06

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

### 2026-09-05

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

### 2026-09-04

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

### 2026-09-03

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

### 2026-09-01

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

### 2026-08-27

- Fixed: an attack printed "this attack cannot be blocked" could still be
  blocked. Burning Fist is the card in Standard that says it.

- Fixed: a bonus granted to the next attack you play went to the attack being
  resolved instead, or to no attack at all. Unexpected Reunion's sacrificed
  foundation bought nothing.

- Fixed: the same misreading on seven more cards. Some lost the bonus outright,
  some gave away only half of it.

### 2026-08-26

- Board is landscape and 4:3. Cards are drawn larger and the window opens at the
  board's own shape, so there are no black bars.

- Card pool sits above your own stage. Both run the full width of the board.

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

## 0.0.1

### 2026-08-26

- First alpha build.
