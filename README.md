# sodoku_solver
Problem Statement:
Given a partially filled 9×9 2D array ‘grid[9][9]’, the goal is to assign digits (from 1 to 9) to the empty cells so that every row,
 column, and subgrid of size 3×3 contains exactly one instance of the digits from 1 to 9. 

Solution:
Create a function that checks after assigning the current index the grid becomes unsafe or not. Keep Hashmap for a row, column and boxes. 
If any number has a frequency greater than 1 in the hashMap return false else return true; hashMap can be avoided by using loops.
Create a recursive function that takes a grid.
Check for any unassigned location. 
If present then assigns a number from 1 to 9.
Check if assigning the number to current index makes the grid unsafe or not. 
If safe then recursively call the function for all safe cases from 0 to 9.
If any recursive call returns true, end the loop and return true. If no recursive call returns true then return false.
If there is no unassigned location then return true.
