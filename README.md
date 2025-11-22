### Objects with Dynamically Allocated Members

This project implements a dynamic List class of double values as required in Lab 5 and Lab 11.
The class is built around a manually-managed dynamic array (double* list_) and an integer size counter (size_). 
As a CS student, the goal of this lab was to demonstrate correct use of dynamic memory, deep copying, and object lifetime management.

## Components I implemented

# Core List Functionality

- Check(double) - Search that returns the index of a value or -1 if not found
- addNumber(double) - Prevents duplicates, allocates a new array of size+1, copies existing elements, appends the new value, and replaces the old array.
- removeNumber(double) - Locates a value, allocates a reduced array, copies remaining elements, deletes old memory.
- output() - Prints the contents of the array in a bracketed format.

# Big Three (For Dynamic Memory)
-Copy Constructor - _Deep_ copies the source list
-Overloaded assignment operator - handles self-assignment, deletes old memory, then makes a copy.
-Destructor - Frees allocated memory and nulls the pointer

# Included Test Programs
- Lab5_ListTest tests all functionality, validates duplicate handling, removal, deep copy behavior, stackable assignment and destructor correctness. Provided by Dr. Mikhail Nesterenko.
- Lab11_ListClasses provides implementation for user input, where the user can add or remove numbers and the program reports duplicates and prints the list state.
