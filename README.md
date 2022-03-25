# Programming Exercise

Your task is to figure out how this code works.

* Come with a test input for the function.
* Trace the flow of the program with your test input **without running the code**, keeping track of all of the variables and transformations until you can determine the output.
* Keep coming up with new inputs until you're confident until you're confident that you know how the function works.
* Write a summary of what the function does.

```js
function (actualAge){
  if (actualAge == 1){
    return {
      humanYears: actualAge,
      catYears: 15,
      dogYears: 15,
    }
  }

  if (actualAge == 2){
    return {
      humanYears: actualAge,
      catYears: 24,
      dogYears: 24,
    }
  }

  return {
    humanYears: actualAge,
    catYears: (actualAge - 2) * 4 + 24,
    dogYears: (actualAge - 2) * 5 + 24,
  }
}
```

| Input | Output |
| ----- | ------ |
|       |        | 
|       |        | 
|       |        | 

<table>
  <tr>
    <th>What does this program do?</th>
    <td></td>
  </tr>
</table>

## Rubric

* Contains a plausible collection of test cases
* Outputs are accurately derived from inputs
* Summary is plausible


## Test Inputs and Outputs table

| Inputs | Outputs |
| :---: | :---: |
| 2  |{humanYears: 2, catYears: 24, dogYears: 24} |
| 5 |{humanYears: 5, catYears: 36, dogYears: 39} |
| 50 | {humanYears: 50, catYears: 216, dogYears: 264} |


## for input 2

if the actualAge is 2 then it will skip the first if statement and then will run the second if statement and will stop.

```js

const actualAge = 2;

function (actualAge){                   // 2
  if (actualAge == 1){                  // false
    return {                            // this section is skipped
      humanYears: actualAge,
      catYears: 15,
      dogYears: 15,
    }
  }

  if (actualAge == 2){                  // true
    return {
      humanYears: actualAge,            // humanYears: 2,
      catYears: 24,                     // catYears: 24,
      dogYears: 24,                     // dogYears: 24,
    }
  }

  return {                              // this section does not run.
    humanYears: actualAge,
    catYears: (actualAge - 2) * 4 + 24,
    dogYears: (actualAge - 2) * 5 + 24,
  }
}

```

## for input 5

if the actualAge is 5 then is will skip the first two if statements and will run the return statement.

```js

const actualAge = 5;

function (actualAge){                   // 5
  if (actualAge == 1){                  // false
    return {                            // this section is skipped
      humanYears: actualAge,
      catYears: 15,
      dogYears: 15,
    }
  }

  if (actualAge == 2){                  // false
    return {                            // this section is skipped
      humanYears: actualAge,
      catYears: 24,
      dogYears: 24,
    }
  }

  return {
    humanYears: actualAge,                      // humanYears: 5,
    catYears: (actualAge - 2) * 4 + 24,         // catYears: 36,
    dogYears: (actualAge - 2) * 5 + 24,         // dogYears: 39,
  }
}

```

## for input 50

if the actualAge is 50 then is will skip the first two if statements and will run the return statement.

```js

const actualAge: 50;

function (actualAge){                   // 50
  if (actualAge == 1){                  // false
    return {                            // this section is skipped
      humanYears: actualAge,
      catYears: 15,
      dogYears: 15,
    }
  }

  if (actualAge == 2){                  // false
    return {                            // this section is skipped
      humanYears: actualAge,
      catYears: 24,
      dogYears: 24,
    }
  }

  return {
    humanYears: actualAge,                      // humanYears: 50,
    catYears: (actualAge - 2) * 4 + 24,         // catYears: 216,
    dogYears: (actualAge - 2) * 5 + 24,         // dogYears: 264,
  }
}

```

## Summary

When the value of the variable did not execute in the statements as truthy then it moved to the next statement,
if no statements were truthy then it executed the return statement at the end.


