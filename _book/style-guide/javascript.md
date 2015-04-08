Numbers

Strings

Use single-quoted strings.

```
// Bad
"hello"
"<a href='/'>Home</a>"

// Good
'hello'
'<a href="/">Home</a>'
```

> Single quotes ensures HTML attributes will be written correctly.

Operators

Use spaces around operators

```
// Bad
(2+3)*(9-8)
[1,2,-3]
('')? 'hello':'goodbye'

// Good
(2 + 3) * (9 - 8)
[1, 2, -3]
('') ? 'hello' : 'goodbye'

```

> Provide better readibility

Return Values

Use leading comment

```
// Bad
8 * 2
=> 16

// Good
8 * 2
// 16
```

> The hash rocket syntax is an overloaded term and will take on additional
> meaning with es6's fat arrow syntax.

Variables

Use camelCase for variable names.

```
// Bad
cell_one;
my_friends = ['ellen','mary','doug','pat'];

// Good
cellOne;
myFriends = ['ellen', 'mary', 'doug', 'pat'];
```

> Follow JavaScript conventions

Functions

Use anonymous function expressions.

```
// Bad
function greet(name) {
  return 'Hello ' + name;
}

// Good
var greet = function(name) {
  return 'Hello ' + name;
}
```

> Stress that functions are data just like any other type and may be passed
> around as callbacks.
