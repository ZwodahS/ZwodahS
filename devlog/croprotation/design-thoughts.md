# Preface
This doc is written for myself, despite being public. "you" in most cases refers to "future me" and not the reader "you", and sometimes "you" refers to the gamer.

Reading this before playing Crop Rotation or understanding the game will spoil the game and experience.

# Introduction
I kind of want to write down various design pillars for Crop Rotation, and how I think when designing new content for the game.
The goal of this doc is to write down my current understanding of the game so that you can use this as a reference to add content in the future.
I will try to write such that each section is self contained.

This is written as of Version 1.3 (June). Let's try to keep this updated when things changed.

# Balance and Baseline Values

## 1. Rating
Let's start with balance.
In 1.2, the game was balanced around 1k rating, i.e. a good player should be able to beat the game 100% of the time at 1000 rating.
In 1.3, this is moved to 1.5k due to many cards being buffed at T3/T4.

This is also balanced around rating mode and not turbo mode.

**Note** After playing quite a bit, it seems like even 2k is doable as of now. I think it might be possible to streak at 2.5k, and with some number changes to the mid game number, 3k might even be doable.

## 2. Passives(Animal/Permit) Baseline
The biggest problem I have with passive in 1.2 are multipliers.
Multipliers are hard to value because they are really strong.
If the passive card does not have a multiplier then it is really weak.

Let's compare 2 passives as example. Wet Permit vs Big Farm Permit.
They both scale similarly until T3, and when it hit T4, Big Farm Permit instantly out-scale Wet Permit.

This really make some permits less useful than those with multiplier.

Looking at the number, previously in 1.2, the balance point for these were [2/5/12/2x] for most of these passive.
At T4, the jump from 12 to 2x is too much. For non-2x passives, the balance point was [2/5/12/30].
Looking at this, it is obvious that non-2x passives are too weak.

After 1.2, I realised this problem and I know that finding the balance between multiplier and raw value needs to be done eventually.
These passive cards are now balanced around [2/6/18/60|2x].

Honestly, I am not sure if 60 is even enough to compete with 2x but most 2x has a lot more stricter requirement, so I think it is still fine.

## 3. Predicted/Expected Game flow
The game flow wasn't designed initially in pre1.1, but more of a discovered flow based on playing the game.

1. Fixing water needs to happen before summer.
2. First power spike should happen at start of week5 (first trade in) by getting first T4.
3. Second power spike should happen at start of week6 (second trade in) by getting second T4.
4. Deck should be completed by start of week6 with minimum changes moving forward (i.e. just upgrading).
5. Second T4 Passive by end of week 6 / early week 7.
6. Week 7 and 8 is a test to see if the build actually scale well into end game.
7. 3 T4 by end of game is normal, but sometimes 2 T4 + 3 T3 will suffice.

In 1.3 this becomes more interesting with the trade-in change.
Pre1.3, Trade-in are fixed, i.e. Animal at week5, Permit at week6, Crops at week7.
1.3 changed it such that you choose which one you get, which allow for first power up via permit instead of animal.

Pre1.3 always has issues with animal being stronger than permits because it was the first power spike.
Tradein for crop was also quite week being at week7.

With this change, power spike via crops is viable. Hitting T5 bomb rare like snapdragon and thyme is also another form of power spike.

## 4. Baseline Values
These values are what the game is designed around.

0. 1.5k / 2k rating
1. Having 14 Crops and 2 Tools in Deck.
2. Having full deck space by end of Week 4, full storage by end of week 5.
3. 12 Crops by week 3, 16 Crops by week 4, 20 Crops by week 5, 24 Crops by week 6 (4 rows of 6).
4. Focusing on maxing a value-generating croptype, at least in the early game. i.e. (Vegetable/Fruit/Herb/Flavours/Spatial).
5. Deck Cost should be around 120 by end game (with mutations).
6. Based on (5), you should generating around 120 Farm Water / day, and also expected to maintain 150 water at the start of each day.
7. Gaining around 2 crops per day by mid game (week3), excluding skip.
8. Completing 80-90% of all contracts before week 7, i.e. you should have around 35-38 passives/tools by start of week 7.
9. Expect mostly Tier 3 crops by the end of the game, with some T4 and 1 or 2 T5.

# Key Design Pillars

## 1. Constraint Builds.
This is the key way that the game is designed now (1.1+), but not the way it was created initially (pre 1.1).

The key idea is that passive cards provide values but create constraints on how you build your deck.
The bigger the constraint, the bigger the rewards.

Let's use 3 cards as example to showcase this.

Small Farm Permit requires you to have less than [22/20/18/16] crops on the farm and the value gain is [1/5/22/3x].
Dual Flavour Permits requires you to have 2 flavour active to gain the bonus [2/6/18/8+], and at max level, it gain value per level active.
Pig requires you to have [6/8/10/12] active set bonuses and the value gain is [2/7/20/2x].

These numbers are 1.3 numbers and they might have changed but it is enough to show the principle in action.

The baseline for passives is [2/6/18/60], and dual flavour permit is the main card that all other cards balanced against.

Getting 2 specific flavours is not hard, but it constraints 4 cards in your deck.
Getting 6 active set bonuses is not hard, and you naturally get them. Despite it requires more active bonuses, it also allows for alot of flexibility.
The game kind of balanced around having 16-20 crops, so having less than 22 crops is very normal.

This is why the number for T1 is 2 for flavour and pig, but 1 for small farm.

However, as you go up the tiering, the difficulty of pig and small farm changes.
The flavour permits constraint stays the same, while the other 2 increases in difficulty.
These are all balanced against the "baseline values" of a normal farm (see 0. Baseline Values in previous section).
So if the constraints forces you off the baseline, then it will give more values, since you need to work around the constraints.
This is why upgraded pig provide more value than baseline passive cards. (See 6. Upgrading Cards)

Small Farm and Pig also gives multiplier at 2x, because their constraints is very limiting.

At T4, the dual flavour permits generate max values only when you max out both flavours.
This extremely limits your deck composition, unless you mutate most of your crops to have the flavours.
This makes the constraints dynamic, and also makes the value gen dynamic.

## 2. Build Pathing
A huge part of the game revolve around pathing to different build to maximise value gain.
With every card acquired, there are opportunity to change the build for the better.

To allow for build pathing, the way that mechanics interacts with each other needs to be soft and not hard.

### Soft Synergy over Hard Synergy
Card interacts with each other mostly via croptypes.
This is very important because if a specific card is named, when one is banned, the other become useless.

## 3. Water
At the start of the game, the player get 15 water from Spring effect, and 20 from Sprinkler.
This allows the player to have 7 crops.

In summer, the player loses 15 water and gains 1 sprinker (which provide 15 water, 20 if not upgraded.). This is a net 0 change.
However, with Summer, the cost of crop increases. This serves as a push for the player to scale water.

Do not change Spring and Summer. These 2 seasons are the way they are for a reason.

There are 3 ways that water gain happens.

1. Start of day
2. Middle of the day
3. End of day

At the start of the game, you get Sprinkler, which is a mid day water gain.
Many crops also provide water on mature and on harvest. They are considered as end of day water gain.
Wet synergy and Spring season effect are start of day water gain.

In general
Mid day > End day > Start of day

The reason is due to how some cards/synergy rely on water threshold. Gaining water before crop matures usually gets more value.

On mature water gain is also considered as end of day water gain since you can't control when they happen.
Sometimes they happen at the end and most of the crops already matured and did not gained from fruit synergy.

On wither water gain is considered mostly as mid day water gain since you can control it reasonably.

Potential Design space
- start of day water source isn't explore as much at the moment.

### Water vs Farm Water vs Excess Water
In general, Water > Excess Water > Farm Water, meaning to say that Excess Water is easier to achieved than Farm water.

This is because farm water requires you to consume the water first, and you can assume that per day, Farm Water is usually cap at 150.
Consuming and gaining more than 150 farm water per day requires specific build.

There is also a reason why Fish specifically gain value based on farm water.
Duck + Fish + Sprinklers was pretty dumb as a strat in the early build where you can just plant nothing and win.
It wasn't fun, so I nerf it to farm water.

### Deck Cost
Related to water, max water capacity is also fixed at 150.
Because of this, this means that if you consume more than 150 water per day, you need to figure out a way to gain water mid day.

This number cannot and should not be changed. This means no passive that increase max water cap.

This will change the balance of the game drastically.

## 4. Engine building vs Problem Solving
The game is an engine builder.

I had some ideas for a system where the game further restricts or change the rules, like curses in slice and dice.

However, I feel that this changes the focus of the game from engine building to problem solving, which is not what I want with the game.
The game revolve around finding the best parts for your engine on a fixed track, and not a track that keep changing that you need to adapt to.

Many might think that a difficulty system where the payment keep increasing is a badly designed difficulty settings, but I disagree.
I think for engine builder, the difficulty revolve around learning how to build better engines, and not solve harder problems.

## 5. Crop Rarity
Common Crops should be simple and should just provide value or water. The current exceptions are the invasive crops.
Uncommon Crops in general provide spread/mutliplier, or provide draft. Some uncommon crops also provide unique ability that are too weak for Rare.
Rare Crops should be either value bomb, or oddly specific ability.

One interesting thing here is common being the only source of water gain outside of mutations.
This means that for Cat build to work, water need to be solved outside of crops.

On the other hand Rat build means that drafting will be an issue, and going wide will also be tricky.

I think it is important to keep in mind this when adding cards in each rarity.

## 6. Upgrading Cards
In 1.2, upgrading passive cards to T3 was not satisfying, and you can't see a significant jump in value, and the T4 jump for multiplier is too big.
In 1.3, the goal is to make upgrading passives to T3 and T4 satisfying.

Keep in mind that passives are limited, so upgrading them need to feel good.

General guideline will be:

- 2x Tier 1 < 1x Tier 2
- 2x Tier 2 << 1x Tier 3
- 2x Tier 3 <<<< 1x Tier 4

Another way to put it will be

- Tier 2 = 2x Tier 1 + [Reward for upgrading] + [Value from constraints]
- Tier 3 = 2x Tier 2 + [Even bigger reward for upgrading] + [Value from constraints]

There are some cases where 2x lower tier is better than 1x higher tier, like bee or if the higher tier requirement is not met.

Similarly, upgrading crops to T5 should be rewarding, so most T5 common should be as strong as t2-t3 uncommon crops.
Most of the time, we can assume that most crops will finish at T3.

Although it seems like it is harder to reach T4/T5 with Rare crops, it is still possible with trade-in.
Some crop spike is very powerful, like Snapdragon and Thyme etc.

### Power spike
Another point to consider is the power spike for each card.

Let's use a few cards as example

1. Fig
2. Peanut
3. Pumpkin

Fig power spike at T5. These cards are the cards that you usually want to aim to be T5.
Peanut doesn't power spike and grow linearly. These cards usually don't need to be at max tier, and player can take the upgrade as they come or on a need basis.
Pumpkin and many of the multiplier crops doesn't power spike. Most of the time, even T1 is strong.

Having different crops with different growth curve makes for interesting gameplay.

Mutations also have different powerspike curve. So combine this with crops powerspike, this allows for emergence.

Although the numbers may be small, they adds up over time.

# Specific Thoughts

## 1. Crop Types
Overall I think that all the Crop Types are relatively balanced right now.

Crop Types are split into 3 groups, Value, Water and Misc

In the Value group, we have Fruit, Herb, Vegetable, Flavours and Spatial.
In the Water group, we have Dry, Wet, Root and Mushroom.
In the Misc group, we have Seed, Flower and Invasive.

I think the types are very balanced right now. Some note for each type (from my own actual games).

### Fruit
Fruit is very strong early and help if you don't get enough value permits. However, once the deck gets too big retaining 120 water is harder.
Late game fruit synergy requires cost reduction or strong mid day water gain.

### Vegetable
Vegetable is quite a strong synergy but it forces you to maintain a certain ratio of flavours to non-flavours.
Changing from adjacent to around reduces the ratio. I might reduce the value gain since it is easier now, but we can test it more.

### Herb
Herb is very basic but it also make crops that stays around better.
I definitely want more slow growing crops ideas eventually, probably variant-ish

### Flavours
Flavours are pretty decent now. With the new flavour mutation (1.3), this becomes easier.
Because flavours usually span multiple rarity, it means early flavours isn't easy to hit.

### Spatial
Spatial is tricky to value. I think it needs a buff.
It is quite hard to hit and once you are in, it is hard to pivot unlike the rest.

### Dry
Dry is a very early game fixer for water. I think it need a buff somehow, because it really fall off really fast.

### Wet
Wet is decent. Because it happens at the start of the day, it is not as broken.
It might deserve a buff.

### Root
Root is pretty balanced right now. No need to change.

### Mushroom
Mushroom is very specialised water fixer and requires you to build around it, or have specific cards to abuse it.

### Seed
Pretty staple and balanced. I experimented with 3/4/5 and it was too strong. 3/5/7 should be the most stable version of this.

### Flower
No comment. Pretty unique.

### Invasive
Not sure about this yet. I have a feeling that this may need a buff to 1/2/3.
Might become too strong after that, especially with a single crop allowing for a set means that pig get buffed.
I do want to try it though.

## 2. Crops
For common crops, I think most of them are fine as it is.
The only 1 ability that I dislike now is the one in Portobello and Apple.
Both of them still rely on the outdated ability of adjacency.
Given that they are both "Spatial", i.e. Support and Climber, I think it is fine to leave them be.

For uncommon crops, similar to common, the only one that is weaker (in term of design) is the flavour adjacency ones in ginger and lotus root.
I don't mind it here, but if an interesting root ability can be found, then these 2 can be replaced.

For rare crops, all of them are there for a purpose.
Maple seed is the weakest of them all, but it still serve a purpose as a support crop spam.

Overall Crops should be fine. Maybe adding variant to the weaker ones is better than changing them.

## 3. Permits
Permits has a few that I really want new ability for, or some type of rework.

Fruit Permit is by far the weakest (design wise) of them all.
I initially design fruit permit to be the counterpart of herb permit, where herb improves everything, while fruit only improve itself.
Fruit also uses Sour + Sweet, while Herb uses Spicy + Bitter.
I still want to keep this design, but perhaps remove the flavour link ? Not sure.

Salad Bar permit is very single-dimension and I want to see if there is a way to improve it.

Alcohol and Tea is pretty similar to Butterfly, and I feel that these 2 should also be changed.

One question perhaps is whether or not we can link flavours into alcohol and tea.

For example

Fruit Permit - Frut + Sour and Sweet
Herb Permit - Herb + Spicy and Bitter
Alcohol Permit - Fruit/Seed + Bitter and Sweet
Tea Permit - Herb/Flower + Sweet and Spicy
Vegetable Permit - ????

Perhaps one thought is to remove Flavouring permit, and replace Salad bar with flavouring permit ?

I think if we have ideas for new permits that causes the number of permits to overflow, then we can consider removing some of these permits.

Some croptypes are used multiple time, which makes them(the croptype) too strong.
More thinking/testing is required.

## 4. Animals
Rabbit and Duck is the 2 main animals that I have issues with right now.

They act as water fixer, but having them generally weaken the build.

Overall we want passives to provide values and use crops / tools to do water fixing.

## 5. Mutations
There is only one last issue with mutations - Vegetable mutation.
I honestly still don't like this mutation and I think there is a case to be made to replace vegetable mutation with organic mutation and remove organic mutation.
This treatment is the same as making climber mutation spreader mutation.

This will then allow each crop type to have a mutation, and streamline the game even further.

## 6. Tools
I think I need 1 more tool to dilute the pool but I am still not sure yet.
The 5 tools already cover all things I need from tools.
If ever another tool is added to the game, it should be in the base set.

# Last Card set and beyond
I have left 10 crops , 2 permits and 2 animals open for the last set, probably 1.4.

After the last set is added, new crops ability should be added as variants.

Adding variants has an implication on the banning of cards.
For example, because tulip has 4 variants for flavours, it is counted for 5 types.
Meaning if it is chosen as the rare for the run, some flavours will have very little cards.
