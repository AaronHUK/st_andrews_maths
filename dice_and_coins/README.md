# Dice and Coins

## Dice

### Flat distribution

Rolling a dice gives you an even chance of getting every number. Let's quickly demonstrate that now:

> [!IMPORTANT]
> Grab 2 same coloured dice from the front. Roll one of them 10 times and tally your results in table A.

[Dice rolling example](https://docs.google.com/spreadsheets/d/1HUFuqyx0c2wW2K_zEDdOnPgo2Z_aOr8HdQ8JqLKjLnc/edit?usp=sharing)

<details>
<summary>python dice roller</summary>

```import random
from collections import defaultdict

outcomes = defaultdict(int)
trials = 1000
dice = 1

for _ in range(trials):
    my_int = 0
    for die in range(dice):
        my_int += random.randint(1, 6)
    if trials <= 100:
        print("Rolled a score of " + str(my_int) + "!")
    outcomes[my_int] += 1

if trials > 100:
    print("Performed " + str(trials) + " dice rolls!")

header, outcome = "", ""
for result in range(dice, dice*6 + 1):
    header += str(result).rjust(8)
    outcome += str(outcomes[result]).rjust(8)

print header
print outcome
```

[Python sandbox](https://pythonsandbox.com/)

</details>

### 2 Dice distribution

What do you think 2 dice rolls look like (as in monopoly)? Will it be flat like a single dice roll?

> [!IMPORTANT]
> Roll both dice 10 times and tally your results in table B.

Why is `7` more likely than any other number?

Let's look at the possible outcomes:

```
Dice ||  1  |  2  |  3  |  4  |  5  |  6
=====++=====+=====+=====+=====+=====+=====
  1  ||  2  |  3  |  4  |  5  |  6  |  7
  2  ||  3  |  4  |  5  |  6  |  7  |  8
  3  ||  4  |  5  |  6  |  7  |  8  |  9
  4  ||  5  |  6  |  7  |  8  |  9  | 10
  5  ||  6  |  7  |  8  |  9  | 10  | 11
  6  ||  7  |  8  |  9  | 10  | 11  | 12
```

In fact, `7` is the only number you can always reach regardless of what the first dice roll is!

Does anyone have any guesses on what the graph for 3 dice would look like?

## Coins

Coins are a simpler example than dice - if you toss two coins and count the number of heads, you see a similar pattern emerge - the table might look like this:

```
Heads ||  0  |  1
======++=====+=====
   0  ||  0  |  1
   1  ||  1  |  2
```

What do you think the graph will look like?

> [!IMPORTANT]
> Come up and take 2 coins from the front. You and your partner both toss a coin and tally the number of heads in table C 10 times.

For 3 coins, we can go through the options in this table:

```
 Coin1 || Coin2 || Coin3 || Heads
=======++=======++=======++=======
   0   ||   0   ||   0   ||
   0   ||   0   ||   1   ||
   0   ||   1   ||   0   ||
   0   ||   1   ||   1   ||
   1   ||   0   ||   0   ||
   1   ||   0   ||   1   ||
   1   ||   1   ||   0   ||
   1   ||   1   ||   1   ||
```

