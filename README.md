# Cash Problem

## Note 

This was created as soiution for Problem Set #1 of CS50 Course Cash Problem (less comfortable version): https://cs50.harvard.edu/x/2023/psets/1/cash/

## Cash Problem using Greedy Algorithm in C

This is a C program that solves the cash problem using the greedy algorithm. Given a cash amount and a set of coin denominations, the program determines the minimum number of coins needed to make the change.
For instance, if some customer is owed 41¢, the biggest first (i.e., best immediate, or local) bite that can be taken is 25¢. (That bite is “best” inasmuch as it gets closer to 0¢ faster than any other coin would.) 

## Getting Started
### Prerequisites
* C compiler ( C compiler(GCC, Clang, etc.) Note: Personally I recommend using Clang or Clangd compiler and it's extension for VS Code
* CS50 Library installed on your machine(detailed installation information can be found here: https://cs50.readthedocs.io/libraries/cs50/c/)

## installation 

1. Clone the Repository:
` git clone https://github.com/Kate-h36/Cash.git`
2. Open a terminal window and navigate to the cloned directory.
3. Compile and linking the program by running:
`clang -o cash cash.c -lcs50`
4. Run program by:
`make cash` and `./cash`

## Usage 

The program prompts the user to enter a cash amount and a set of coin denominations. For example:

`$ ./cash`
`Change owed: 41`
`4`

if the user doesn’t, in fact, input a positive integer  when prompted the program should re-prompt the user:

`$ ./cash`
`Change owed: -41`
`Change owed: foo`
`Change owed: 41`
`4`

The program also must output the minimum number of coins needed to make the change. 
For exaple if you input `99` program should outputs `9` ('cause this is three quarters, two dimes, and four pennies)

## Algorithm
The algorithm works as follows:

 * Sort the coin denominations in descending order.
 *  While the cash amount is greater than 0, do the following:
 
1. Take the largest coin denomination that is less than or equal to the cash amount.
2. Subtract the coin denomination from the cash amount.
3. Increment the count of the number of coins used.
 
 The algorithm is guaranteed to produce the optimal solution for US coin denominations, which are 1, 5, 10, and 25 cents.
