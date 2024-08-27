### JavaScript Arrays and Array Methods

#### Introduction to Arrays
An array in JavaScript is a data structure that allows you to store multiple elements in a single variable. These elements can be of any type, such as numbers, strings, objects, or even other arrays.

**Example:**
```javascript
let numbers = [1, 2, 3, 4, 5, 6];
```

#### Array Methods

1. **push()**
   - Adds one or more elements to the end of an array and returns the new length of the array.
   - **Example:**
   ```javascript
   let numbers = [1, 2, 3];
   numbers.push(4); // numbers becomes [1, 2, 3, 4]
   ```

2. **pop()**
   - Removes the last element from an array and returns that element.
   - **Example:**
   ```javascript
   let numbers = [1, 2, 3];
   numbers.pop(); // numbers becomes [1, 2]
   ```

3. **toString()**
   - Converts an array to a string of comma-separated values.
   - **Example:**
   ```javascript
   let numbers = [1, 2, 3];
   let str = numbers.toString(); // "1,2,3"
   ```

4. **concat()**
   - Merges two or more arrays and returns a new array without changing the existing arrays.
   - **Example:**
   ```javascript
   let numbers = [1, 2, 3];
   let numbers2 = [4, 5];
   let newArray = numbers.concat(numbers2); // newArray becomes [1, 2, 3, 4, 5]
   ```

5. **shift()**
   - Removes the first element from an array and returns that element. This method changes the length of the array.
   - **Example:**
   ```javascript
   let numbers = [1, 2, 3];
   numbers.shift(); // numbers becomes [2, 3]
   ```

6. **unshift()**
   - Adds one or more elements to the beginning of an array and returns the new length of the array.
   - **Example:**
   ```javascript
   let numbers = [2, 3];
   numbers.unshift(1); // numbers becomes [1, 2, 3]
   ```

7. **slice()**
   - Returns a shallow copy of a portion of an array into a new array, selected from start to end (end not included). The original array is not modified.
   - **Example:**
   ```javascript
   let numbers = [1, 2, 3, 4, 5];
   let slicedArray = numbers.slice(1, 3); // slicedArray becomes [2, 3]
   ```

8. **splice()**
   - Adds/removes items to/from an array, and returns the removed item(s). This method changes the original array.
   - **Example:**
   ```javascript
   let names = ["aman", "puja", "siddarth"];
   names.splice(1, 0, "index", "javascript", "body"); // names becomes ["aman", "index", "javascript", "body", "puja", "siddarth"]
   ```

#### Complete Code Snippet from the class
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa nemo
      voluptatem expedita, magni repudiandae debitis! Velit nisi ex ut
      laudantium.
    </p>

    <script>
      let numbers = [1, 2, 3, 4, 5, 6];
      let numbers2 = [10, 11, 12];

      let userData = [
        {
          name: "Sudhanshu",
          age: 24,
          mobileNumber: [13424, 223, 3241],
        },
        {
          name: "Shristi",
          age: 23,
        },
        {
          name: "Ashish",
          age: 80,
        },
      ];

      //   console.log(userData[0]);

      //   for (let i = 0; i < userData.length; i++) {
      //     console.log(userData[i].name);
      //   }

      //   console.log(userData[0].age);

      //   console.log(numbers[0]);

      //   console.log("before pushing the value");
      //   for (let i = 0; i < numbers.length; i++) {
      //     console.log(numbers[i]);
      //   }

      // push adds an element to the end index
      //   numbers.push(7);
      //   numbers.push(8);

      //   console.log("after pushing the value");
      //   for (let i = 0; i < numbers.length; i++) {
      //     console.log(numbers[i]);
      //   }

      //   console.log(numbers.length);

      //   console.log("after poping the value");
      //   numbers.pop();
      //   numbers.pop();
      //   for (let i = 0; i < numbers.length; i++) {
      //     console.log(numbers[i]);
      //   }

      //   console.log("after converting to String");
      //   let newArrayToString = numbers.toString();
      //   console.log(newArrayToString);

      //concat
      //   let newArray = numbers.concat(numbers2);

      //   for (let i = 0; i < newArray.length; i++) {
      //     console.log(newArray[i]);
      //   }

      //   removes one Element from the front
      //   numbers2.shift();
      //   console.log(numbers2.length);

      //   numbers2.unshift(1);
      //   console.log(numbers2[0]);

      //   let slicedArray = numbers.slice(2, 4);
      //   for (let i = 0; i < slicedArray.length; i++) {
      //     console.log(slicedArray[i]);
      //   }

      //   let names = ["aman", "puja", "siddarth"];
      //   names.splice(1, 0, "index", "javascript", "body");
      //   for (let i = 0; i < names.length; i++) {
      //     console.log(names[i]);
      // }
    </script>
  </body>
</html>
```
