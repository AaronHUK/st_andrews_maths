# Dice and Coins

Dice have the same chance of rolling 1 - 6

[Dice rolling example](https://docs.google.com/spreadsheets/d/1HUFuqyx0c2wW2K_zEDdOnPgo2Z_aOr8HdQ8JqLKjLnc/edit?usp=sharing)

<details>
<summary>python dice roller</summary>
```import random
from collections import defaultdict

outcomes = defaultdict(int)
trials = 100000
dice = 3

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
    header += str(result).rjust(6)
    outcome += str(outcomes[result]).rjust(6)

print header
print outcome```
</details>
