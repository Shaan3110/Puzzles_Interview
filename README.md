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

## Mislabeled Jars

There are 3 jars, namely, A, B, C. All of them are mislabeled. Following are the labels of each of the jars:A: CandiesB: SweetsC: Candies and Sweets (mixed in a random proportion)You can put your hand in a jar and pick only one eatable at a time. Tell the minimum number of eatable(s) that has/have to be picked in order to label the jars correctly.

**Solution** - 1 pick from the jar of combined is enough to determine it.

There are three jars labelled A, B, and C, and all are incorrectly labelled.

Jar A: “Candies”
Jar B: “Sweets”
Jar C: “Candies and Sweets” (mixed)

Step 1: Start with Jar C (labeled “Candies & Sweets”)

All jars are incorrectly labeled.
So, Jar C cannot be a mixture.
It must contain only Candies or only Sweets.
Pick one item from Jar C.
Suppose you get a candy → Jar C = Candies only

Step 2: Identify Jar B

Jar B is labeled “Sweets”, but labels are wrong.
So, Jar B cannot be only sweets.
It also cannot be candies (because Jar C already has candies).
Therefore, Jar B must be Candies & Sweets (mixture)

Step 3: Identify Jar A

Only option left is Sweets
So, Jar A = Sweets

## 50 red marbles and 50 blue marbles

Give two boxes B1 and B2 one has 50 red marbles and the other has 50 blue marbles. A ball is selected randomly from any of the boxes and the task is to maximize the probability of selecting a red ball, by reshuffling marbles in both boxes.

**Solution** - Just move one red ball to one jar and all left ones to right adding 49 red balls plus 50 blue balls on jar 2.

With Redistribution

If we decrease the number of red marbles in B1 and increase the number of red marbles in B2, the probability of getting a red marble will be maximized.

To maximize P(R), place 1 red marble in B1 and move the remaining 49 red marbles to B2. After redistribution:

B1 contains: 1 red marble (1 marble total)
B2 contains: 49 red + 50 blue marbles (99 marbles total)
Therefore:

```P (R) = ((1 / 2) * (1 / 1)) + ((1 / 2) * (49 / 99)) = 0.747474```

Hence, the maximum probability of choosing a red ball is ``0.747474``

## Minimum cut Puzzle

You have got someone working for you for five days and a gold bar to pay him. You must give them a piece of gold at the end of every day. What are the fewest number of cuts to the bar of gold that will allow you to pay him 1/5th each day?

**Solution** - Just make 2 cuts one after 1 unit and other after 2 unit.

It can also be explained using the table below:

Days	Worker Gets	You Take Back	
Worker Holds

**Explanation** -

``Day 0	:`` No Payment yet.

``Day 1:``Pay the worker Gold Bar with 1 unit.

``Day 2:``Pay the worker Gold with 2 units and take back the gold bar with 1 unit.

``Day 3:``Pay the worker Gold Bar with 1 unit.

``Day 4:``Pay the worker Gold with 2 units and take back the gold bar with 1 unit.

``Day 5:``Pay the worker with only left Gold Bar with 1 unit.



