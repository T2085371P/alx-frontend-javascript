0x00-ES6_basic
08806026ef621f900121

This repository contains exercises and examples for learning the basics of ES6 (ECMAScript 2015) in JavaScript.

Resources
ECMAScript 6 - ECMAScript 2015
Statements and declarations
Arrow functions
Default parameters
Rest parameter
Javascript ES6 — Iterables and Iterators
Learning Objectives
What ES6 is

New features introduced in ES6

The difference between a constant and a variable

Block-scoped variables

Arrow functions and function parameters default to them

Rest and spread function parameters

String templating in ES6

Object creation and their properties in ES6

Iterators and for-of loops

Tasks
Const or let? Modify
function taskFirst to instantiate variables using const
function taskNext to instantiate variables using let
export function taskFirst() {
  var task = 'I prefer const when I can.';
  return task;
}

export function getLast() {
  return ' is okay';
}

export function taskNext() {
  var combination = 'But sometimes let';
  combination += getLast();

  return combination;
}
Block Scope
Given what you’ve read about var and hoisting, modify the variables inside the function taskBlock so that the variables aren’t overwritten inside the conditional block.
export default function taskBlock(trueOrFalse) {
  var task = false;
  var task2 = true;

  if (trueOrFalse) {
    var task = true;
    var task2 = false;
  }

  return [task, task2];
}
Arrow functions
Rewrite the following standard function to use ES6’s arrow syntax of the function add (it will be an anonymous function after)
export default function getNeighborhoodsList() {
  this.sanFranciscoNeighborhoods = ['SOMA', 'Union Square'];

  const self = this;
  this.addNeighborhood = function add(newNeighborhood) {
    self.sanFranciscoNeighborhoods.push(newNeighborhood);
    return self.sanFranciscoNeighborhoods;
  };
}
Parameter defaults
Condense the internals of the following function to 1 line - without changing the name of each function/variable.
export default function getSumOfHoods(initialNumber, expansion1989, expansion2019) {
  if (expansion1989 === undefined) {
    expansion1989 = 89;
  }

  if (expansion2019 === undefined) {
    expansion2019 = 19;
  }
  return initialNumber + expansion1989 + expansion2019;
}
Rest parameter syntax for functions
Modify the following function to return the number of arguments passed to it using the rest parameter syntax
export default function returnHowManyArguments() {

}
> returnHowManyArguments("Hello", "Holberton", 2020);
3
>
The wonders of spread syntax
Using spread syntax, concatenate 2 arrays and each character of a string by modifying the function below. Your function body should be one line long.
export default function concatArrays(array1, array2, string) {
}
Take advantage of template literals
Rewrite the return statement to use a template literal so you can the substitute the variables you’ve defined.
export default function getSanFranciscoDescription() {
  const year = 2017;
  const budget = {
    income: '$119,868',
    gdp: '$154.2 billion',
    capita: '$178,479',
  };

  return 'As of ' + year + ', it was the seventh-highest income county in the United States'
        / ', with a per capita personal income of ' + budget.income + '. As of 2015, San Francisco'
        / ' proper had a GDP of ' + budget.gdp + ', and a GDP per capita of ' + budget.capita + '.';
}
Object property value shorthand syntax
Notice how the keys and the variable names are the same? Modify the following function’s budget object to simply use the keyname instead.
export default function getBudgetObject(income, gdp, capita) {
  const budget = {
    income: income,
    gdp: gdp,
    capita: capita,
  };

  return budget;
}
