# Problem Solving with TypeScript

This assignment is designed to assess your understanding of fundamental TypeScript concepts. It includes a series of problems that cover topics such as types, functions, classes, interfaces, and array manipulation.

## Problem 1:

Create a function **formatValue** that accepts a value which may be a **string**, **number**, or **boolean**, and returns the following based on the value type:

- If the input is a **string** → return the string in **uppercase**
- If the input is a **number** → return the number multiplied by **10**
- If the input is a **boolean** → return the **opposite value** (`true → false`, `false → true`)

### Requirements:

- You must write the correct type for the function parameter and the return type.
- You must use type checking to handle each case.

### Sample Input:

```ts
console.log(formatValue('hello'));
console.log(formatValue(5));
console.log(formatValue(true));
```

### Sample Output:

```ts
HELLO;
50;
false;
```

## Problem 2:

Create a function **getLength** that accepts a value which may be a **string** or an **array**, and returns the **length** of the value.

- If the input is a **string** → return the number of characters.
- If the input is an **array** → return the number of elements.

### Requirements:

- You must write the correct type for the function parameter and the return type.
- You must use type checking to handle each case (`typeof` or `Array.isArray`).

### Sample Input:

```ts
console.log(getLength('typescript'));
console.log(getLength([10, 20, 30, 40]));
```

### Sample Output:

```ts
10;
4;
```

## Problem 3:

Create a `Person` class with `name` and `age` properties. Add a method `getDetails` that returns a string with the person's name and age.

### Requirements:

- You must use a constructor to initialize the properties.
- The `getDetails` method should return a string in the format: `"Name: [name], Age: [age]"`.

### Sample Input:

```ts
const person1 = new Person('John Doe', 30);
console.log(person1.getDetails());

const person2 = new Person('Alice', 25);
console.log(person2.getDetails());
```

### Sample Output:

```ts
'Name: John Doe, Age: 30';
'Name: Alice, Age: 25';
```

## Problem 4:

Create a function **filterByRating** that accepts an array of items, where each item has the following properties:

- `title` (string)
- `rating` (number between 0 and 5)

The function should return a new array containing only the items with a rating of 4 or more.

### Requirements:

- You must write the correct type for the function parameter and the return type.
- Do not mutate the original array.

### Sample Input:

```ts
const books = [
  { title: 'Book A', rating: 4.5 },
  { title: 'Book B', rating: 3.2 },
  { title: 'Book C', rating: 5.0 },
];

console.log(filterByRating(books));
```

### Sample Output:

```ts
[
  { title: 'Book A', rating: 4.5 },
  { title: 'Book C', rating: 5.0 },
];
```

## Problem 5:

Create a function **filterActiveUsers** that accepts an array of user objects. Each user object contains `id`, `name`, `email`, and `isActive` properties. The function should return a **new array** containing only the users whose `isActive` property is `true`.

### Requirements:

- You must write the correct type for the function parameter and the return type.
- Do not mutate the original array.
- Use type checking if necessary.

### Sample Input:

```ts
const users = [
  { id: 1, name: 'Rakib', email: 'rakib@example.com', isActive: true },
  { id: 2, name: 'Asha', email: 'asha@example.com', isActive: false },
  { id: 3, name: 'Rumi', email: 'rumi@example.com', isActive: true },
];

console.log(filterActiveUsers(users));
```

### Sample Output:

```ts
[
  { id: 1, name: 'Rakib', email: 'rakib@example.com', isActive: true },
  { id: 3, name: 'Rumi', email: 'rumi@example.com', isActive: true },
];
```

## Problem 6:

Define an interface `Book` with the following properties:

- `title` (string)
- `author` (string)
- `publishedYear` (number)
- `isAvailable` (boolean)

Then, create a function `printBookDetails` that accepts an object of type `Book` and prints its details to the console in the format: "Title: [title], Author: [author], Published: [publishedYear], Available: [Yes/No]".

### Requirements:

- You must define the `Book` interface correctly.
- The `printBookDetails` function must accept an object that follows to the `Book` interface.

### Sample Input:

```ts
const myBook: Book = {
  title: 'The Great Gatsby',
  author: 'F. Scott Fitzgerald',
  publishedYear: 1925,
  isAvailable: true,
};

printBookDetails(myBook);
```

### Sample Output:

```
Title: The Great Gatsby, Author: F. Scott Fitzgerald, Published: 1925, Available: Yes
```

## Problem 7:

Create a function **getUniqueValues** that accepts two arrays and returns a new array containing only the unique values from both arrays, without any duplicates.

### Requirements:

- You must write the correct type for the function parameter and the return type.
- The function should handle arrays of strings or numbers.
- You are not allowed to use any built-in methods to solve this problem.

### Sample Input:

```ts
const array1 = [1, 2, 3, 4, 5];
const array2 = [3, 4, 5, 6, 7];
console.log(getUniqueValues(array1, array2));
```

### Sample Output:

```ts
[1, 2, 3, 4, 5, 6, 7];
```

## Problem 8:

Create a function **calculateTotalPrice** that accepts an array of product objects. Each product object contains the following properties:

- `name` (string)
- `price` (number)
- `quantity` (number)
- **discount?**: optional number from **0–100**, representing a percentage discount

The function should return the **total price** of all products in the array, taking into account the discount for each product (if provided).
If the array is empty, return `0`.

### Requirements:

- You must write the correct type for the function parameter and the return type.
- Use array methods (`map`, `reduce`, etc.) to calculate the total.
- The total price of each product is calculated as: `(price * quantity)`.
- Correctly handle products with and without the `discount` property.

### Sample Input:

```ts
const products = [
  { name: 'Pen', price: 10, quantity: 2 },
  { name: 'Notebook', price: 25, quantity: 3, discount: 10 },
  { name: 'Bag', price: 50, quantity: 1, discount: 20 },
];

console.log(calculateTotalPrice(products));
```

### Sample Output:

```ts
127.5;
```

## 🎯 Interview Questions - Blog Task

### Blog Post (in Bangla): Answer any 2 of the questions below:

1. What are some differences between interfaces and types in TypeScript?
2. What is the use of the `keyof` keyword in TypeScript? Provide an example.
3. Explain the difference between `any`, `unknown`, and `never` types in TypeScript.
4. What is the use of `enums` in TypeScript? Provide an example of a numeric and string enum.
5. Provide an example of using **union** and **intersection** types in TypeScript.

## ✅ Instructions & Submission Guidelines:

- **Blog:** Write a blog post on **any 2** of the provided topics and include it in this `README.md`.
- **Coding:**
  - Place all your solutions in a single TypeScript file (e.g., [solution.ts](./solution.ts)).
  - Use the exact function names provided in the problems.
  - Your function's output must **exactly** match the sample output provided. This includes punctuation, spacing, and capitalization. Any deviation will result in marks being deducted. For instance, if the sample output is `'Name: John Doe, Age: 30'`, your function must return that exact string. A return value like `'name: John Doe, age: 30'` or `'Name: John Doe,Age: 30'` will be considered incorrect.
  - Use meaningful names for all variables, functions, and classes.
  - Do not include comments like “Problem 1” in your code.
  - Do not include any `console.log` in your final code.
- **Originality:** All work must be original. Plagiarism will result in a **zero**.
- **Submission:** Submit a single public GitHub repository which will includes your [solution.ts](./solution.ts) file and the updated `README.md`.

## 🕒 Assignment Deadlines:

- **60 Marks:** November 18, 2025 – _before 11:59 PM_
- **50 Marks:** November 19, 2025 – _before 11:59 PM_
- **30 Marks:** After November 19, 2025

---
