# Week 4

[Day 1](#day-1) | [Day 2](#day-2) | [Day 3](#day-3) | [Day 4](#day-4) | [Day 5](#day-5)

## Goals for the week

- Build a simple web app with a database
- Follow an effective debugging process for database applications
- Explain the basics of how databases work (e.g. tables, SQL, basic relationships)

## Day 1

### Code Review

- Change play again to get method
- Implement a score
- Refactor if else statement
- Go to play when play again instead of index, put home button instead

Group discussion:
- What's the difference between class method and instance methods?
- How do you access a class method's methods? 

Todo:
- Look at rubric
- Look at deeper learning objectives link

**Gaps in knowledge to rectify**  
SQL commands  

## Day 2

## Goals for today
- Learn SQL commands
- Plan a blog on doubles/stubs/mocks (write by end of week) 

### Independent Learning

Some basic SQL commands:
(From a table with name, population, area etc as columns)

SELECT name, population, area FROM world
WHERE area > 3000000
OR population > 250000000

SELECT name FROM world
WHERE name LIKE 'United%'

SELECT name, population 
FROM world
WHERE name IN ('France', 'Germany', 'Italy')

SELECT name, population/1000000
FROM world
WHERE continent = 'South America'

SELECT name, gdp/population
FROM world
WHERE population>200000000

SELECT name FROM world
WHERE population > 200000000

SELECT name, continent, population FROM world

SELECT name, population, area FROM world
WHERE area > 3000000
XOR 
population > 250000000
(XOR is for either but not both)

SELECT name, ROUND(population/1000000, 2), ROUND(gdp/1000000000, 2)
FROM world
WHERE continent = 'South America'

SELECT name, ROUND(gdp/population, -3)
FROM world
WHERE gdp > 1000000000000

SELECT name, capital FROM world
WHERE LENGTH(name) = LENGTH(capital)


SELECT name, capital FROM world
WHERE LEFT(name, 1) = LEFT(capital, 1) 
AND name <> capital
(<> is a NOT EQUALS sign)

SELECT yr, subject, winner FROM nobel
WHERE subject = 'Physics' AND yr = '1980' 
OR subject = 'Chemistry' AND yr = '1984'

More advanced commands:

SELECT name, continent FROM world
WHERE continent = (SELECT continent FROM world
                WHERE name = 'Argentina') OR
            continent = (SELECT continent FROM world
                WHERE name = 'Australia')
ORDER BY name

SELECT name, population FROM world 
WHERE population > 
    (SELECT population FROM world
     WHERE name = 'Canada') AND population <
        (SELECT population FROM world 
         WHERE name = 'Poland')
         
         
Environment variable:
do export NAME=PASSWORD in .bashrc
then call ENV[NAME] in your file

**Gaps in knowledge to rectify**
- Having a hash as a paramter/argument for a method, e.g. (url:)

## Day 3

### Class Responsibility Workshop

Learning Objectives:
- Explain how to use CRC cards to model a domain
- Model a simple domain using CRC cards
- Infer database structure from domain structure

![IMG_0508](https://user-images.githubusercontent.com/53044792/70140986-e9fb9400-168d-11ea-9f51-136887c832d3.JPG)

### My Process Workshop notes
Ellie's process workshop:
- Be more vocal and explain what you were doing 'going to pass the test', ''
TDD:
- Good set up on rspec
- Passing the test the simplest way good
- Expecting to fail the correct tests
Debugging:
- Expecting bugs and knowing how the tests will fail
Modelling:
- Good breakdown of the problem taking it step by step
- Trying to pass each acceptance criteria one by one good steps
- Identifying the edge cases good
Refactoring:
- Good at refactoring when you see a problem
- Clear variable names
- Not so readable but not given much time to refactor as the challenge was ongoing
Problem Solving:
- Good use of opening IRB and using it to help to solve the problem
- Good use of google to search for syntax


**Gaps in knowledge to rectify**

## Day 4

**Goals for the day**
- Go over my process workshop with Katarina

### Reviewing my process workshop
- Setup my spec file and write first test without lib set up (because e.g. might make a typo in lib and wouldn't show up if I'd started testing something else)
- Good running tests frequently, doing the simplest thing
- Could use black box testing to plan beforehand
- Use acceptance criteria more
- Good to hard code and see a pattern then refactor to fit the pattern
- Going through the motions of TDD instead of actually using tests usefully
- Need about 5 mins planning in a half hour session

Overall advice:
- Lack of planning, need to see input and output
- Should start with the simplest tests, but the ones that I used seemed the simplest to me but actually weren't the simplest. Need to use the tests to identify a pattern, e.g. test 'A', 'AA', 'AAA', 'AAAA' would show a pattern, and where I tested for 'A', 'B', 'C', 'D', this seems simpler but is actually more complicated because there's no pattern identified that can help you write your code. 

**Gaps in knowledge to rectify**


## Day 5


**Gaps in knowledge to rectify**
