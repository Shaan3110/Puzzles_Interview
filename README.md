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


## 100 Doors 

There are 100 doors in a row, all doors are initially closed. A person walks through all doors multiple times and toggle (if open then close, if close then open) them in the following way: In the first walk, the person toggles every door In the second walk, the person toggles every second door, i.e., 2nd, 4th, 6th, 8th, … In the third walk, the person toggles every third door, i.e. 3rd, 6th, 9th, … Likewise, In the 100th walk, the person toggles the 100th door. Which doors will be open at the end ?

**Solution** - A door is toggled in the i-th walk if i divides the door number, for example: Door number 45 is toggled during the 1st, 3rd, 5th, 9th, 15th, and 45th walks.
Each door is toggled once for every divisor of its number, and divisors typically come in pairs (e.g., for 45: (1,45), (3,15), (5,9)).
Each pair of divisors cancels out the toggle effect (open - close or close -open), therefore, doors with an even number of divisors return to their initial closed state.
Perfect square numbers (e.g., 16) have one unpaired divisor (like 4 in 4×4), resulting in an odd number of divisors.
An odd number of toggles leaves the door in the open position; hence, only perfect square-numbered doors (e.g., 1, 4, 9, 16, ..., 100) remain open.
Prime numbers (e.g., 2, 3, 5, 7) have exactly two divisors (1 and itself), which is a pair - the door remains closed.
Non-square composite numbers (e.g., 15) have divisor pairs, so they are also closed at the end.

So the answer is ```1, 4, 9, 16, 25, 36, 49, 64, 81 and 100.```

## Find the fastest 3 horses 

There are 25 horses among which you need to find out the fastest 3 horses. You can conduct a race among at most 5 to find out their relative speed. At no point, you can find out the actual speed of the horse in a race. Find out the minimum no. of races that are required to get the top 3 horses. 

**Solution** - 7 races needed to analyze this.

Make group of 5 horses and run 5 races. Suppose five groups are [a, b, c, d, e] and next alphabet is its individual rank in this group(of 5 horses).for eg. d3 means horse in group d and has rank 3rd in his group. [ 5 RACES DONE ] 

a1 b1 c1 d1 e1 
a2 b2 c2 d2 e2 
a3 b3 c3 d3 e3 
a4 b4 c4 d4 e4 
a5 b5 c5 d5 e5 

Now make a race of (a1,b1,c1,d1,e1).

[RACE 6 DONE] suppose result is a1>b1>c1>d1>e1 which implies a1 must be FIRST. 
b1 and c1 MAY BE(but not must be) 2nd and 3rd. 
FOR II position, horse will be either b1 or a2 

(we have to find top 3 horse therefore we choose horses b1,b2,a2,a3,c1 do racing among them [RACE 7 DONE]. 
The only possibilities are : 

c1 may be third 
b1 may be second or third 
b2 may be third 
a2 may be second or third 
a3 may be third 

The final result will give ANSWER.

suppose result is a2>a3>b1>c1>b2 then answer is a1,a2,a3,b1,c1. 

Hence, the answer is 7 RACES 

## Calculate total distance traveled by the bee 

Two trains are on the same track and they are coming toward each other. The speed of the first train is 50 km/h and the speed of the second train is 70 km/h. A bee starts flying between the trains when the distance between two trains is 100 km. The bee first flies from the first train to the second train. Once it reaches the second train, it immediately flies back to the first train … and so on until trains collide. Calculate the total distance traveled by the bee. The speed of the bee is 80 km/h. 


**Solution** - With respect to Train A, train B's velocity is (70+50) = 120 km/hr. Thus, the time taken by Train B to collide with Train A will be

 ```(100 km) / (120 km/hr)  = 5/6 hr = 50 min```

 
 Now, since the velocity of the bee is 80 km/hr, the distance travelled by the bee in this time interval will be

 ```80 km/hr * 5/6 hr = 66.67 km (approx)```

 ## 3 cuts to cut the round cake into 8 equal pieces 
 
 You have a birthday cake and have to cut it into 8 equal pieces by making 3 cuts only. How do you do it?

 **Solution** - Just make horizontal and vertical cut which would devide the cake in 4 pieces and 3rd cut on center of the height to make it 8 pieces.

 ## Find the last ball to remain after the entire process 
 
There are 20 red balls and 16 blue balls in a bag. Any 2 balls are removed at each step and are replaced with a new ball on the basis of the following conditions: If they are of the same color, then they are replaced by a blue ball. If they are of different colors, then they are replaced with a red ball. Find the last ball to remain after the entire process. Here replacement means that the new ball is inserted into the bag. Once you take out the balls, you do not put them back in the bag – so the balls keep reducing. 

**Solution** - Blue ball would be the last one as the red keeps decreasing in even so i cannot be the last ball which is odd.

**Explanation** -

Step 1: Check the number of Red balls

Initially:

20 Red balls
16 Blue balls
20 is an even number.

Step 2: What happens to Red balls?

When two balls are removed:

Red + Red → Red decreases by 2
Blue + Blue → Red unchanged
Red + Blue → Red unchanged
So the number of Red balls either decreases by 2 or stays the same.

This means the number of Red balls always remains even.

Step 3: The last ball

At the end, only one ball remains.

If it were Red, then the number of Red balls would be 1 (odd).
But we have already shown that the number of Red balls always remains even.

Since this is not possible, the last ball cannot be Red.

So, the only possibility is that the last remaining ball is Blue.

Core Insight

For this set of replacement rules:

If the initial number of Red balls is odd, the last ball is Red.
If it is even, the last ball is Blue.
