# Counterbalancing Program
No one wants order effects messing around in their methodology. This is a command line Python program to automatically counterbalance the order of conditions. You input the number of conditions and the number of participants, and the program will output the most optimal set of orderings for the given number of participants.

## Contents:
  * [How it works](#how-it-works)
  * [How to run](#how-to-run)
    + [How to run on your PC](#how-to-run-on-your-pc)


## How it works
Basically, the program compares two permutatons and scores the difference (larger difference = larger score). For example, if you have [1, 2, 3, 4], the sequence [4, 3, 1, 2] will score higher than [1, 2, 4, 3] since the positions of the conditions has changed more. It does this for every possible ordering of conditions and you end up with an N sized subset of orders (where N = number of participants). The distribution of conditions across this subset is listed in the final output and there will be a maximum of 1 difference in the amount of times a condition is in a certain position. Within the subset itself, the program also ensures there are no patterns within the orders that it selected. This means that, for example, condition 1 will not be followed by condition 3 multiple times (or more than is necessary).  


The final output looks like this:

```
Final list:
(1, 4, 3, 2)
(2, 3, 4, 1)
(4, 2, 1, 3)
(3, 1, 2, 4)
(4, 3, 2, 1)
(1, 2, 3, 4)
(2, 4, 1, 3)
Count of each condition per position:
1: [2, 1, 1, 2]
2: [1, 2, 2, 1]
3: [1, 2, 2, 1]
4: [2, 1, 1, 2]
```
Here you can see the final subset of orders, and also the amount of times each condition appears in each position.
When you run the program you will see a lot of other stuff print out before this final output - you can ignore all this. It's just to show what the computer is doing to get to the final answer.  


**Note:** The more conditions and participants you have, the longer it'll take to run.

## How to run
Command line can be intimidating, so you can use these links to to run the program in your web browser instead :)


For the full program use [this link](https://py2.codeskulptor.org/#user48_IGMEb8Teln_1.py ) 


For the faster version use [this link](https://py2.codeskulptor.org/#user48_dSOzRVwd5r_0.py). However, speed comes at a cost. This one doesn't monitor the distribution of conditions per position so you might get condition 1 appearing first three times, but condition two appears first only once. Use the first link if you want to ensure the position distribution differs by a max of 1.  


Press the little play icon on the left of the blue menu bar to run the program. You should get a pop-up asking for the number of conditions and then another one asking for the number of participants.  

Running it through the link can sometimes be a lot slower than running it on your own PC. It's fine if you have a small number of conditions and participants (around 5 conditions and 12-15 participants). If you have a large amount of participants or conditions, the universe might die before it finds an answer, so I highly reccommend you download the file and run it yourself to expedite the process.  

### How to run on your PC

**1.** Make sure Python 3 is installed on your computer https://www.python.org/downloads/

**2.** Download permutations.py using the green "Code" download button above and download the ZIP file.

**3.**  Extract permutations.py to a place of your choice, e.g. downloads folder. Make a note of the file path location of wherever it saved e.g. C:\Users\Alice\Downloads

**4.**  This program runs through command prompt. Press the windows key + R on your keyboard and then type “cmd”. Alternatively, go to your taskbar, click the search button and search for command prompt. Command prompt is known as Terminal on Mac (see here if you're stuck on Mac https://support.apple.com/en-gb/guide/terminal/apd5265185d-f365-44cb-8b09-71a064a42125/mac)

**5.**  In the command prompt, type "cd C:\Users\Alice\Downloads" without the quotes but replace the file path with your path that you made a note of earlier. Then press enter (on your keyboard)

![command prompt](https://i.ibb.co/mGd81ps/cmd1.png)

**6.**  Then type "python permutations.py" and press enter on your keyboard to run the program

![command prompt2](https://i.ibb.co/R3QzJ7M/cmd2.png)

**7.** It will ask you for the number of conditions, then number of participants, and finally calculate the optimal orderings from all possible permutations. The final output will look something like this (depending on how many conditions and participants you have):

![command prompt2](https://i.ibb.co/xqfxV5L/cmd3.png)
