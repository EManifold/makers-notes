# Week 1

## Goals for the week

- Test-drive a simple program using objects and methods
- Pair using the driver-navigator style
- Follow an effective debugging process
- Describe some basic OO principles like encapsulation, SRP

## Day 2

### Skills Workshop

Fixing a bug:
- Understand the problem
- Tighten the loop
- Get visibility using ``` p ```

Different types of errors:
- Syntax Error - problem with the syntactic structure of your code so the compiler doesn't know what went wrong
- Runtime Error - e.g. a Name Error, an uninitialized constant where you haven't declared a variable before using it
- Program doesn't terminate - e.g. infinite loop
- Unexpected results - the program doesn't do what you expect it to do

### Pair Programming - Boris Bike Challenge

Achieved up to Step 10 with Charlie

Gaps in knowledge to rectify:
- The difference between a Unit test and a Feature test
- What a Domain Model is and how the above relate to it

## Day 3

### Goal Setting
- Go forward with the resources provided for Week 1
- Fill in the gaps in my knowledge from yesterday, research the above topics
- Explain these concepts to a friend at the end of independent learning
- Organise my files

### Independent Learning

**Domain Model**
- The domain model is the structure of your program, how the objects relate to the messages. 
- An example of a domain model would be in a company you have the categories of Manager, Employee, and Person. Person encapsulates Manager and Employee, whereas Employee does not necasserily include Manager, and so on and so forth. 
- An accurate domain model guides how user stories (the specification of what the program should do, provided by the client and broken down into 'user stories') are translated into classes. 

**Feature Testing**
- Feature testing tests what the product and new feature does what it's supposed to do, and whether it's integrated effectively.
- Used when software developers release a new feature to their product. 
- Feature testing is encouraged to be undergone earlier in the process, so that all possible problems are caught before they arise. 
- Testing co-operation between different modules of the software.
- Functionality vs state - feature testing should test how whether an aspect of the code does what it's supposed to do, not the way in which it does it (state). 

**Unit Testing**
- Unit testing is where each bit of the software is tested. 
- This prevents unexpected bugs arising later on. 
- Unit testing improves confidence in changing or mainting your code, to ensure that it's what you write to start with is not set in stone and unchangeable. 
- We use rspec to carry out unit testing. 

## Day 4

## Day 5

## Weekend Challenge
