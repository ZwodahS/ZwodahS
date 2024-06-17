*(Note1)*
This doc is written for myself, despite being public. "you" in most cases refers to "future me" and not the reader "you", unless you are me....
"we" refers to me and "future me" as well.

*(Note2)*
Reading this will spoil some parts of the game.

*(Note3)*
This doc is a work in progress.

I kind of want to write down my understanding of Crop Rotation after 1+ years of working on it.
These understanding will fade once I start my next project, so it is good to formalise them, in case I need to add more content in the future.

This is written as of Version 1.3 (June). Let's try to keep this updated when things changed.

# Balance and Baseline Values

## 1. Rating
In 1.2, the game was balanced around 1k rating, i.e. a good player should be able to beat the game 100% of the time at 1000 rating.
In 1.3, this is moved to 1.5k due to many cards being buffed at T3/T4.

This is also balanced around rating mode and not turbo mode.

Note that after playing quite a bit, it seems like even 2k is streakable.

## 2. Passives(Animal/Permit) Baseline
The biggest problem for passive in 1.2 are multipliers.
Multipliers are hard to value, and they are really strong.
If the passive card does not have a multiplier then it is really weak.

Let's compare 2 passives as example. Wet Permit vs Big Farm Permit.
They both scale similarly until T3, and when it hit T4, Big Farm Permit instantly out-scale Wet Permit.

This really make some permits less useful than those with multiplier.

To put in more details, previous in 1.2, the balance point for these were [2/5/12/2x] for most of these passive.
At T4, the jump from 12 to 2x is too much. For non-2x passives, the balance point was [2/5/12/30].
Looking at this, it is obvious that non-2x passives are too weak.

After 1.2, I realised this problem and I know that finding the balance between multiplier and raw value needs to be done eventually.
These passive cards are now balanced around [2/6/18/60|2x].

## 3. Predicted/Expected Game flow
1. First power spike should happen at start of week5 (first trade in) by getting first T4.
2. Second power spike should happen at start of week6 (second trade in) by getting second T4.
3. Deck should be completed by start of week7 with minimum changes moving forward (i.e. just upgrading).
4. Week 7 and 8 is a test to see if the build actually scale well into end game.
5. 3 T4 by end of game is normal, but sometimes 2 T4 + 3 T3 will suffice.

Note that this game flow wasn't designed initially in pre1.1. This is more discovered than designed.
There are also a few playstyle that do not follow this.

In 1.3 this is more interesting with the trade-in change.
pre1.3, Trade-in are fixed, i.e. Animal at week5, Permit at week6, Crops at week7.
1.3 changed it such that you choose which one you get.

## 4. Baseline Values
These values are what the game is designed around.

1. Having 14 Crops and 2 Tools in Deck.
2. Having full deck latest by end of Week 4, full storage by end of week 5.
3. 12 Crops by week 3, 16 Crops by week 4, 20 Crops by week 5, 24 Crops by week 6 (4 rows of 6).
4. Focusing on maxing a value-generating croptype, i.e. (Vegetable/Fruit/Herb/Flavours).
5. Deck Cost should be around 100 by end game (with mutations).
6. Based on (5), you should generating around 100 Farm Water / day, and also expected to maintain 150 water at the start of each day.
7. Gaining around 2 crops per day by mid game (week3), excluding skip.
8. Completing 80-90% of all contracts before week 7, i.e. you should have around 35-38 passives/tools by start of week 7.
9. Expect mostly T3 crops by the end of the game, with some T4 and 1 or 2 T5.
10. Most deck should contains unique crops. Mono-cropping should not be the main strategy and should only work in some cases.

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

Getting 2 specific flavours is not hard, but it constraints 4 cards of your deck.
Getting 6 active set bonuses is not hard, and you naturally get them, so despite it requires more bonuses, it allows for alot of flexibility.
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

## 2. Water
At the start of the game, the player get 15 water from Spring effect, and 20 from Sprinkler.
This allows the player to have 7 crops.

In summer, the player loses 15 water, but gained 1 sprinker (which provide 15 water, 20 if not upgraded.). This is a net 0 change.
However, with Summer, the cost of crop increases. This serves as a push for the player to scale water.

Do not change Spring and Summer. These 2 seasons are the way they are for a reason.

## 3. Engine building vs Problem Solving
The game is an engine builder.

I have some ideas for a system where the game further restricts or change the rules, like curses in slice and dice.

However, I feel that this changes the focus of the game from engine building to problem solving, which is not what I want with the game.
The game revolve around finding the best parts for your engine on a fixed track, and not a track that keep changing that you need to adapt to.

Many might think that a difficulty system where the payment keep increasing is a badly designed difficulty settings, but I disagree.
I think for engine builder, the difficulty revolve around learning how to build better engines, and not solve harder problems.

## 4. Deck Cost
Because the max water is 150, this means that if your deck cost more than 150, you need to figure out a way to gain water mid day.
There are also other stuffs that cost water.

This number cannot and should not be changed. This means no passive that increase max water cap.

This will change the balance of the game drastically.

## 5. Crop Rarity
Common Crops should be simple and should just provide value or water. The current exceptions are the invasive crops.
Uncommon Crops in general provide spread/mutliplier, or provide draft. Some uncommon crops also provide unique ability that are too weak for Rare.
Rare Crops should be either value bomb, or oddly specific ability.

## 6. Upgrading Cards
In 1.2, upgrading to T3 is not satisfying, and you can't see the jump in value, and the T4 jump for multiplier is too big.
In 1.3, the goal is to make upgrading passives to T3 and T4 satisfying.

Similarly, upgrading crops to T5 should be rewarding, so most T5 common are as strong as t3-t4 uncommon crops.

General guideline will be:

1. 2x Tier 1 < 1x Tier 2
2. 2x Tier 2 << 1x Tier 3
3. 2x Tier 3 <<<< 1x Tier 4

or in a way

1. Tier 2 = 2x Tier 1 + [Reward for upgrading] + [Value from constraints]
2. Tier 3 = 2x Tier 2 + [Even bigger reward for upgrading] + [Value from constraints]

There are some cases where 2x lower tier is better than 1x higher tier, like bee or if the higher tier requirement is not met.

# Remaining problems and challenges.

## Cards
There are still some cards that I am extremely unsatisfied with.
I will list them down here for reference and you can change them once you find suitable effects.

### 1. Crops

For common crops, I think most of them are fine as it is.
The only 1 ability that I dislike now is the one in Portobello and Apple.
Both of them still rely on the outdated ability of adjacency.
Given that they are both "Spatial", i.e. Support and Climber, I think it is fine to leave them be.

For uncommon crops, similar to common, the only one that is weaker (in term of design) is the flavour adjacency ones in ginger and lotus root.
I don't mind it here, but if an interesting root ability can be found, then these 2 can be replaced.

For rare crops, most are in theme or serve a purpose.
Maple seed is the weakest of them all, but it still serve a purpose as a support crop spam.

Overall Crops should be fine.

### 2. Animals

Rabbit and Duck is the 2 main animals that I have issues with right now.
They act as water fixer, but having them generally weaken your build.
Overall you want passives to provide values and use crops / tools to do water fixing.

### 3. Permits

Permits has a few that I really want new ability for, or some type of rework.

Fruit Permit is by far the weakest of them all.
I initially design fruit permit to be the counterpart of herb permit, where herb improves everything, while fruit only improve itself.
Fruit also uses Sour + Sweet, while Herb uses Spicy + Bitter.
I still want to keep this design, but perhaps remove the flavour link ? Not sure.

Salad Bar permit is very single-dimension and I want to see if there is a way to improve it.

Alcohol and Tea is pretty similar to Butterfly, and I feel that these 2 should also be changed.

One question perhaps is whether or not we can link flavours into alcohol and tea.

In short

- Fruit Permit - Frut + Sour and Sweet
- Herb Permit - Herb + Spicy and Bitter
- Alcohol Permit - Fruit/Seed + Bitter and Sweet
- Tea Permit - Herb/Flower + Sweet and Spicy
- Vegetable Permit - ????

Perhaps one thought is to remove Flavouring permit, and replace Salad bar with flavour permit ?

I think if we have ideas for new permits that causes the number of permits to overflow, then we can consider removing some of these permits.

### 4. Tools

I think I need 1 more tool to dilute the pool but I am still not sure yet.
The 5 tools already cover all things I need from tools.
If ever another tool is added to the game, it should be in the base set.

## Mutations

There is only one last issue with mutations - Vegetable mutation.
I honestly still don't like this mutation and I think there is a case to be made to replace vegetable mutation with organic mutation and remove organic mutation.
This treatment is the same as making climber spreader.

This will then allow each crop type to have a mutation, and streamline the game even further.

## Rating
Currently I have re-balanced the game around 1.5k.
However, after playing the game and getting good at it, 2k rating seems to be streakable as well.

At 2k, I am still able to win on week7 quite often. More testing is needed, but I think by shifting some numbers to week7/8 heavy, 3k or even 4k will be streakable.

## Last Card set and beyond
I have left 10 crops , 2 permits and 2 animals open for the last set, probably 1.4.

After the last set is added, new crops should be added as variants.

Adding variants has an implication on the banning of cards.
For example, because tulip has 4 variants for flavours, it is counted for 5 types.
Meaning if it is chosen as the rare for the run, some flavours will have very little cards.
