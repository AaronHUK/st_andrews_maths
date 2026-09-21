# Dice and Coins

## Coins

### Adding more coins

Last week, we saw that the outcomes for flipping 2 coins look like this:

```Number of heads:
  0  |  1  |  2
=====+=====+=====
  1  |  2  |  1
```

Does anyone have any predictions about what flipping 3 coins will look like?

We can do better than predict - we can work out what the distribution will be!

let's put the outcome of 2 coin flips as one side of a table:
```
First ||
  2   ||
Coins ||
======++
   0  ||
   1  ||
   1  ||
   2  ||
```

Why does 1 appear twice in this table?

Then let's add another coin toss:
```
 First ||
  Two  || Second coin
 Coins ||   0   |   1
=======++=======+=======
   0   ||       |
   1   ||       |
   1   ||       |
   2   ||       |
```

Counting up the results:
```
  0  |  1  |  2  |  3
=====+=====+=====+=====
     |     |     |
```

Let's check if our predictions match what we actually get.

### Pascal's triangle

Does anyone see a pattern in these numbers?

```  1   1
   1   2   1
 1   3   3   1
```

### Pointy or flat
