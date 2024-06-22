# Preface
Before I start, I will have to first confess why I made Crop Rotation(CR).

I played Luck be a landlord(LBAL) a lot previously, but one issue I had with LBAL is the inability to pivot, and how the game is usually fixed after the third payment.
By fixed I don't mean that the game is beaten. By fixed I meant that the decision is mostly made for you regarding what build you will have and what symbols/items to pick.
I didn't know why that was the case, but I know I wanted something different, so I made CR.

The core premise of CR was "LBAL but with more diversity in build and more strategic depth", and at least for me, I think I achieved it with CR.

This is not to say that LBAL is a bad game, just that the game wasn't set out to be what I want.
It is meant as a fun slot machine game, and happens to be an engine builder.
After playing LBAL, I know I want an engine builder even tho I didn't use the term back then.
So I decided to craft one from scratch.

There will be a lot of references to LBAL, Balatro and CR and why I did the things I did.
Do not take my analysis of LBAL or any other games as a criticism of them.
It is a critical analysis of them including CR.

I am also still not 100% happy with CR, but for the most part, to solve these issues requires big changes which might create new problems.
Most of the other games probably also have their problems because of how they were designed.
They probably can't be changed without changing the whole game.

# Introduction
This is written shortly after the launch of CR 1.3 patch as an analysis of the game and the genre of engine builder.

First of all, these are mostly my thoughts and understandings, feel free to agree or disagree.
The post will use a lot of examples from CR, so some understanding of the game is probably needed.

This is also a very long post, so brace yourself.

# Engine builder
Before talking about engine builder, we first need to define engine builder, or specifically, the kind that Crop Rotation belongs to.

0. Run Based
1. Engine builder revolve around building a "engine" using random parts given to you.
2. The core system is automatic, and requires minimum tactical decision.
3. The game usually revolve around scaling against a production curve.

## Games in the space
Let's first list down the games that are in the space. This is not a comprehensive list, but ones that I know of.

- [Luck be a landlord](https://store.steampowered.com/app/1404850/Luck_be_a_Landlord/)
- [Farm Keeper](https://store.steampowered.com/app/2458940/Farm_Keeper/)
- [Crop Rotation](https://store.steampowered.com/app/2348090/Crop_Rotation/)
- [Lucky Mayor](https://store.steampowered.com/app/2659970/Lucky_Mayor/)
- [Balatro](https://store.steampowered.com/app/2379780/Balatro/)
- [Bingle Bingle](https://store.steampowered.com/app/2789810/Bingle_Bingle/)
- [Cat God Ranch](https://store.steampowered.com/app/2797340/Cat_God_Ranch/)
- [Ballionaire](https://store.steampowered.com/app/2667120/Ballionaire/)
- [Dungeons and Degenerate Gamblers](https://store.steampowered.com/app/2400510/Dungeons__Degenerate_Gamblers/)

LBAL should be the most recent one that started the space. If there is an earlier one please let me know.

## Run Based
The game is run based (or many like to call it roguelike).

## Random Parts
There needs to be some type of randomness to the parts that is given to you.
If you always have the same parts, the game will feel more like a puzzle, or an automation game like Factorio.

## Automated System
The simuation / core system should be automated or almost automated.

Most deckbuilder are technically also engine builder.
However, these games usually have a heavy focus on the tactical aspect, which makes the overall engine-building aspect less significant than a pure engine builder.

Some games may feel like there are tactical decisions, e.g. Balatro and Farm Keeper but they are also part of pure engine builder.
This comes from an observation that despite having tactical decision, the decision made for each round is more or less the same.

For example, once you set up your engine in Balatro, you will be doing the same hand(s) for each stake, i.e. Flush/Straight/TwoPair.
Similarly for Farm Keeper, once you set up your farm, you will be clicking the farm in the same order, mostly.

On the other hand, in a tactical deckbuilder like Slay the Spire(STS), the enemies you face in a fight changes how you play your hand.

This is why despite having tactical decision in Balatro or Farm Keeper, I still put it in this space.
This also applies to many of the other games listed above.

## Scaling against a production curve
There is a section on this below, so I shall not repeat here.

## Wrap up for criteria
Engine builder is also a very big genre, which includes deckbuilders, single player autobattlers, and many in between.

For the purpose of this post, I want to focus my learnings on a specific type of engine builder, but some ideas probably translate to other type of engine builder.
For the sake of this post, I will call this type of engine builder "Production Engine Builder" instead of "Pure Engine builder" since pure may accidentally implies that it is better.

I feel that production engine builders was previously unexplored compared to other types of engine builders, but with Balatro popularity, I suspect more devs will explore this space more even though they might not know that they are making one.

# Design Thoughts
These are some concepts/ideas/analysis that I learnt from Crop Rotation.

## Building Engine vs Problem Solving
The first core concept is Engine Building versus Problem Solving.

One type of complains/suggestions that I got for CR early on is how boring the difficulty settings are, i.e. increasing rating only result in an increased in payment.
I agree with this idea initially but I couldn't find a solution then (in 1.2).

When I was working on 1.3, I experimented with the idea of having a curse difficulty system like Slice and Dice / SpellRogue.
I realised immediately that it changes the game way too much and I didn't like it.
After introspecting, I realised a core concept for production engine builder.

> Production Engine builder should revolve around learning how to build better engine, and not solve harder or different problems.

Using CR as an example, most of the difficulty changes revolve around giving you more limited set of "parts", like less cards, less resources and force you to make the best of the situation.
This may feel like problem solving but they are different from curses that reduce seed harvest price or harder seasonal effects etc.

Another side effect of this realisation is the understanding of the role of "Contract" in CR.
In some games, contract would have serve as the goal and have the gold serve as a resource.
This changes the game from a engine building to problem solving.

We can then compare this to deckbuilder and single player autobattlers.
Deckbuilders and autobattlers are also engine builders, but they revolve around building an engine to solve different types of problems rather than just growing the output of the engine.
For these type of engine builders, a curse system will work better because it creates more problems for the players to solve or restricts how they solve existing problems.

For a production engine builder, the core should be scaling engine against a Production Curve.

## Production Curve
As mentioned previously the goal of production engine builder is always the production.

In LBAL, it is determine by how much goal your slot machine can generate per spin.
In CR, it is how much gold you can generate per day.
In Balatro, it is how much value you can make per hand per round.

However, it could also be possible to make something that do not have a curve but instead just have a high score or a final payment.

A good example is [Roll](https://store.steampowered.com/app/1585910/Roll/).
It is almost a production engine builder, but without the curve, it end up feeling like a high score or an incremental game.

When I first created CR, the payment per week was copied from LBAL without knowing why.
After working on it, I realised that without the weekly payment, the game would not be an engine builder.

> A production engine builder must be balanced against a production curve.

A production curve also serve as a counter force to greed based strategy.

In CR, it is really easy to greed by aggressively rerolling at lower rating to get what you want.
However, at higher rating, you rarely have enough money to reroll that much early on.
You are forced to keep up with the production curve, forcing you to make harder decisions.

In Balatro, there is an incentive to save money for interests, but saving too much means you don't have enough joker to clear the stake.

Knowing when to greed and scale is an important skill for players when playing production engine builder.

Also because we have a production curve, we can now balance the game and its difficulty using it.

## Soft Synergy vs Hard Synergy.
Crop types was introduced to Crop Rotation very early on in development.
This idea mainly came from the autobattlers genre.
By having crops of the same crop types, they form set bonuses.

Having set bonuses allow crops to interact with other crops that shares a type with it.
Although this was the original intention of adding crop types, having crop types now allow me to have cards interact with crop types instead of specific cards.

For example, if I want a card to interact with all fruits, I do not need to list all the fruits that it interacts with, and instead can just interact with the fruit type.
This is different from LBAL, where interactions are named specifically to the cards that they interact with.

Both CR and LBAL are a form of soft synergy.
In CR case, cards are connected to multiple cards via types.
In LBAL, cards are just connected to multiple cards directly.

In my opinion, CR's tag based synergy system are softer than LBAL, and it allows for banning of cards (more on this later).

If I am a good article writer, I would put a graphic here.
But I am not, so imagine CR graph where cards are connected to types then to cards, and LBAL's graph where symbols are connected to other symbols directly.

LBAL's graph in this case would be more complex, but would also be more interesting.
However, such graph means that if you remove some symbols, a part of the graph will break and may not connect to another part of the graph, i.e. some cards might end up being totally disconnected.
On the other hand, CR's graph is more boring because everything just connect to crop types, removing cards will not break the graph as long as I ensure that types are never fully removed.

Both have their own uses, but if you want to vary the starting condition of each run, a tag based approach like CR will be better.

In additional to this, adding new cards to CR became easier, since I do not need to update the old cards to name the new cards.

## Pivoting and Local maximum
Another issue I have with LBAL is the lack of opportunity to pivot when you acquire a new item.
You can't acquire parts without adding them to the engine and you can't remove them easily.
This was the same for early versions of CR, and I didn't like it.

I added a storage area because of this, and make the engine part fully configurable without the need to acquire or use any resources; like reroll token.
This allows players to freely acquire cards without putting it in the engine, and provide a mechanism to do big pivots.

> By having the ability to store parts until you have all that you need to pivot, you can do big pivot.

The reason why you want to enable big pivot is because of local maximum.

Most of the time, the engine that a player make might get stuck in a local maximum where 2 or 3 parts need to be changed to make the engine more efficient, and changing 1 at a time make the engine loses a lot of the efficiency until the pivot is completed.

For example, in Crop Rotation, you might want to change from 7/3 fruit/vegetable to 7/3 vegetable/fruit to pivot due to a new card you acquired, but having 5 of each is worse than 7/3 of either.
This means that the player need to change out 3-4 crops in a single day to change the build.
By providing a storage area, this allows the player to hold on to a few cards before pivoting.

To put it in a more technical term,

> Players need to have the ability to do big pivot to get out of local maximum.

In CR, I also lean into pivoting by providing the ability to trade in cards for the same type of cards at specific points in the game.
There are 3 trade-ins which allows you to trade in crops for other crops, animals for other animals and permits for other permits.
This also provide a mechanism to get out of local maximum by allowing players to trade in lower performing cards for their build for those that helps them more.

Does the solution of having a storage area work for other games ?
Will Balatro benefit from a Joker storage area ?
What about LBAL with a symbol storage ?

I do think this will definitely allow for more pivots and adapatation, but whether or not it fits the design of the game and what the designer want, that's a different question.

## Constraints
Constraints are fun ways to force the player to adapt and change.

Although I mentioned that the game is about engine building and not problem solving previously, this does not means we can't give constraints or problems to the players.
We can introduce them as part of engine building and they should not be the goal but a constraints that makes the better engine harder to build.

Using CR as example.

CR has passive cards that provide values to the player.
However, most of them restrict how you can build your deck before you can get the benefits.

For example, the dual flavour permits requires you to have 2 active flavour set bonus.
This usually means that it will lock 4 crops in your deck.
At the max level, to fully utilise the effect, you have to lock in at least half of your deck.

Another example is Rat and Cat.
Rat only increase value of common crops, and Cat only increase value of uncommons and rares.
At max level, they have a constraint that you cannot have crops on the farm that they dislike, i.e. uncommon and rare for Rat, and common for Cat.

These cards add constraints to your deck, and CR fundamentally revolves around stacking as many of them as you can.
Each of these constraints also form their own synergy; i.e. some constraints are easier to complete with some but harder with others.

### Distribution contributions vs hard constraints
There are 2 types of constraints - distribution and hard.

Using Rat and Cat for example, the constraints are distribution constraints at tier 1/2/3 and hard constraints at t4.

Distribution constraints means the effect efficiency may vary based on the distribution of cards in your deck.
For example, to maximise the efficiency of Rat, you want to have all common crops, but you still get the benefit when half of your crops are commons, just less efficient.

Another example is the support permit in CR, which increases the value of crops if they are adjacent to a Support crop.
To maximise the effect, you want to then increase the distribution of your support crops, but you don't need all to be support crop.

Compare this to a hard constraint like Pig, which requires you to have fixed number of active set bonuses before it is activated.
It is binary, either you have it, or you don't.

Both types of constraints are useful and should be used.

## Build Diversity and Identity
One thing I realised in CR is that it lacks build identity, specifically there isn't an easy way to know what a "build" is.

Loosely speaking, I tend to see builds in CR as which 2-3 passive cards I build around and get to max level.
Then with these passive cards, I then figure out which crops to use.
There are many ways to combine passive cards and different combination of crops to activate them.
Combine with the fact that cards are banned and removed, each "build" despite being the same build, will end up looking different.

Let's use a build that I like to use, Pig + Sheep.

Both Pig and Sheep gives a 2x multiplier at tier 4, and if you combine them, you get a 4x multiplier.
Because of this, figuring out a way to combine them is one of the easiest way to get high rating.

Pig's constraints is that you need to have 12 active set bonuses at tier 4.
Sheep's constraints requires you to have 16 unique crops.

Because PigSheep build is one of the easiest 4x multiplier, I have use it a few times and they always end up looking different, and because of this, the build doesn't have an identity like that of other deckbuilders.
In most deckbuilders, when going for a certain type of build, you usually have a few key cards to get.
In the case of CR, the key card is the build itself.

There are ways to almost make 2 passive cards work, except for cases where they restrict each other like Rat and Cat (as intended).
Combine this with the huge number of crops that works with each other, there is really a diverse number of builds in CR.

However, because of this, CR also have a very low build identity.

I am beginning to wonder if when a game's build has a lot of identity, does that game's also loses a lot of build diversity.

Lack of build identity may also sometimes feels like anything can work in the game and the game lack strategy, and at the same time feels like the game doesn't have "builds".
I definitely got a few of those in CR's reviews.

## Build Pathing
When I play CR, because of the harsh production curve in higher rating, I sometimes have to take non-related cards to just fill it in.
When entering mid game, I find myself wanting to change them to fit my build.
This might be because that I did not get the cards I want, or I picked up another cards that allow me to pivot.

This doesn't happen in lower rating or when you are just trying to do specific build.
This happen specifically when there is a pressure to produce more in the short term while working towards a long term build.

This also happens in autobattlers, when you pick up a specific unit to handle a specific problem, while working towards other units that will synergise better long term.

Another good analogy if you play mahjong, is how you pick up pieces so you have a better wait, while at the same time give yourself opportunity to make bigger hands.

The concept of "build pathing" is the idea of how one build can be path into another.

Because the identity of build is not strong in CR, I don't think I have explore this space enough.
I do think it is worth mentioning it as a concept to be explored in other games.

## Randomness and Variability
The ability to pivot also creates the ability to force a build.
If a specific build can be forced every game, then the game would become a sandbox game.

The first step is to provide randomness in the parts that the player is given to build their engine.
In CR, this is mainly done by the drafting of cards.
However, this is not enough and since we have gold based rerolls, it is still possible to force builds if you really want.

We can solve this by adding variance to the start of each run.

### Variance for each run
As mentioned previously, CR uses a tag based system for synergy, which is different from LBAL.
This allows me to have different set of cards each run and it will not directly feel bad if a card is removed.
Compare this to LBAL, if bee and sun is removed, flower immediately becomes pointless.

By changing up cards that is available to the player, we can make each run feels different.
This forces the player to adapt to what is available unless the player restart games until they get the cards they want.

However, this has a drawback and it exists in CR.

By having a ban system and a reroll system like CR, each run becomes a puzzle at the start of the game.
The player might then attempt to solve for which builds are the best, and try to work towards them.
If they fails to get it, it might feel that it is due to RNG.

This forces the analysis to the be front-loaded, and if you choose to play the game this way, it will be overwhelming.
It also goes against the flow that works best for engine builder, i.e. make the best use of the pieces given to you.

I did thought about having a fog of war system in CR to solve this issue.
The key idea is that cards available to the player is not known at the start of the game until they discover it in draft.
I really like this idea, but it overly complicates the game, and changes how the game is played.
Even though I don't usually plan for my full build at the start of each run, knowing what is available changes what I pick in each draft.
By adding a fog of war, it makes drafting extremely random at the start, which I didn't like.

## Length of game
The length of a run often get ignored when talking about the design and balance of a game, because it feels like some games can be cut in half and still functionally be the same game.
However, I now disagree with this and I will explain why.

Let's start by looking at CR.
One thing I added post launch is the turbo mode.
Turbo mode comes from some feedbacks and my own experience that a run might be too long.

I therefore made turbo mode, which is 1 week per season and I provided the players with more drafts to allow max tier of cards to still be able to be completed.

The thing that turbo mode removes from the game are

1. The need to pivot
2. The ability to greed

When you have a shorter run, pivoting becomes something that rarely happens.
In CR, this is because you are given a lot of things at the start, and those usually tend to solidify your build very early on.
Secondly, because the production curve is tighter and shorter, big pivot will usually cost you the run.

Greeding as a strategy also became weaker.
Greeding is the idea of sacrificing short term play for long term benefits.
If the games are shorter, your greeding strategy needs to be stronger.

In CR, there is a specific card that is affected by turbo mode the most.
Dog provides you an animal usually after every week.
This means that a dog will provide you with 7 animals in a normal game, while only providing 3 in a turbo game.
Cards that provide draft instead of value are also greed cards and are definitely weaker in turbo mode.

Let's look at another example for greed strategy.

In Balatro, you earn interests every $5 and cap at $25.
This means that you should only start spending money after $25 and not drop below it.
This usually happens at around 2nd or 3rd stake.
If the game ends at stake 4 instead of 8, greeding only provides 1 stake worth of value.
If Balatro is a 4 stake game, the interest will have to cap earlier or at smaller interval.

So the point here is not that a game needs to be long or short, but the length of a run affects the balance of the game.

In my opinion, this is one of the important thing to figure out early on.
This is also one of the reason why changing CR to a 4 week game requires a big overhaul instead of just adding turbo mode.
Turbo mode might be one the worst thing I added to the game(I know right ?) and is still in the game right now.

Related to this, this is why adding endless mode is also a bad idea.
Adding endless mode makes balancing hard because players might want the endless mode to be balanced when it is rarely balanced around it.
If you try to balance endless mode for engine builder, greed strategy becomes the only viable strategy.

# Problem of the genre

## Comparing it to incremental games
One potential problem of the genre might be how close it is to an incremental game.
Many people might view this as a 'numbers go up' game if they play it at a difficulty curve that is below the balanced curve, or might view it as too random when playing in a difficulty curve above the balanced curve.

I have mentioned an example previously with [Roll](https://store.steampowered.com/app/1585910/Roll/).

The issues lies in the lack of a production curve, or a weak one that allows for greed strategy.

In CR, rating 0 plays like an incremental game.
In LBAL, Floor 0 plays like a slot machine.
Only in Balatro that the first difficulty is reasonably hard.

People might even ask for an endless mode, which I fundamentally hates and refuses to add to CR till this day.
I might change my mind (probably not) and add it to CR later.
To me, this will change a good engine builder to a bad incremental game.

## Comparing it to deckbuilder / tactical engine builder
Many people might play a production engine builder and compare it to deckbuilder and comment on the lack of tactical decision and problems to solve.
This is the reason why I decided to write this post in the first place and hopefully some people can understand this genre a bit more.

> Tactical engine builder and Production engine builder are similar in the way the game is constructed, but different in the way the goals & problems are presented.

We should not ask a production engine builder to have more problems or tactical decisions the same way we should not ask a tactical engine builder to automate their problem solving (aka combats).

# Conclusion
I set out to make CR in a very specific way with a specific vision in mind.
I am also not saying that these ideas fit into all games.
It is what I learnt from CR and what I wanted from a game like this.

Is Crop Rotation perfect ?
No, not really. There are still flaws and definitely cards that I want to change.
However, I can no longer play LBAL, and probably also can't play Balatro as much as I want, because they both remind me of CR and I like CR's systems more.
I can also keep improving CR whenever I have new inspirations or shape it to what I want.

If you are a player of CR, I hope you learn something regarding why CR is the way it is.
If you are a dev and wants to make an engine builder, I hope you had learnt something from this.
Reach out if you have an engine builder to sell me, or if you want feedback.

# Other posts
This is also part of a 3 parts posts from making CR.

- Journey of CR and the various prototypes (Coming Soon)
- Specific balance and design of CR (Coming Soon)
