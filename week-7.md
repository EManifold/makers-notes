# Week 5

[Day 1](#day-1) | [Day 2](#day-2) | [Day 3](#day-3) | [Day 4](#day-4) | [Day 5](#day-5)

## Goals for the week


## Day 1


**Gaps in knowledge to rectify**  


## Day 2


**Gaps in knowledge to rectify**

## Day 3

### JavaScript Event Loop Workshop
- Single threaded languages have one call stack

### Tech CV Workshop
- Say you're a software developer on your cv, not 'aspiring' software dev etc
- Employers need to know why software development is important to you, not just 'it's where i ended up' etc
- Blog post: 'How I evaluate developers for my team' on makersacademy
- Choose 2-5 skills (3 is best) skills to talk about, e.g. discipline, creative problem-solving, writing, organisation, community
- Keep work experience relevant
- Summarise your previous role in a sentence
- Don't go back earlier than the degree (i.e. a-levels)

**Gaps in knowledge to rectify**

## Day 4

### JavaScript Module Pattern Workshop

Why use the module pattern?
- Module pattern solves the problem of encapsulation, JavaScript as a language doesn' thave proper support for making things private. Using an underscore makes thing private but is just a naming convention which tells other devs to 'make this thing private', but doesn't actually make it private automatically. 
- Module pattern good for reusing code. Can write them once and share them in a few places if the functions are generic enough to use elsewhere.
- These two above are the most common reasons for using the module pattern in JS.

What is a closure?
- Bundling functionality with the scope in which it lives. If we were to define a function in JS, it would have acess to all the variables in the scope in which it was created. BUndling the state/environment together.
- A good use of closures is what makes the module pattern so effective. 

``` let myModule = (function() {
      function _privateMethod() {
      reutrn "Hello World!"
      }
      function publiccMethod() {
      return _privateMethod()
      }
      return {
        publicMethod: publicMethod
      }
      })()
      
      myModule.publicMethod() // 'Hello World!'
      myModule._privateMethod() // error
      ```
      
      These returns are 'unusual' because the public method works while using the private method, but you can't call the private method. This is because of the use of closures. Private method was in the public method's closure. 



**Gaps in knowledge to rectify**


## Day 5


**Gaps in knowledge to rectify**
