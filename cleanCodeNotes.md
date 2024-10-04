# Clean Code by Robert C. Martin - Personal Notes

This document contains my personal takeaways from each chapter of "Clean Code" by Robert C. Martin. I've supplemented some of the points in the book with extra research and references. 

## Table of Contents
- [Chapter 1: Clean Code](#chapter-1-clean-code)
- [Chapter 2: Meaningful Names](#chapter-2-meaningful-names)
- [Chapter 3: Functions](#chapter-3-functions)
- [Chapter 4: Comments](#chapter-4-comments)
- [Chapter 5: Formatting](#chapter-5-formatting)
- [Chapter 6: Objects and Data Structures](#chapter-6-objects-and-data-structures)
- [Chapter 7: Error Handling](#chapter-7-error-handling)
- [Chapter 8: Boundaries](#chapter-8-boundaries)
- [Chapter 9: Unit Tests](#chapter-9-unit-tests)
- [Chapter 10: Classes](#chapter-10-classes)
- [Chapter 11: Systems](#chapter-11-systems)
- [Chapter 12: Emergence](#chapter-12-emergence)
- [Chapter 13: Concurrency](#chapter-13-concurrency)
- [Chapter 14: Successive Refinement](#chapter-14-successive-refinement)
- [Chapter 15: JUnit Internals](#chapter-15-junit-internals)
- [Chapter 16: Refactoring SerialDate](#chapter-16-refactoring-serialdate)
- [Chapter 17: Smells and Heuristics](#chapter-17-smells-and-heuristics)

---

## Chapter 1: Clean Code

- It's not easy to write clean code.
- Later = never.
- Clean code is focused, it does one thing well.
  - Single Responsiblity Principle:
    - A class should have one reason to change (avoid GOD classes), 'separate the responsibilities'
    - It should have a single responsiblity, lest the code becomes to rigid to change later on.
- Clean code is easy for other people to enhance.
- Easy to read != ready to change.
- Clean code is easier to test.
- Your code should look like it was written by someone who cares.
- We read code far more than we write it.
- Leave the campground cleaner than you found it.
- Less != better.
  

## Chapter 2: Meaningful Names

- Change them when you find better ones.
- A name should indicate: why something exists, what it does and how it is used.
  - Should NOT require a comment.
- Avoid prefixes, small variations and un-pronouncable variable names.
- There's nothing wrong with a longer name (performance in some languages?).
- Class names should be nouns, methods should be verbs/ verb phrases
- Standardise word concepts (fetch vs retrieve vs get).

## Chapter 3: Functions

- They should be small, and smaller.
  - I don't agree with the extent that the book inists on one line functions.
  - Blocks within IF ELSE should be function calls
  - Avoid more than 2 nested layers.
- How can you tell if a function has a single responsibility (or too many)?
  - Should only do things stated in the name or a single level below.
  - If you have comments splitting them up, they should probably be separate.
  - Same level of abstraction. (I don't think this is crucial)
  - Should not be able to meaningful extract methods without major changes in the code.
  - Try to avoid switch statements.
  - Open Closed Principle: Classes, modules, functions should be open for extension but not modification.
  - https://gist.github.com/dmmeteo/f630fa04c7a79d3c132b9e9e5d037bfd#file-1-srp-py-L38
  - Avoid more than 3 arguements for a function (easier for testing, idealy none).
  - For transform functions, return the transform.
  - Avoid flag arguements, complicates structure.
  - Could a dyadic function be converted to a method?
  - A function should only change the state of it's own object.
  - Function should either do something or return and ans, not both!
    - Error handling is a 'thing' (need to think more about this).
  - Writing 'good' functions is an iterative process.
    
## Chapter 4: Comments

- Comments compensate for a failure to express our ideas in code
  - If you have to write a comment, there is liekly an alternative way.
- !!!! Comments are not refactored and will go out of date !!!!!
- Comments don't ammend bad code.
- Well named functions can reduce the risk of misinformation.

## Chapter 5: Formatting

- Related concepts should be vertically close.
- Instance variables at the top of the class / function (similar to how it is done in React).
- Dependant functions should be close to each other.

## Chapter 6: Objects and Data Structures

- Don't want to expose the details / implementations of our data.
  - Return percentageFuel over fuelInGallons + capacityInGallons
  - Requires thought.
- Objects hide data and expose implementations.
- Data structures expose data and have no meaningful functions.
- Avoid creating hybrids that encapsualte data and methods, muddled design.
- Law of Demeter: Need to work on this more.
- If we need to get a vavriable from an object with real behaviour, why not make that a method for the object?

## Chapter 7: Error Handling

- Exceptions make code easier to read, they define a scope.
- Wrap 3rd party API calls, to minimise dependancy and easier mocking.
- Special Case Pattern Fowler: Instead of returning 'null', just throw a specialised version of the object. Similar to the 'null case object pattern.
- Avoid null, as it just adds more work.
- Hard to deal with passing in null arguements, forces more checking.
- Avoid checked exceptions due to verbosity and violates (?) OCP.

## Chapter 8: Boundaries

- 

## Chapter 9: Unit Tests

- 

## Chapter 10: Classes

- 

## Chapter 11: Systems

- 

## Chapter 12: Emergence

- 

## Chapter 13: Concurrency

- 

## Chapter 14: Successive Refinement

- 

## Chapter 15: JUnit Internals

- 

## Chapter 16: Refactoring SerialDate

- 

## Chapter 17: Smells and Heuristics

- 

---
