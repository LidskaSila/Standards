# Testing

## JavaScript

It will take time to get to the nearly ideal status. New code should be made with tests and where possible tests will be added gradually or when we decide to refactor/rewrite some code, it will be accompanied with tests.

Running tests should be part of the git push to develop process (CI) and deployment (having develop branch "all green" all the time).


Testing generally consists of:

* Acceptance testing
* part of the app (mostly unit testing)
* code quality

React app consist generally from:

* reducers
* action and action creators
* selectors
* components
* helpers


Strategy for each one may be little bit different.


## Acceptance testing

Testing strategies that simulate real web pages and real users. They have to be tested on fully functional test copy of the production systems and web pages.

Supposed tools: Selenium and similar tools.

_david: I have very small practical experience with these tests_


## Tools

[Interesting article about AVA and Jest](https://medium.com/@kentcdodds/migrating-to-jest-881f75366e7e#.h6176qd25). Maybe we should try Jest - so any mentions here about AVA may mean Jest :).


### Reducers

Reducer are pure functions and unit tests are best tool.

Tool: AVA. 

We want 100% coverage here.



### Action and action creators

Testing standard actions seems to be redundant (they generate object with standard structure).

Testing thunk actions (actions that dispatch multiple actions or have side effects) is important, we want 100% coverage here.

Testing action creators (and bound action creators) is desirable if they do anything more complex than passing the data from one point to another point.

Tool: AVA.



### Selectors

They are pure functions.

We want 100% coverage.

Tool: AVA.



### Components

Testing of pure components depends on complexity of the component.

We do not want 100% coverage.

We should try to get nearly 100% coverage for HoC (higher order components) and for stateful components.

Tool: AVA + Enzyme



### Helpers

Helpers are usually simple functions and we want 100% coverage here.

Tool: AVA + Enzyme







## Tools

The structure of the AVA tests should have similar pattern, we agreed on. It may be verbose but it should be very easy to read. The reason is to reuse most of the patterns or templates for most of the tests.


### Acceptance testing


### Unit Testing

I recommend AVA. It is fast, doesn't bloat global scope. Tests may run in parallel.


### Component testing

I recommend using AVA + Enzyme. Enzyme is Airbnb tool and widely used.


### Other stack

Sinon to use spies and fake time.

For mocking up the API calls we can use simple tools (for mocking fetch for example), we can use static files with mocked responses and/or we can use testing tools for API (Apiary or other) or we can setup docker with testing API and testing data and run tests against it (should be probably used for acceptance tests).


_ THIS IS WORK IN PROGRESS_
