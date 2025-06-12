## 1. Difference between `<link>` and `<script>` tags?

* **`<link>`** is used to link external resources like CSS files to the HTML.
* **`<script>`** is used to embed or reference JavaScript code in the HTML.

| Tag        | Purpose                | Placement                                            |
| ---------- | ---------------------- | ---------------------------------------------------- |
| `<link>`   | Link stylesheets (CSS) | Inside `<head>`                                      |
| `<script>` | Link or embed JS       | Usually before `</body>` or in `<head>` with `defer` |

---

## 2. What is the difference between `find` and `filter` in JavaScript?

* `find()` returns the **first matching element** from an array.
* `filter()` returns **all matching elements** as an array.

```js
const arr = [1, 2, 3, 4];
arr.find(x => x > 2);   // 3
arr.filter(x => x > 2); // [3, 4]
```

---

## 3. What is a PRIMARY KEY and why is it important?

* A **PRIMARY KEY** is a column (or a combination) in a database table that uniquely identifies each row.
* Important because:

  * Ensures data uniqueness
  * Improves indexing and access speed
  * Prevents duplicate entries

---

## 4. Can you explain event bubbling and event capturing?

* **Event Bubbling**: Event starts from the **target element** and bubbles **up** to ancestors.
* **Event Capturing**: Event starts from the **document root** and travels **down** to the target.

```js
// Bubbling (default)
element.addEventListener('click', handler, false);

// Capturing
element.addEventListener('click', handler, true);
```

---

## 5. What is the difference between `var`, `let`, and `const`?

| Keyword | Scope    | Reassignable | Redeclarable | Hoisted         |
| ------- | -------- | ------------ | ------------ | --------------- |
| `var`   | Function | Yes          | Yes          | Yes (undefined) |
| `let`   | Block    | Yes          | No           | No              |
| `const` | Block    | No           | No           | No              |

---

## 6. What are the DDL commands in SQL?

DDL stands for **Data Definition Language**. Common DDL commands:

* `CREATE`: Create new tables or databases
* `ALTER`: Modify existing structure
* `DROP`: Delete table/database
* `TRUNCATE`: Delete all records but keep table

---

## 7. What is the difference between `map` and `forEach` in JavaScript?

* `map()` creates a **new array** with results.
* `forEach()` performs operations for each item but **does not return** a new array.

```js
arr.map(x => x * 2);     // returns new array
arr.forEach(x => x * 2); // no return
```

---

## 8. What is the purpose of using `filter` and `reduce` in JavaScript?

* `filter()`: Extracts items that satisfy a condition
* `reduce()`: Aggregates array into a single value

```js
arr.filter(x => x > 2);        // [3, 4]
arr.reduce((a, b) => a + b);   // sum of all values
```

---

## 9. What is `z-index` in CSS?

* `z-index` controls the **stacking order** of elements.
* Higher `z-index` elements appear **on top** of lower ones.

```css
.modal {
  position: absolute;
  z-index: 1000;
}
```
