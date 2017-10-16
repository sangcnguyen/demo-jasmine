## More Matchers

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
`expect(actual).not.toBe(expected);`
`expect(actual).not.toBeDefined(expected);`
