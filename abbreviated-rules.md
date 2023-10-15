# Uno: Chaos Edition
alt title: who's turn is it anyway?

Here is a summary of all the rules required to play Uno: Chaos Edition.
## Basic rules
Every player begins the game with 7 cards. All other cards are placed face down in a pile called the draw pile. The top card is then flipped over to create the discard pile. The effect of the revealed card is applied as if the player who flipped the card played it. If the revealed card is wild, any card is allowed to be played next.
Play initially proceeds in a clockwise direction, with each player playing one card. The card played must either match the color, or symbol of the card on the discard pile, with the exception of wild cards, which can be played no matter what card is on the discard pile.
If a player does not have a card that can be played, they must draw cards from the draw pile until they do, and play that card.
## Cards
There are two types of cards: number cards and power cards. Power cards are any cards that have a non trivial effect. 0, 1, 2, 7 and 8 are treated as power cards for reasons you will see later. The cards effect the game as follows:
- 3, 4, and 5: Turn moves to the next player; no effect.
- 6, and 9: Same as the other number cards, however 6 and 9 are treated as identical. (They look close enough, don't they?)
- Skip: The next players turn is skipped.
- Reverse: the turn order is reversed, clockwise to counter clockwise and vice-versa
- +2: The next player must draw 2 cards and skip their turn
- 0: Each player must give their cards to the next player in the turn order
- 7: The player choses another and they must trade hands.
- Wild: The player who placed the card can chose one of the 4 colors on the card, and the next player can only play a card of that color or another wild card.
- Wild +4: Functions exactly the same as a wild card, however the next player must pick up 4 cards and pass their turn.
- 2: The card on top of the draw pile is flipped to create an additional discard pile. The effect of the revealed card is applied as if the player who played the 2 played it, however if it is a wild card then the color is determined by the next player to play. Players may chose to play on either pile when playing cards.
- 1: The discard pile it is placed on, is moved on top of another discard pile of the players choice. If there is only one discard pile, the card has no effect, however it is still treated as a power card.
- 8: Functions like a normal number card, however you can jump in with them as if they were a power card. Also used by the Crazy 8's rule described below.

## Challenging
If a player plays a wild +4, another player can chose to challenge  it.
- If the player who played it had another valid card they could have played, the +4 is applied to them instead. Otherwise it is applied to the challenging player.
- If the last card played on a stack was a +4 wild, any player can still challenge it, unless another card is placed on top.
	- +4 is added to the stack.
	- If the player had another plus card they could have played then the stack is pointed at them
	- Otherwise it is pointed at whoever challenged
## Jumping in
If a player has a number card that is the same number and color as the one currently on the discard pile, they can "jump in" and play it even if it is not their turn. 
- Play then proceeds as if it was their turn and the player after them in the turn order plays next.
- For power cards, only the symbol has to match. 
	- For example if there is a blue skip on the discard pile, a player can jump in with a yellow skip. 
- This operation is defined similarly for plus cards, however this is much more complicated and the rules for it are defined under "stacking".
#### Edge cases
- Stacking 7's: If the trade has not yet occurred from the previous 7, it is canceled. Then either way the player to play the new 7 gets to trade.
- If there is an ongoing trade, a not involved player can jump in on a 7 on a different discard pile.
	- This creates an independent trade which is treated separately.
	- If a new trade targets a player already involved in a trade, the old trade is canceled by the new one.
- stacking 2's: new piles are only revealed 
- If a player is unable to play and has to pick up until they can, a player can jump in during this time
	- The player who was picking up can not return the cards they picked up but they don't have to pick up anymore
- If you are forced to pick up cards, you cannot jump in until someone else plays a card
## Stacking
Jumping in is much more complicated for plus cards
- Plus cards are all treated as the same for the purposes of jumping in. +4 cards can be jumped in on with +2's and so on.
- When a plus card is played on top of another plus card, the values are added together, and this is called a stack.
- The player who's turn it is after the last plus card is played must pick up the total amount of cards from the stack. This player also skips their turn.
- Once a player has picked up all the cards required by the stack, the stack is considered dead
	- This card is still able to be jumped in on, however the stack created does not include it, or any cards below it.
#### Edge cases
- If a new discard pile is created with a plus card, this card can be stacked and jumped in on
	- This includes the very start of the game
	- If the cards from this plus card are picked up, this stack now counts as dead
- If a there is an ongoing stack, a player who is not currently receiving a stack can chose to jump in on another discard pile that has a plus card
	- This creates an additional stack, which is treated completely independently from the others
- If a player has only drawn some of the cards, the stack is still alive and other players can jump in. 
	- The player does not get to return the picked up cards if this happens, but does not have to draw more.
	- The amount of cards drawn is subtracted from the total of the stack
	- When this happens the player who had to draw is also now able to jump in on the stack again, however they cannot while they are drawing cards.
### Immutable stacks
- This is created by any card that is not a plus card that incites drawing cards.
- These stacks cannot be changed in value, however they can still be deflected.
- When one is created, it is created as an independent stack to any other stack going on.
- This applies even when the stack is created on top of another stack.
	- It does not effect the target of the underlying stack, only creates a new stack relative to the person who played the card
## Deflection
- If a player is faced with a stack and they do not have any more plus cards they can play, there is still a way out if they have other power cards. 
- If the player has a power card that matches the color of the top card of the stack they can play it to have the effect defined below. 
- If their are multiple draw piles, and the player has a deflection card that is valid to be played on any of them, they can play the card on that pile.
	- If it is not the players turn, they can only play on the stack that is targeting them, unless there is another discard pile that they can jump in on.
- If the last card on the stack was wild, the color is decided by whoever played the card. 
- This applies to stacks of plus cards, 7's or 0's.
- Below are the effects of every useable card on the different types of stacks:

Plus cards
- Skip: The stack is passed to the next player in the turn order.
- Reverse: The turn order is reversed and the stack is passed to the next person in the turn order.
- 7: The stack is put on the player of your choice.
- 2: Half of the stack is given to the next person. This creates two stacks that function independently. Does not apply to immutable stacks.
- 1: Can only be played if the player is receiving a stack that was at some point half of a previous stack. This causes the portion of the stack that you are receiving to go back to the person that created this fragment. Does not apply to immutable stacks.
- 0: All ongoing stacks are passed to the next person in the turn order, relative to each stack.

7's:
- If someone is attempting to swap cards with you, you can deflect it with the following cards:
- Skip: they are forced to attempt trading with the next person in the turn order
- Reverse: turn order is reversed and they are forced to attempt trading with the next person in the turn order
- 7: Cancels the trade and allows you to initiate a trade
- 0: all ongoing trades are moved one spot further in the turn order. This includes both people involved in the trade

0's
- Before the shift occurs any player can play on of the following cards as long as it follows the rules previously.
- Skip: Makes the shift amount increase by one
- Reverse: reverses the shift direction
- 0: Adds one to the shift count
- 2: Doubles the shift count
- 1: Halves the shift count
#### Edge cases
- If the deflection card is placed directly on a stack, it effects that stack specifically
- If the deflection card is placed on any other discard pile, it directly effects the stack targeting the player
- If multiple stacks face one player, deflecting will effect the stack they played on
	- If they play on a free discard pile, it effects all stacks facing them
	- In this case, if there is an immutable stack facing them, 2's will split up the normal stacks and immutable stacks. The player choses which type is passed to the next player.

## Crazy 8's
- If four 8 cards are played on top of each other in the same pile, it invokes this rule.
- Every player who did not play an 8 on the pile must draw 8 cards.
	- Subject to deflection rules for regular stacking, however the draw count cannot be increased.
	- A player can avoid having to pick up by playing another 8 on the pile. However this only cancels the specific 8 cards that they were meant to draw, not any that were deflected onto them.
## Win condition
#### The "Uno" rule
- When a player plays a card such that they only have one card remaining, they must say "Uno".
- If they fail to do this, any other player can call them out on it, forcing the "Uno" player to pick up 4 cards
	- However the challenging player must wait until at least the next player has played a card to call it out
- If the challenging player calls them out but they actually did say "Uno" already, the challenging player must draw 4 instead.
- If they have not said "Uno", no one has challenged them on it, and they play their last card, they can again be challenged. 
	- The player would then have to return the card they played to their hand, and draw 4 more.
	- However if the player has already said "Uno", the challenging player must pick up 4 cards
- If the player currently being challenged is also facing a stack, instead of drawing 4 cards, +4 is added to the stack and the stack is pointed at whoever failed the challenge
#### Edge cases
- If the "Uno" player gains more cards, they can no longer be challenged.
-  If another player trades hand with you while you only have one card, you are no longer subject to being challenged. The player who stole your hand now has until the next card is played before they can also be challenged.
- If after winning a round you draw one card, you have until the first player plays before you can be called out
	- If a player trades with you while you have one card, this also applies to them.
	- This effect is lost once they have more than 1 card in their hand
#### Winning the game
Points:
- Each player starts the game with a number of "points" equal to the number of cards they start with.
	- Usually every player starts with 7 points, because they start with 7 cards.

Playing the last card in your hand:
- If you play the last card in your hand, no player can play a card except for jumping in
- Card effects are still processed as normal, and jumping in is also unaffected.
- Once all card effects, stacks, etc. (Including 7's and 0's, even if they were the last card played of someone's hand) have been resolved, and no more players jump in, all players with no cards in their hand are subject to the "round won" rules listed below.

Round won:
- If a player or players have won the round, they each subtract 1 from their point score.
- If a player reaches 0 points, they are the winner, and the game is over.
- All players with 0 cards now draw a number of cards equal to their current point score.
	- If you only have 1 point, the cards you draw from the "Uno" rule double, as well as the cards drawn from a failed challenge against you
- Once all players have drawn their cards, play resumes, starting with the next player in the turn order after the last player to play a card


#todo uno flip (word generator)
- cards
- stacking
- deflection
- convergence
#todo turn order multiplier????
