# Preface
I played a lot of "Luck be a landlord" (LBAL) in the past.
One issue I had with LBAL is the lack of strategic depth and how the game generally feels fixed after the third payment.
By fixed, I meant that the decision of what symbols/items to pick after the third payment is usually made for you.
I know I wanted something different, and that was the reason why I made Crop Rotation(CR).

The core premise of CR was "LBAL with more build diversity and more strategic depth".
I feel that I have achieved it with CR, at least for me.

This is not to say that LBAL is a bad game, just that the game wasn't what I wanted.
It is meant as a fun slot machine game, but happens to be a Production Engine Builder.

So I decided to craft one(Production Engine Builder) from scratch.

There will be a lot of references to many games including LBAL, Balatro and CR.
Do not take my analysis of them as a criticism.
It is just a critical analysis of the games.

I am still not 100% happy with CR.
However, to solve its issues, it would probably require me to make big changes which might create new problems.
Most of the other games mentioned probably also have their problems because of how they were designed.
They probably can't be changed without changing the whole game.

# Introduction
I have learnt a lot about what I call "Production Engine Builder" from making CR.
This post is an attempt to document all the learnings, while using CR (and some other games) as an example.
With the success of Balatro, many devs would likely be making games in this genre even though they might not know it.
The goal here is then to share my learnings, so that perhaps someone making those games might read this and learn something from it.

This post is also a way for me to dump my knowledge and move on so I can start making my next game.

# Production Engine Builder
CR is considered by many as Deckbuilder and Autobattler.
However, in my opinion, CR falls into a different category which I name "Production Engine Builder".

Deckbuilders, Production Engine Builders and Autobattlers fall into the category of Engine Builders.
Additionally, Deckbuilders fall under another category which I name "Tactical Engine Builders".
Production Engine Builders and Autobattlers both fall under what I call "Automated Engine Builders", which is why many consider CR as Autobattler.

![Venn diagram](/venn.png)

Production Engine Builder has 2 key characteristics that differentiate it from Deckbuilders and Autobattlers.

Firstly, Production Engine Builder's system is automated or almost automated, which is different from Deckbuilders.
Secondly, Production Engine Builder revolves around scaling output against a Production Curve, instead of solving problems.

I will touch on these 2 points more in detail below.

Here is a non-comprehensive list of games in the genre.

- [Luck be a landlord](https://store.steampowered.com/app/1404850/Luck_be_a_Landlord/)
- [Another Farm Roguelike](https://store.steampowered.com/app/2116850/Another_Farm_Roguelike/)
- [Terracards](https://store.steampowered.com/app/2464880/Terracards/)
- [Farm Keeper](https://store.steampowered.com/app/2458940/Farm_Keeper/)
- [Crop Rotation](https://store.steampowered.com/app/2348090/Crop_Rotation/)
- [Lucky Mayor](https://store.steampowered.com/app/2659970/Lucky_Mayor/)
- [Balatro](https://store.steampowered.com/app/2379780/Balatro/)
- [Bingle Bingle](https://store.steampowered.com/app/2789810/Bingle_Bingle/)
- [Cat God Ranch](https://store.steampowered.com/app/2797340/Cat_God_Ranch/)
- [Ballionaire](https://store.steampowered.com/app/2667120/Ballionaire/)
- [Dungeons and Degenerate Gamblers](https://store.steampowered.com/app/2400510/Dungeons__Degenerate_Gamblers/)

LBAL should be the most recent one that started the space.
If there is an earlier game, please let me know.

# Design Thoughts
Here are some learnings and concepts that I have learnt from Crop Rotation.
The sections can be read in any order, and they might reference each other.

## Building Engine vs Problem Solving
I mentioned previously that this is a key difference between Production Engine Builders and Tactical Engine Builders.

One type of complaint/suggestion that I got for CR is how boring the difficulty settings are.
For example, increasing ratings only resulted in an increase in payment.
I agreed with this idea but I couldn't find a solution back in version 1.2.

When I was working on 1.3, I experimented with the idea of having a curse difficulty system like Slice and Dice / SpellRogue.
I realised immediately that it changes the game way too much and I didn't like it.

After introspecting, I realised a core principle that applies to CR (and Production Engine Builder).

> Production Engine Builder revolves around building a better engine, and not solving harder or different problems.

We can compare this to Tactical Engine Builders.
They revolve around building an engine to solve different types of problems instead of scaling the output of the engine.
For these types of games, a curse system will work better because it creates more problems for the players to solve.

For a Production Engine Builder, the core should be building and scaling an engine against a Production Curve.

## Production Curve
In LBAL, you are required to pay the rent every X spins.
In CR, you are required to pay the loan every week.
In Balatro, you need to get a score for every stake.

This amount increases after every interval, hence forming a (production) curve.

However, it could also be possible to make an Engine Builder that does not have a curve, but instead just has a high score or a final payment at the end.

A good example is [Roll](https://store.steampowered.com/app/1585910/Roll/).
It is almost a Production Engine Builder, but without the curve, it ends up feeling like a high score or an incremental game.

When I first created CR, the payment cycle was copied from LBAL without knowing why.
After working on it, I realised that without the weekly payments, the game would not be a Production Engine Builder.

> A Production Engine Builder must be balanced against a Production Curve.

A Production Curve also serves as a counter force to greed based strategy.

In CR, it is really easy to greed by aggressively rerolling at lower ratings to get what you want.
However, at the higher ratings, you rarely have enough money to reroll that much early on.
You are forced to keep up with the Production Curve, forcing you to make harder decisions.

In Balatro, there is an incentive to save money for interests, but saving too much means you don't have enough joker to clear the stake.

Knowing when to greed and scale is an important skill for players when playing Production Engine Builders.

## Automated Decisions vs Tactical Decisions
Another key difference between Tactical Engine Builders and Production Engine Builders is the lack of tactical decisions.
Production Engine Builders are mostly automated.

Some games that have tactical decisions may also belong to Production Engine Builders.
This is because the decisions made for each round are more or less the same.

For example, Balatro is considered by many as a Deckbuilder.
However, once you have set up your engine in Balatro, you will be aiming for the same hand(s) for each stake, i.e. Flush/Straight/TwoPair.
Similarly in Farm Keeper, once you have set up your farm, you will be clicking the farm in the same order.

This is why, despite having tactical decisions in Balatro or Farm Keeper, I still classified them as Production Engine Builders.
This also applies to many of the other games listed above.

In comparison, in a Tactical Engine Builder like Slay the Spire(STS), the enemies you face in a fight changes how you play your hand.

## Soft Synergy vs Hard Synergy
Crop types were introduced to CR very early on in its development.
This idea mainly came from the Autobattlers genre.
By having crops of the same crop type, they form set bonuses.

Having set bonuses allows crops to have a soft synergy with other crops that share a type with it.
Although this was the original intention of adding crop types, it enables me to have the cards interact with crop types instead of specific cards.

For example, if I want a card to interact with all fruits, I do not need to list all the fruits that it interacts with.
Instead, I can just have them interact with the fruit type.
This is different from LBAL, where interactions are named specifically to the cards that they interact with.

Both CR and LBAL contain a form of soft synergy.
In CR, cards are connected to multiple cards via types.
In LBAL, cards are just connected to multiple cards directly.

We can visualise the connections of cards and symbols in CR and LBAL using these graphs.

![Graph](/graph.png)

LBAL's graph in this case would be more complex, but would also be more interesting.
However, such a graph means that if you remove some symbols, a part of the graph will break and be disconnected from the rest of the graph.

On the other hand, CR's graph looks less interesting because everything just connects to crop types.
However, removing cards will not break the graph as long as I ensure that types are never fully removed.
Adding new cards is also easier because of this.

In my opinion, CR's type based synergy system is softer than LBAL's, and it allows for banning of cards (see [Randomness](#randomness-and-variability) below).

## Pivoting and Local maximum
Another issue I had with LBAL is the lack of opportunity to pivot when you acquire a new item.
You can't acquire parts without adding them to the engine and you can't remove them easily.
This was the same for early versions of CR, and I didn't like it.

I then added a storage area because of this, and made the engine fully configurable without the need to introduce a new type of resource; e.g. reroll tokens or removal tokens.
This allows players to freely acquire cards without putting it in the engine, and provides a mechanism to do big pivots.

> By having the ability to store parts until you have all that you need to pivot, you allow for big pivots.

The reason why you want to enable big pivots is because of local maximum.

Most of the time, the engine that a player makes might get stuck in a local maximum.
In this case, usually 2 or 3 parts need to be changed to make the engine more efficient, and changing 1 part at a time makes the engine lose a lot of the efficiency until the pivot is completed.

For example, in CR, you might want to change from 7/3 fruit/vegetable to 7/3 vegetable/fruit due to a new card you acquired.
Because having 5 of each is worse than 7/3 of either, changing it 1 at a time loses efficiency.
This means that the player needs to change out 3-4 crops in a single day to change the build.
By providing a storage area, this allows the player to hold on to a few cards before fully pivoting.

To put it in a more technical term,

> Players need to have the ability to do big pivots to get out of local maximum.

In CR, I also lean into pivoting by providing the ability to trade in cards for the same type of cards at specific points in the game.

Does the solution of having a storage area work for other games?
Will Balatro benefit from a Joker storage area?
What about LBAL with symbol storage?

I do think this will definitely allow for more pivots and adaptation, but whether or not it fits the design of the game and what the designer wants, that's a different question.

## Constraints
Constraints are fun ways to force the player to adapt.

Although I mentioned that the game is about engine building and not problem solving, this does not mean we can't give constraints or problems to the players.
We can introduce them as part of engine building and they should not be the goal.

> Constraints are there to make the better engine harder to build.

Let's use CR as an example.

CR has passive cards that provide values to the player.
However, most of them restrict how you can build your deck before you can get the benefits.

For example, the dual flavour permits require you to have 2 active flavour set bonuses.
This usually means that it will restrict about 4 crops in your deck.
At the max level, to fully utilise the effect, you have to lock in at least half of your deck.

Another example is Rat and Cat.
Rats only increase the value of common crops, while Cats only increase the value of uncommons and rares.
At max level, they become a constraint that you cannot have crops on the farm that they dislike, i.e. uncommon and rare for Rat, and common for Cat.

These cards add constraints to your deck, and CR fundamentally revolves around stacking as many of them as you can.

### Distribution Constraints vs Strict Constraints
There are also 2 types of constraints in CR - distribution and strict.

Using Rat and Cat for example, the constraints are distribution constraints at tier 1/2/3 and strict constraints at tier 4.

Distribution constraint means the efficiency of the card may vary based on the distribution of cards in your deck.
For example, to maximise the efficiency of Rat, you want to have all common crops, but you still get the benefit when half of your crops are commons, just less efficient.

Another example is the "Support Permit" in CR, which increases the value of crops if they are adjacent to a Support crop.
To maximise the effect, you then want to increase the distribution of Support crops in your deck, but you don't need all of them to be Support crops.

Compare this to a strict constraint like Pig, which requires you to have a certain number of active set bonuses before it is activated.
It is binary, either you have it, or you don't.

Both types of constraints are useful and should be used.

## Randomness and Variability
The ability to pivot also creates the ability to force a build.
If a specific build can be forced every game, then the game would become a sandbox game or an incremental game.

The first step to solve this, is to provide randomness in the parts that the player is given to build their engine.

In CR, this is mainly done by the drafting of cards.
However, this is not enough and since we have gold based rerolls, it is still possible to force builds if you really want.

We can solve this by adding variance to the start of each run.

### Varied Start
As mentioned previously, CR uses a type based system for synergy, which is different from LBAL.
This allows me to have a different set of cards available each run, and not feel bad if specific cards are removed.
Compare this to LBAL, if "Bee" and "Sun" are both removed, "Flower" immediately becomes pointless.

By changing up cards that are available to the player each run, we can make each run feel different.
This forces the player to adapt to what is available.
The player can still restart games until they get the cards they want, but that's not within our control.

> By changing up cards that are available to the player each run, we can make each run feel different.

However, this has a drawback and it exists in CR.

By having a ban system and a reroll system like CR, each run becomes a puzzle at the start of the game.
The player might then attempt to solve for which builds are the best, and try to work towards them.
If they fail to get it, it might feel that it is due to RNG.

This forces the analysis to be front-loaded, and if you choose to play the game this way, it will be overwhelming.
It also goes against the flow that works best for an Engine Builder, i.e. make the best use of the pieces given to you.

A potential solution to this is to add an information fog of war.
The key idea here is, cards available to the player are not known at the start of the game until they discover them in draft.
I really like this idea, but it overly complicates the game, and changes how the game is played.
Even though I don't usually plan for my full build at the start of each run, knowing what is available changes what I pick in each draft.
By adding a fog of war, it makes drafting extremely random at the start, which I didn't like.

## Length of game
The length of a run often gets ignored when talking about the design and balance of a game.
This is because it feels like you could cut some games in half, and it will still functionally be the same game.
However, I now disagree with this and I will explain why.

Let's start by looking at CR.

There was some player feedback, and from my own experience playing, that a run is too long.
Therefore, I added a Turbo mode, which only has 1 week per season.

### Pivoting in a shorter game
Shorter runs remove the need to pivot.

When you have a shorter run, pivoting becomes something that rarely happens.
In CR, this is also because you are given a lot of cards at the start (in Turbo), and those usually tend to solidify your build very early on.
Thirdly, because the Production Curve is tighter and shorter, big pivots will usually cost you the run.

### Greeding in a shorter game
Shorter runs also remove the ability to greed.

Greeding as a strategy also becomes weaker.
Greeding is the idea of sacrificing short term play for long term benefits.
If the games are shorter, your greeding strategy needs to be stronger.

In CR, there is a specific card that is affected by Turbo mode the most.
Dog provides you an animal usually after every week.
This means that a Dog will provide you with 7 animals in a normal game, while only providing 3 in a turbo game.
Cards that provide draft instead of value are also greed cards and are weaker in Turbo mode.

Let's look at another example of greed strategy in another game.

In Balatro, you earn interest every $5 and it is capped at $25.
This means that you should only start spending money after $25 and not drop below it.
This usually happens at around 2nd or 3rd stake.
If the game ends at stake 4 instead of 8, greeding only provides 1 stake worth of value.
If Balatro is a 4 stake game, the interest will have to cap earlier or at a smaller interval.

### Summary
So the point here is not that a game needs to be short or long, but the length of a run affects the balance of the game.

In my opinion, this is one of the important things to figure out early on.
This is also one of the reasons why changing CR to a 4 week game requires a big overhaul, instead of just adding a Turbo mode.
Turbo mode might be one of the worst things I added to the game, and is still in the game right now.

Related to this, this is why adding endless mode is also a bad idea.
Adding endless mode makes balancing hard, because players might want the endless mode to be balanced when in reality, it is rarely balanced around it.
If you try to balance the endless mode for Engine Builders, greed strategy becomes the only viable strategy.

# Comparison to other genres

## Comparing it to incremental games
One potential problem of the genre might be how close it is to an incremental game.
Many people might view this as a 'numbers go up' game, if they play it at a difficulty that is below the balanced curve.
They might also view it as too random when playing on a difficulty above the balanced curve.

I have also mentioned an example previously with [Roll](https://store.steampowered.com/app/1585910/Roll/).

Without a Production Curve, or a weak one that allows for greed strategy, the game will feel and play like an incremental game.

In CR, rating 0 plays like an incremental game.
In LBAL, Floor 0 plays like a slot machine.
Only in Balatro that the first difficulty is reasonably hard.

People might even ask for an endless mode, which I fundamentally hate and refuse to add to CR till this day.
I might change my mind (probably not) and add it to CR later.
However, in my opinion, this will change a good Production Engine Builder to a bad incremental game.

> Adding endless mode to a production engine builder may change it from a good production engine builder to a bad incremental game.

## Comparing it to Deckbuilders / Tactical Engine Builders
Many people might play a Production Engine Builder and compare it to Deckbuilders, then comment on the lack of tactical decisions and problems to solve.
This is the reason why I decided to write this post in the first place, and hopefully people can understand this genre a bit more.

Tactical Engine Builder and Production Engine Builder are similar from the point of engine building.
However, they also differ in the goals that they give the players.

> Tactical Engine Builder and Production Engine Builder are similar in the way the game is constructed, but different in the way the goals & problems are presented.

We should not ask a Production Engine Builder to have more problems or tactical decisions, and we should not ask a Tactical Engine Builder to automate their problem solving.

# Conclusion
I set out to make CR in a very specific way with a specific vision in mind.
I am also not saying that these ideas fit into all games.
It is what I learnt from CR and what I wanted from a game like this.

Is Crop Rotation perfect ?
No, not really. There are still flaws and definitely cards that I want to change.
I will probably continue to improve on CR every year, because I still enjoy working and playing it.

If you are a player of CR, I hope I have explained why CR is the way it is.
If you are a dev and want to make an Engine Builder, I hope you find this analysis useful.
If you are making a Production Engine Builder, feel free to reach out.

# Other posts
This is also part of a 3 parts post mortem from making CR.

- Journey of CR and the various prototypes (Coming Soon)
- Specific balance and design of CR (Coming Soon)

