# **sort-array-by-key**
### Sort a typed array of objects by a specified element key in  Typescript/JS (ES6)

## **Installation**

> `npm install sort-array-by-key --save`

or

> `yarn add sort-array-by-key`

---

## **Syntax**

> **`sortArrayByKey<T>(arr:T[]);`**

### **Parameters**

- `arr`:
  Required typed Array value of type `T[]`. Type defaults to `Record<any, any>`.
- `key`:
  Required value of type `keyof T`, upon which the items in the array are sorted by their corresponding values.
- `ascending`:
  Optional value of type `boolean`. Determines whether the elements of the `arr` value are sorted in ascending order. Defaults to true

### **Return value**

- `sortArrayByKey` will return a reference to the original `arr` array, of type `T[]`, sorted by `key` values.

---

## **Usage**

**Import the `sortArrayByKey` function**

```
import sortArrayByKey from "sort-array-by-key";
```

or

```
const sortArrayByKey = require("sort-array-by-key")
```

**Sample implementation**

```
type User = {
  name: string;
  age: number;
};

const userList: User[] = [
  { name: 'Sally', age: 43 },
  { name: 'Wally', age: 13 },
  { name: 'Hally', age: 73 },
  { name: 'Cally', age: 23 },
];

// returns
/**
 [
    { name: 'Wally', age: 13 },
    { name: 'Cally', age: 23 },
    { name: 'Sally', age: 43 },
    { name: 'Hally', age: 73 },
  ]
 */
const sortedUserList = sortArrayByKey<User>(userList, 'age');
```

