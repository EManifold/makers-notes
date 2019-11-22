# Week 2

[Day 1](#day-1) | [Day 2](#day-2) | [Day 3](#day-3) | [Day 4](#day-4) | [Day 5](#day-5) | [Weekend Challenge](#weekend-challenge)

## Goals for the week

- Use all of week 1's skills (don't underestimate the importance of this)
- Break one class into two classes that work together, while maintaining test coverage
- Unit test classes in isolation using mocking
- Explain some basic OO principles and tie them to high level concerns (e.g. ease of change)
- Review another person's code and give them meaningful feedback

## Day 1

### Code review

Reasons to review code:
- Improve the code (Refactor, readability)
- Learn (solve problems, spot patterns)

Reasons to do peer review code:
- Improve communication skills
- Part of pair programming
- Learning from eachother

### Process Workshop

My feedback:  
Read instructions v carefully - good  
Jumped straight into creating code first - could think about starting with tests  
Use of online REPL - good  
Started working with first test that passed - could think about starting with simplest test and building up in complexity  
Jumped straight into quite complicated solution (if statements, loops) - demonstrates confidence fluency in coding, but not TDD process  
Used existing tests to test your solution - good  
Looked for other methods to refactor code (switch statements) - good  
Tested code after introducing new method - good  
Refactored to make methods shorter - good  
Could think about using your own tests 

**Gaps in knowledge to rectify**
- Stubs/mocks/doubles

## Day 2

### Feedback Workshop
1. Shift your perspective
- No positive or negative
- Feedback is kind

2. Empowered receiver
- Basically free therapy

3. Know thyself
- Truth triggers, relationship triggers, identity triggers
- Wrong-spotting

4. Understand feedback 
- Appreciation, evalution, coaching

5. Use a framework
- Actionable, specific, kind

**Gaps in knowledge to rectify**
- Mocks, stubs and doubles

## Day 3

Goals for the day:
- Learn more about mocks, stubs and doubles

### Domain Modelling Workshop

Google diagramming chart: Draw.io (if you want to present your diagram to other people)

Use makers > skills workshop > domain modelling walkthrough

using private methods in a test:

      expect{subject.send(:deduct, 1)}.to change{subject.balance}.by -1
      
## Day 4

**Gaps in knowledge to rectify**

- Dependency injection, forwarding and polymorphism


## Day 5

**Gaps in knowledge to rectify**
