# Practice problems
### General Approach
For each drill,
- pseudocode your solution
- assign the input to a variable
- write the function
- invoke the function, assigning the return value to a new variable
- `console.log` the result

Example setup:
```
const inputValue = <the specified input>

function mySolution(parameterName) {
  // make the magic happen
  return myReturnValue
}

const outputValue = mySolution(inputValue)
console.log(outputValue)
```
This setup gets even better with quokka! Search for it in your vscode extensions market

Tips:
- Pseudocode until your steps are simple and easily translatable into code.
- Set up the above framework for a problem before you start building out the function
- Take baby steps and check your output after each one

### digDown: tests recursion
Imagine an array that is guaranteed to have length 1, ie it contains just a single element. That element will be either a string or an array. If it's an array, it will contain just a single element, and that single element will be either a string or an array. And so on: that array will contain just one element, which could be a string or an array... to create a russian nesting doll array of unknown depth of layers. One example of such an array is below. Before moving on, take a minute to draw a few similar arrays of your own.

```js
[
  [
    [
      ["hi"]
    ]
  ]
]
```

Write a function called digDown that accepts a nested array of unknown depth as an argument. digDown drills down through the nested array until it finds the string, and returns the string.

Implement digDown twice, once using a loop and once using recursion. (You can give them different names, like digDownLoop and digDownRecursion.) They should both result in exactly the same output. Do whichever makes more sense first! Hot tip: after defining your function, test drive it on several test cases.

Next level: once you have digDown working with both a loop and recursion, enhance both functions as follows. Instead of returning just the string at the core of the array, your function should return an object like this:

```js
{
  target: "hi",
  layers: 4 // this is the number of layers that we had to dig through to find it. the above example had 4 layers of arrays
}
```

### multipleLengths: generic workout
Given: an array of strings, for example `['hey', 'whoa', 'whoooaaa']`
<br>
Expect: an object with those strings as keys, and the length of each string as a value, for example
```
{
  hey: 3,
  whoa: 4,
  whoooaaa: 8
}
```

### vowelCount: generic workout
Given: an array of strings, for example `['hey', 'whoa', 'whoooaaa']`
<br>
Expect: an object with those strings as keys, and the number of vowels in each string as a value, for example
```
{
  hey: 1,
  whoa: 2,
  whoooaaa: 6
}
```

### justTheNames: generic workout
Given: an array of objects that contain person data, for example:
```
[
  {
    name: 'Joel',
    state: 'CO'
  },
  {
    name: 'Ryan',
    state: 'NJ'
    },
  {
    name: 'Pete',
    state: 'GA'
  },
  {
    name: 'Dexter',
    state: 'GA'
  },
]
```


Expect: an array containing just the name values, for example:

```js
['Jordan', 'Mike', 'Pete', 'J']
```

### shortNamesOnly: generic workout
Given: an array of person data (same as justTheNames)
Expect: an array containing just the name values that are less that 4 characters in length, for example: `['Ryan', 'Pete', 'Joel']`
Tip: your answer to `justTheNames` should help! Look for a clever way to reuse it

### fizzBuzz: generic workout
Given: a single number `inputNumber`
- Expect: an object that contains 3 keys: 'fizz', 'buzz', and 'fizzBuzz'. Each key points to an array. The 'fizz' array should contain all number less than or equal to `inputNumber` that are multiples of 3. The 'buzz' array should contain all number less than or equal to `inputNumber` that are multiples of 5. The 'fizzBuzz' array contains all numbers less than or equal to `inputNumber` that are multiples of both 3 and 5.

Example input: `20`

Example output:

```
{
  fizz: [3, 6, 9, 12, 15, 18],
  buzz: [5, 10, 15, 20],
  fizzBuzz: [15]
}
```

### turtleBuilder: generic workout

Given: the following 3 arrays

```
const names = ['Leonardo', 'Michelangelo', 'Raphael', 'Donatello']
const colors = ['blue', 'orange', 'red', 'purple']
const weapons = ['katanas', 'nunchuks', 'sais', 'bo staff']
```


Expect: the following array of objects

```
[
  {
    name: 'Leonardo',
    color: 'blue',
    weapon: 'katanas'
  },
  {
    name: 'Michelangelo',
    color: 'orange',
    weapon: 'nunchuks'
  },
  {
    name: 'Raphael',
    color: 'red',
    weapon: 'sais'
  },
  {
    name: 'Donatello',
    color: 'purple',
    weapon: 'bo staff'
  },
]
```

Tip: your function should take in 3 parameters, corresponding to the 3 input arrays


