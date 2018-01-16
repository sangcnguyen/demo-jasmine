## Jasmine

[Jasmine](https://jasmine.github.io/) is a javascript testing framework that supports a software development practice called
[Behaviour Driven Development](https://en.wikipedia.org/wiki/Behavior-driven_development), or BDD for short. It’s a specific flavour of [Test Driven Development](https://en.wikipedia.org/wiki/Test-driven_development) (TDD).<br/>
For example if you wanted to test this function:
```
function(number1,number2) {
    return number1 + number2;
}
```
You would write a jasmine test spec like so:
```
describe('Calculator', () => { (1)
  it('sums 1 and 1 to 2', () => { (2)
  var calc = new Calculator(); 
  expect(calc.sum(1, 1)) (3)
      .toEqual(2); (4)
  });
});
```
(1) The **describe(string, function)** function defines what we call a Test Suite, a collection of individual Test Specs.<br/>
(2) The **it(string, function)** function defines an individual Test Spec, this contains one or more Test Expectations.<br/>
(3) The **expect(actual)** expression is what we call an Expectation. In conjunction with a Matcher it describes an expected piece of behaviour in the application.<br/>
(4) The **matcher(expected)** expression is what we call a Matcher. It does a boolean comparison with the **expected** value passed in vs the **actual** value passed to the **expect** function, if they are false the spec fails.

## Build-in matchers

MATCHERS         | PURPOSE
------------     | -------------
toBe()           | passed if the actual value is of the same type and value as that of the expected value. It compares with === operator
toEqual()        | works for simple literals and variables;
toMatch()        | to check whether a value matches a string or a regular expression
toBeDefined()    | to ensure that a property or a value is defined
toBeUndefined()  | to ensure that a property or a value is undefined
toBeNull()       | to ensure that a property or a value is null
toBeTruthy()     | to ensure that a property or a value is `true`
toBeFalsy()      | to ensure that a property or a value is `false`
toContain()      | to check whether a string or array contains a substring or an item
toBeLessThan()   | for mathematical comparisons of less than
toBeGreaterThan()| for mathematical comparisons of greater than
toBeCloseTo()    | for precision math comparison
toThrow()        | for testing if a function throws an exception
toThrowError()   | for testing a specific thrown exception

The Jasmine `not` keyword can be used with every matcher’s criteria for inverting the result. 
E.g.
`expect(actual).not.toBe(expected);`<br/>
`expect(actual).not.toBeDefined(expected);`

## Setup and teardown
Sometimes in order to test a feature you need to perform some setup, perhaps it’s creating some test
objects. Also you may need to perform some cleanup activities after you have finished testing,
perhaps you need to delete some files from the hard drive.<br/>
These activities are called setup and teardown (for cleaning up) and Jasmine has a few functions you
can use to make this easier:<br/>
**beforeAll**<br/>
This function is called once, before all the specs in describe test suite are run<br/>
**afterAll**<br/>
This function is called once after all the specs in a test suite are finished.<br/>
**beforeEach**<br/>
This function is called before each test specification, it function, has been run.<br/>
**afterEach**<br/>
This function is called after each test specification has been run.<br/>

## Running Jasmine tests
To run Jasmine tests you would download [a jasmine standalone zip](https://github.com/jasmine/jasmine/releases) from github and include javascript like so: 
```
 <!-- include source files here... -->
 <script src="src/MathUtils.js"></script>
 <!-- include spec files here... -->
 <script src="spec/MathUtils.js"></script>
```

## References
* <https://jasmine.github.io/edge/introduction.html#section-Included_Matchers>
* <https://howtodoinjava.com/scripting/javascript/jasmine-javascript-unit-testing-tutorial/>
