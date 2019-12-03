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

## Day 3


**Gaps in knowledge to rectify**

## Day 4

**Gaps in knowledge to rectify**


## Day 5


**Gaps in knowledge to rectify**
