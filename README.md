# Puzzles_Interview

Refer to greeksforgreeks 100 puzzles cheat sheet for better understanding. It's a revision note here -

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

## How to Measure 45 minutes using two identical wires

How do we measure forty-five minutes using two identical wires, each of which takes an hour to burn? We have matchsticks with us. The wires burn non-uniformly. So, for example, the two halves of wire might burn in 10 minutes and 50 minutes respectively.

**Solution** - If we light a wire, it takes 60 minutes to burn completely. What if we light the wire from both sides? It will take exactly half the original time, i.e. 30 minutes to burn completely.

0 minutes – Light wire 1 on both sides and wire 2 on one side. 


30 minutes – wire 1 will be burnt out. Light the other end of the wire 2.

45 minutes – wire 2 will be burnt out. Thus 45 minutes is completely measured.

## Find ages of daughters : Alok has three daughters. His friend Shyam wants to know the ages of his daughters. Alok gives him the first hint.

The product of their ages is 72. 
Shyam says this is not enough information Alok gives him a second hint.
The sum of their ages is equal to my house number. 
Shyam goes out and looks at the house number and tells “I still do not have enough information to determine the ages”. 
Alok admits that Shyam can not guess and gives him the third hint
The oldest girl likes strawberry ice cream. 
Shyam is able to guess after the third hint.

**Solution** -

From Hint 1: The Product of the ages is 72

Below are all 12 possibilities to get 72 from the product of three different ages:

1 * 1 * 72 = 72
1 * 2 * 36 = 72
1 * 3 * 24 = 72
1 * 4 * 18 = 72
1 * 6 * 12 = 72
1 * 8 * 9 = 72
2 * 2 * 18 = 72
2 * 3 * 12 = 72
2 * 4 * 9 = 72
2 * 6 * 6 = 72
3 * 3 * 8 = 72
3 * 4 * 6 = 72
Shyam was not able to guess the ages of daughter so, he asked for 2nd hint.
From Hint 2: The Sum of the Ages Equals the House Number

The second hint tells us that the sum of the ages equals the house number. Sum of the ages is given as:

1 + 1 + 72 = 74
1 + 2 + 36 = 39
1 + 3 + 24 = 28
1 + 4 + 18 = 23
1 + 6 + 12 = 19
1 + 8 + 9 = 18
2 + 2 + 18 = 22
2 + 3 + 12 = 17
2 + 4 + 9 = 15
2 + 6 + 6 = 14
3 + 3 + 8 = 14
3 + 4 + 6 = 13
From this, we can see that the two sets of daughters have the same sum of 14:

2 + 6 + 6 = 14
3 + 3 + 8 = 14
At this point, Shyam is still unsure about the daughters’ ages, so we move to the final hint.
From Hint 3: The oldest girl likes strawberry ice cream. 

This hint is important because it tells Shyam there is a single eldest daughter. If there were two daughters who were the oldest, Shyam wouldn’t be able to figure out the ages, as there would be ambiguity.

In the combination (2, 6, 6), there are two daughters who are the oldest (6 years old), so this cannot be the correct answer.

## Camel and Banana Problem

A person owns a banana plantation and needs to transport 3000 bananas to a market located 1000 km away. The only available means of transportation is a camel.

The camel has the following limitations:

It can carry a maximum of 1000 bananas at a time.
It consumes 1 banana per kilometre travelled.

**Solution**-

Step 1: From 3000 to 2000 Bananas

The camel must transport 3000 bananas, but it can carry only 1000 at a time. Therefore, 3 trips are required.

For each kilometre:

Two trips involve moving forward and returning, consuming 2 bananas each
One trip involves only moving forward, consuming 1 banana
Total consumption = 5 bananas per kilometer

3000 − 5x = 2000
 x = 200 km

After this stage:

Distance covered = 200 km
Bananas remaining = 2000

Step 2: From 2000 to 1000 Bananas

Now, 2 trips are required.

For each kilometre:

One trip involves moving forward and returning, consuming 2 bananas
One trip involves only moving forward, consuming 1 banana
Total consumption = 3 bananas per kilometer

2000 − 3y = 1000
 y = 333.33 km

After this stage:

Total distance covered = ``533.33 km``
Bananas remaining = 1000

Step 3: Final Stage

At this stage, the camel carries 1000 bananas in a single trip.

Remaining distance:
 ```1000 − 533.33 = 466.67 km```

Bananas consumed: ``466.67``

Bananas remaining at destination:
 ```1000 − 466.67 = 533.33```

##  Jar with Contaminated Pills

You are given five jars of pills, each containing the same number of pills. Every pill normally weighs 10 grams, but one jar contains contaminated pills that weigh 9 grams each. You are allowed to use a digital weighing scale only once.

Since we are allowed to use the weighing scale only once, we need to use a smart strategy rather than weighing each jar separately.

**Solution** -

Step 1: Label the jars as Jar 1 to Jar 5.

Step 2: Take a different number of pills from each jar:

```
1 pill from Jar 1
2 pills from Jar 2
3 pills from Jar 3
4 pills from Jar 4
5 pills from Jar 5
```
Step 3: Weigh all the selected pills together in one measurement.

If all pills were normal, the total weight would be 150 grams (15 × 10 g). Since one jar has pills that are 1 gram lighter, the actual weight will be less than 150 grams.

Step 4: Identify the jar

```
149 g → Jar 1
148 g → Jar 2
147 g → Jar 3
146 g → Jar 4
145 g → Jar 5
```

## 100 Prisoners with Red/Black Hats

One hundred prisoners are standing in a straight line, all facing the same direction.

Each prisoner is wearing a hat that is either red or black.
Every prisoner can see the hats of all prisoners standing in front of them, but not their own hat or those behind them.
The prisoners will be questioned one by one, starting from the last person in the line (who can see all others) and moving forward.
Rules:

Each prisoner must state the colour of their own hat.
If the guess is correct, the prisoner survives.
If the guess is incorrect, the prisoner is executed.
Before the process begins, the prisoners are allowed to discuss and agree on a strategy.
Once the questioning starts, no communication is allowed, except for stating “red” or “black”.
What strategy should the prisoners adopt to maximise the number of survivors, and how many prisoners can be guaranteed to survive?

**Solution** - 

A maximum of 99 prisoners can be guaranteed to survive by using a parity-based strategy.

Step 1: Signal by the Last Prisoner (100th)

The last prisoner counts the number of red hats in front.
If the count is even, he says “Red”.
If the count is odd, he says “Black”.
This announcement encodes the parity (even/odd) of red hats.
His own survival is uncertain (50% chance), as he is only passing information.

Step 2: Information Available to Others

Each subsequent prisoner has access to:

The initial parity signal
The answers have already been spoken
The hats visible in front
Step 3: Deduction Process

Each prisoner uses the expected parity given by the first prisoner.
Each prisoner counts the number of red hats visible ahead and the number of red hats confirmed from previous answers.
Each prisoner compares the observed parity with the expected parity.
If both match, the prisoner concludes their hat is black.
If they do not match, the prisoner concludes their hat is red.

Result

The first prisoner may be incorrect.
The remaining 99 prisoners are guaranteed to be correct.

## Monty Hall problem

The Monty Hall problem is a surprising probability puzzle:

There are 3 doors—two hide goats, and one hides a car.
You pick one door (let’s call it door 2), hoping it has the car.
The game show host, Monty Hall, then looks at the other two doors (1 and 3) and opens one that has a goat behind it (Say 3). (If both doors have goats, he chooses one at random.)
He then says to you, "Do you want to pick door 2 or stick to door 1.

What do you decide to have better chances of winning a car?

**Solution**-

The main trick is that the host would open the door with a goat only, so the chances of the other door having a car are higher. Hence, you should always switch to improve your chances. Below is a detailed solution.

Let’s solve the Monty Hall problem step by step, assuming the gates are numbered 1, 2, and 3:

Setup:

Player’s choice: The player initially picks gate 2.
The car is equally likely to be behind any of the three gates initially. Let’s evaluate the three possible arrangements:

1. Car behind gate 1:

Player picks gate 2 (initial choice).
Host must open gate 3, showing a goat (since gate 1 has the car).
Switching to gate 1 wins the car.
2. Car behind gate 2:

Player picks gate 2 (initial choice).
Host opens gate 3, showing a goat.
Switching to gate 1 loses, as the car is behind gate 2.
3. Car behind gate 3:

Player picks gate 2 (initial choice).
Host cannot open gate 3 because it has the car. Instead, he opens gate 1, showing a goat.
Switching to gate 3 wins the car.
Summary of outcomes:

In 2 out of 3 scenarios, switching wins the car.
In 1 out of 3 scenarios, staying with the initial choice wins.
As probability of winning a car by switching is higher than not switching. It is advantage to switch.

## Strategy for a 2 Player Coin Game

Consider a two-player coin game with an even number of coins in a row. Players A and B alternately pick one coin from any one end. The player who collects the greater total value wins. Develop a strategy for the player making the first turn i.e, Player A, that guarantees A never loses.

Note that a greedy strategy (always picking the larger end coin) may fail.

Initial row:  18, 20, 15, 30, 10, 14
Player A picks 18, now row of coins is: 20,15,30,10,14

After first pick:  20 ,15, 30, 10, 14
Player B picks 20, now row of coins is: 15,30,10,14

After second pick:  15 ,30 ,10, 14
Player A picks 15, now row of coins is

After third pick:  30, 10, 14
Player B picks 30, now row of coins is

After 4th pick:  10 ,14
Player A picks 14, now row of coins is

Last pick:  10 
Player B picks 10, game over.

The total value collected by Player B is more (20 + 
30 + 10) compared to first player (18 + 15 + 14).
So the second picker, Player B wins. 


**Solution** -

The Player A should always start picking all the even position ones so he can win, so from righ side it would give us all even position ones booked.

The idea is to add up the values at even positions and odd positions, then compare the two. The first player can always force the game so that the opponent gets only one of these two sets of coins, depending on which set has the smaller total.

So here are the steps to a proper algorithm of either winning the game or getting a tie:

Step 1: Count the sum of all the coins in the even places(2nd, 4th, 6th and so on). Let the sum be "EVEN".

Step 2: Count the sum of all the coins in the odd places(1st, 3rd, 5th and so on). Let the sum be "ODD".

Step 3: Compare the value of EVEN and ODD and this is how the first player, here Player A must begin its selection.

if (EVEN > ODD), start choosing from the right-hand corner and select all the even placed coins.
if (EVEN < ODD), start choosing from the left-hand corner and select all the odd placed coins.
if (EVEN == ODD), use a dynamic strategy to maximize the value based on the immediate and subsequent possible values (see approach below).
Example:

Suppose you are given the following rows of coins:

``18, 20, 15 ,30, 10, 14``

Coins at even places: 20, 30, 14 Coins at odd places: 18, 15, 10 These places are fixed independent of whether the choice of selection must begin from the left or the right-hand side. 

Step 1: Sum of all even placed coins = 20 + 30 + 14 = 64 

Step 2: Sum of all odd placed coins = 18 + 15 + 10 = 43 

Step 3: Comparing the even and the odd placed coins where EVEN > ODD.

Therefore, Player A must start selecting from the right-hand side and choose all the even-placed coins every time(here they are 14, 30 and 20).
So first picker, Player A picks 14. Now, irrespective of whether the second Player B starts selecting from the left-hand side i.e., 18 or from the right-hand side i.e., 10, the even placed coins i.e., 14, 30 and 20 are booked for the Player A.
Therefore, be it any situation that arises, the first picker Player A will always win the game. 



Case 1: When Player B starts picking from the left corner.

Case 2: When Player B starts picking from the right corner after Player A.

Dynamic Strategy for EVEN = ODD:

When EVEN = ODD, Player A should dynamically evaluate the potential outcomes of the first few moves and choose the highest immediate benefit while considering the opponent's optimal responses.

Example:

Suppose you are given the following rows of coins:

``5, 2, 3, 4, 2, 4``

Sum of even-placed coins: ``2 + 4 + 4 = 10``
Sum of odd-placed coins: ``5 + 3 + 2 = 10``
In this case, since EVEN == ODD, Player A should dynamically choose based on immediate benefit:

Player A picks 5 (left end), remaining: ``2, 3, 4, 2, 4``
Player B picks 4 (right end), remaining: ``2, 3, 4, 2``
Player A picks 2 (left end), remaining: ``3, 4, 2``
Player B picks 2 (right end), remaining: ``3, 4``
Player A picks 4 (right end), remaining: `3`
Player B picks 3, game over.

Totals:

Player A: 5 + 2 + 4 = 11
Player B: 4 + 2 + 3 = 9

Player A wins.
