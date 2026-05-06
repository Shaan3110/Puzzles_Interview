# Puzzles_Interview

## Ant Puzzle

Three Ants and Triangle : There are 3 ants sitting on three corners of a triangle. All ants randomly pick a direction and start moving along the edge of the triangle. What is the probability that any two ants collide?

**Solution** - See , ants are not going to collide in 2 cases one is they can move clockwise ( all of them ) and other is they all move anti-clockwise. Now to find probability we need to find the sample size so , each of our ants ( 3 ants ) have 2 choices to move either left or right. So the total number of options would be 2^3 = 8. Now probability of any two ants collide is 6/8 then.

## Heaven and Hell

There are two gates, one to hell and the other to heaven. Two gatekeepers, one for each gate. One of them always speaks the truth and the other always lies but you don’t know which one guards which gate. You are allowed only one question and you need to find out the gate to heaven.

**Solution** - See, I am going to ask this question -> Tell me if i ask the other guard about the route to heaven then which gate he is going to point me to.

Let's say the guard was truthy, he knows the other guard is the lier so the gate he would point to going to be hell.
Let's say the guard was lier , he knows the other guard is the truthy so he is going to point to the gate going towards hell to trick me.

In both cases I am getting the gate of hell , just go opposite of what they say and you will have gate of heaven.

## 10 Coins Puzzle

You are blindfolded and 10 coins are placed in front of you on the table. You are allowed to touch the coins but can’t tell which way up they are by feel. You are told that there are 5 coins head up, and 5 coins tails up but not which ones are which. Can you make two piles of coins each with the same number of heads up? You can flip the coins any number of times. 

**Solution** - See, Let's just make 2 random groups with 5 coins each. Now we know that there were 5 heads and 5 tails randomly so if the first group has x heads now the below group will have 5-x .

So to just make them same, flip all coins of first group so it becomes 5-x heads.

Pile 1: H H T T T
Pile 2: H H H T T

Now flip all coins in Pile 1:

Pile 1 becomes: T T H H H
Pile 2 remains: H H H T T

Now both piles have 3 heads each.




