# Speed Networking Pairing Problem:
My wife is hosting a speed networking event on belhalf of her employer. For this event, there is availability for 20 participants. These **20 participants** will form **10 groups of 2** and spend ~5 minutes in each group. Once the time limit expires, the participants will then form another 10 groups of 2 for the following 5 minutes. This process will repeat until every participant has a ~5 minute networking session with **Every** other participant. Since this is __*Speed* Networking__, two separate participants can only join **one** group together throughout the entire process. To clarify, no two participants will meet twice.

### Goal:
Make a simple method to form these groups where there is a logical flow between each cycle

### Notes:<br>This is a combinatorics problem.

Let each participant be defined as a unique member of the set of postitive integers $[1,20].$<br>
The full set of `groups` are defined as $All\ Groups$
$$ All\ Groups={1,\ 2,\ 3,\ ...,\ 18,\ 19,\ 20  \choose 2}$$

The library itertools has a combinations subclass to simplify the process. This will return the full unique set of groupings that will be used throughout the Networking Event.

## Questions:
- How many total groups are there throughout the networking event?
- How many `rounds` are needed for all 20 participants to network with everyone exactly **once**
- What should the process that shifts rounds look like

# Reults:

---------------------------------------------------------------------------
Round 1
[ 1, 11]
[ 2, 12]
[ 3, 13]
[ 4, 14]
[ 5, 15]
[ 6, 16]
[ 7, 17]
[ 8, 18]
[ 9, 19]
[10, 20]
---------------------------------------------------------------------------
Round 2
[ 1, 12]
[11, 13]
[ 2, 14]
[ 3, 15]
[ 4, 16]
[ 5, 17]
[ 6, 18]
[ 7, 19]
[ 8, 20]
[ 9, 10]
---------------------------------------------------------------------------
Round 3
[ 1, 13]
[12, 14]
[11, 15]
[ 2, 16]
[ 3, 17]
[ 4, 18]
[ 5, 19]
[ 6, 20]
[ 7, 10]
[ 8,  9]
---------------------------------------------------------------------------
Round 4
[ 1, 14]
[13, 15]
[12, 16]
[11, 17]
[ 2, 18]
[ 3, 19]
[ 4, 20]
[ 5, 10]
[ 6,  9]
[ 7,  8]
---------------------------------------------------------------------------
Round 5
[ 1, 15]
[14, 16]
[13, 17]
[12, 18]
[11, 19]
[ 2, 20]
[ 3, 10]
[ 4,  9]
[ 5,  8]
[ 6,  7]
---------------------------------------------------------------------------
Round 6
[ , 16]
[1, 17]
[1, 18]
[1, 19]
[1, 20]
[1, 10]
[ ,  9]
[ ,  8]
[ ,  7]
[ ,  6]
---------------------------------------------------------------------------
Round 7
[ 1, 17]
[16, 18]
[15, 19]
[14, 20]
[13, 10]
[12,  9]
[11,  8]
[ 2,  7]
[ 3,  6]
[ 4,  5]
---------------------------------------------------------------------------
Round 8
[[ 1 18]
[17 19]
[16 20]
[15 10]
[14  9]
[13  8]
[12  7]
[11  6]
[ 2  5]
[ 3  4]
---------------------------------------------------------------------------
Round 9
[ 1, 19]
[18, 20]
[17, 10]
[16,  9]
[15,  8]
[14,  7]
[13,  6]
[12,  5]
[11,  4]
[ 2,  3]
---------------------------------------------------------------------------
Round 10
[ 1, 20]
[19, 10]
[18,  9]
[17,  8]
[16,  7]
[15,  6]
[14,  5]
[13,  4]
[12,  3]
[11,  2]
---------------------------------------------------------------------------
Round 11
[ 1, 10]
[20,  9]
[19,  8]
[18,  7]
[17,  6]
[16,  5]
[15,  4]
[14,  3]
[13,  2]
[12, 11]
---------------------------------------------------------------------------
Round 12
[ 1,  9]
[10,  8]
[20,  7]
[19,  6]
[18,  5]
[17,  4]
[16,  3]
[15,  2]
[14, 11]
[13, 12]
---------------------------------------------------------------------------
Round 13
[ 1,  8]
[ 9,  7]
[10,  6]
[20,  5]
[19,  4]
[18,  3]
[17,  2]
[16, 11]
[15, 12]
[14, 13]
---------------------------------------------------------------------------
Round 14
[ 1,  7]
[ 8,  6]
[ 9,  5]
[10,  4]
[20,  3]
[19,  2]
[18, 11]
[17, 12]
[16, 13]
[15, 14]
---------------------------------------------------------------------------
Round 15
[ 1,  6]
[ 7,  5]
[ 8,  4]
[ 9,  3]
[10,  2]
[20, 11]
[19, 12]
[18, 13]
[17, 14]
[16, 15]
---------------------------------------------------------------------------
Round 16
[ 1,  5]
[ 6,  4]
[ 7,  3]
[ 8,  2]
[ 9, 11]
[10, 12]
[20, 13]
[19, 14]
[18, 15]
[17, 16]
---------------------------------------------------------------------------
Round 17
[ 1,  4]
[ 5,  3]
[ 6,  2]
[ 7, 11]
[ 8, 12]
[ 9, 13]
[10, 14]
[20, 15]
[19, 16]
[18, 17]
---------------------------------------------------------------------------
Round 18
[ 1,  3]
[ 4,  2]
[ 5, 11]
[ 6, 12]
[ 7, 13]
[ 8, 14]
[ 9, 15]
[10, 16]
[20, 17]
[19, 18]
---------------------------------------------------------------------------
Round 19
[ 1,  2]
[ 3, 11]
[ 4, 12]
[ 5, 13]
[ 6, 14]
[ 7, 15]
[ 8, 16]
[ 9, 17]
[10, 18]
[20, 19]
