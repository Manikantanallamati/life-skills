# Cheatsheet

## Array cheatSheet:

| Method          | Description                              | Example           |
| --------------- | ----------------------------------       | ----------------- |
| `append(x)`     | Adds `x` at the end                      | `a.append(10)`    |
| `extend(list2)` | Adds all items from list2                | `a.extend([4,5])` |
| `insert(i, x)`  | Inserts `x` at index `i`                 | `a.insert(1, 99)` |
| `remove(x)`     | Removes first occurrence of `x`          | `a.remove(10)`    |
| `pop(i)`        | Removes and returns element at index `i` | `a.pop(2)`        |
| `index(x)`      | Returns index of first `x`               | `a.index(5)`      |
| `count(x)`      | Counts how many times `x` appears        | `a.count(3)`      |
| `sort()`        | Sorts list in ascending order            | `a.sort()`        |
| `reverse()`     | Reverses the list                        | `a.reverse()`     |
| `copy()`        | Returns a shallow copy                   | `b = a.copy()`    |
| `clear()`       | Removes all items from list              | `a.clear()`       |

## String Methods:

| Method              | Description                         | Example                          |
| ------------------- | ----------------------------------- | -------------------------------- |
| `lower()`           | Converts to lowercase               | `"ABC".lower()` → `'abc'`        |
| `upper()`           | Converts to uppercase               | `"abc".upper()` → `'ABC'`        |
| `title()`           | Title-case string                   | `"hello world".title()`          |
| `strip()`           | Removes leading/trailing spaces     | `" hi ".strip()` → `'hi'`        |
| `replace(old, new)` | Replaces old with new               | `"hi".replace('i','ey')`         |
| `split(delimiter)`  | Splits by delimiter                 | `"a,b".split(',')` → `['a','b']` |
| `join(list)`        | Joins list with string as separator | `'-'.join(['a','b'])`            |
| `find(x)`           | Returns first index of `x`          | `"apple".find('p')` → `1`        |
| `count(x)`          | Count occurrences of `x`            | `"apple".count('p')` → `2`       |
| `startswith(x)`     | Checks if starts with `x`           | `"hello".startswith('h')`        |
| `endswith(x)`       | Checks if ends with `x`             | `"hello".endswith('o')`          |
| `isalpha()`         | All letters?                        | `"abc".isalpha()` → `True`       |
| `isdigit()`         | All digits?                         | `"123".isdigit()` → `True`       |


## OOPS Concept:

| Concept               | Description                          | Syntax / Example                       |
| --------------------- | ------------------------------------ | -------------------------------------- |
| **Class**             | Blueprint for objects                | `class Car:`                           |
| **Object**            | Instance of a class                  | `c = Car()`                            |
| **Constructor**       | `__init__()` initializes object      | `def __init__(self, name):`            |
| **Self**              | Refers to current object             | `self.name = name`                     |
| **Inheritance**       | One class inherits another           | `class A: ... class B(A):`             |
| **Encapsulation**     | Data hiding using `_` or `__` prefix | `_var`, `__var`                        |
| **Polymorphism**      | Same method, different behavior      | `def area()` in different classes      |
| **Method Overriding** | Child class overrides parent method  | Define same method name in child class |
| **Static Method**     | Doesn’t need self or class           | `@staticmethod` above the method       |
| **Class Method**      | Works with class not instance        | `@classmethod` + `cls` as parameter    |
