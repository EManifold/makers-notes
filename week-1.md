# Week 1

[Day 2](#day-2) | [Day 3](#day-3) | [Day 4](#day-4) | [Day 5](#day-5) 

## Goals for the week

- Test-drive a simple program using objects and methods
- Pair using the driver-navigator style
- Follow an effective debugging process
- Describe some basic OO principles like encapsulation, SRP

## Day 2

### Debugging Workshop

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

**Gaps in knowledge to rectify**
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
- Unit testing is the practice of testing small pieces of code, typically individual functions, alone and isolated.
- This prevents unexpected bugs arising later on.
- Unit testing improves confidence in changing or mainting your code, to ensure that it's what you write to start with is not set in stone and unchangeable.
- We use rspec to carry out unit testing.

### Pair Programming Challenge - Boris Bikes

Reached challenge 13 with David

**Gaps in knowledge to rectify**
- attr_reader
- Use of instance variables within classes
- The start of an rspec test where you write the code that should be carried out

## Day 4

### TDD Workshop

Production code = the code of the software that is shown to the client. Code that is ready to deploy to the client. Doesn't mean that it's finished because you could still be working on it to add more features, but happy to show what you have to the client.

What is TDD and why do we use it?
- The process of writing tests to guide the writing of code that meets user needs.
- It helps break down the problem
- Tests can serve as documentation
- Acts as a safety net (tests in general, not necasserily TDD)

**PiggyBank Program**

Steps:
1. Define user needs
2. Write user stories
3. Domain
4. Write a feature test
5. Write a unit test, fail it and make it pass
6. Refactor


User needs
- Store money
- Discourage people from taking it out
- Destroy + taking all the money out
- Shaking it tells us if there is money

User stories:

--

As a user - (WHO'S DOING THE ACTION)  
So I can save up money - (CONTEXT, WHO MAY DO THIS AND WHAT PURPOSE DO THEY HAVE IN MIND)  
I want to store it - (THIS IS THE LINE WE'RE INTERESTED IN)  

As a user  
So I can spend money  
I want to take money out of the piggy bank  

--

Nouns: USER, MONEY, PIGGY BANK  
Verbs: SAVE UP, STORE  

PiggyBank object  
Store method  


When you're testing something, you have to ask yourself 'what is the behaviour of the thing I want to test?'  
 => Use an input/output table  
 Once we've described the behaviour, we can use these to write our tests  


Feature test:

```
piggy_bank = PiggyBank.new
piggy_bank.store(1)
=> 'clink'

```

Input | Output
--- | ---
1 | 'clink'
2 | 'clink'
0 | nil

---------

```
piggy_bank = PiggyBank.new
piggy_bank.destroy
=> 0
```

Input | Output
--- | ---
pb.store(1) | 1
pb.store(1) && pb.store(2) | 3
new pb | 0

------------

piggy_bank_spec.rb:
```
require 'piggy_bank'

describe PiggyBank do
  describe '#store' do
    it 'should return "clink" when I store 1 pound' do
      piggy_bank = PiggyBank.new
      expect(piggy_bank.store(1)).to eq('clink')
    end

    it 'should return "clink" when I store 2 pounds' do
      piggy_bank = PiggyBank.new
      expect(piggy_bank.store(2)).to eq('clink')
    end

    it 'should return nil when I store 0 pounds' do
      piggy_bank = PiggyBank.new
      expect(piggy_bank.store(0)).to eq(nil)
    end
  end

  describe '#destroy' do
    it 'should return 1 when I had stored 1 pound in it' do
      piggy_bank = PiggyBank.new
      piggy_bank.store(1)
      expect(piggy_bank.destroy).to eq(1)
    end
  end
end
```

piggy_bank.rb:

```
class PiggyBank
  def store(amount)
    'clink' if amount > 0
  end

  def destroy
    1
  end
end
```

What's definitely needed in a unit test:
- expect => along with .to eq, .to raise_error or .to output
- describe
- it


3 stages of tests:
- Arrange - set up situation before actual test (before expect)
- Act - what you're doing to the thing (in expect brackets)
- Assert - what comes out of it



## Day 5

### Goals
- Refactor my BB rspec
- Watch Alice's screen recording
- Research earlier gaps in knowledge

### Independent Learning

**Birthday List Program**  
Program created as an exercise to help with methods, classes and testing.  

The program allows you to add a person (with their name and birthday), show the list of birthdays, and show who has a birthday today.

In repositories under 'birthday-list'.  
