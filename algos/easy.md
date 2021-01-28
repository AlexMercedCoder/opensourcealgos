# Easy Challenges

_Any challenge can be made harder by trying to replace all loops with recursion_

## Reverse a String

Create a function that meets the following specification

- Goal: Reverses a string
- Parameters: 1 - String
- Return value: The reversed string

JS TIPS: Look into the split and join string functions

```js
const reverseString = (str) => {};

// Tests
reverseString("Cheese");
reverseString("Hello");
reverseString("Bread");
```

**Solution**

<details>
<summary>
Reveal
</summary>
<p>

```js

const reverseString = (str) => {

    //split the string into an array of individual letters
    const stringArray = str.split("")
    //reverse the array
    const stringArray.reverse()
    //join the array back into a string
    const newString = stringArray.join("")
    //return the new string
    return newString

}

// Tests
reverseString("Cheese") // "eseehC"
reverseString("Hello") // "olleH"
reverseString("Bread") // "dearD"

```

</details>

## Compare Strings

Create a function that returns whether two strings are the same regardless of capitalization, "cheese" is equal to "cHeEsE"/

- Goal: Compare whether strings are the same
- Parameters: 1 - String, 2 - String
- Return value: True or False

JS TIPS: easier to compare if they look alike...

```js
const compareStrings = (str1, str2) => {};

// Tests
compareStrings("Cheese", "cHeSe"); // True
compareStrings("Hello", "hEllOs"); // False
compareStrings("Bread", "brEAd"); // True
```

**Solution**

<details>
<summary>
Reveal
</summary>
<p>

```js
const compareStrings = (str1, str2) => {
  // lowercase string 1 and string 2 so the casing the is the same
  const newStr1 = str1.lowercase();
  const newStr2 = str2.lowercase();
  // Check if they are the same
  const areTheyTheSame = newStr1 === newStr2;
  // return the result
  return areTheytheSame;
};

// Tests
compareStrings("Cheese", "cHeSe"); // True
compareStrings("Hello", "hEllOs"); // False
compareStrings("Bread", "brEAd"); // True
```

</details>

## Array Incrementor

Create a function that takes an array of integers, and returns a new array where each integer has been increased by a given number

- Goal: Increment an array by a given amount
- Parameters: 1 - Array of Integers, 2 - Integer
- Return value: Array of Integers

JS TIPS: loops or map, think about that!

```js

const arrayIncrementer = (arr, num) => {


}

// Tests
arrayIncrementer([1,2,3] 1) // [2,3,4]
arrayIncrementer([2,3,4], 2) // [4,5,6]
arrayIncrementer([3,4,5], 3) // [6,7,8]

```

**Solution**

<details>
<summary>
Reveal
</summary>
<p>

```js

const arrayIncrementer = (arr, num) => {

    //Create a new array
    const newArray = []
    //Loop over the given array
    for(let index = 0; index < arr.length; x++){
        // add item to new array equal to item plus the number
        newArray.push(arr[index] + num)
    }
    //return the new array
    return newArray

}

// Tests
arrayIncrementer([1,2,3] 1) // [2,3,4]
arrayIncrementer([2,3,4], 2) // [4,5,6]
arrayIncrementer([3,4,5], 3) // [6,7,8]


```

</details>

## Array Remove

Create a function that takes an array of integers and number, it will find every instance of the that number in the array and remove it, and return the new array WITHOUT modifying the original array.

- Goal: Return all instances of a particular number from an array
- Parameters: 1 - Array of Integers, 2 - Integer
- Return value: Array of Integers

JS TIPS: splice is your friend

```js

const arrayRemove = (arr, num) => {


}

// Tests
arrayRemove([1,2,3] 1) // [2,3]
arrayRemove([2,2,4], 2) // [4]
arrayRemove([3,3,3], 3) // []

```

**Solution**

<details>
<summary>
Reveal
</summary>
<p>

```js

const arrayRemove = (arr, num) => {
    // array to track indexes of matches and copy of original array
    const arrayCopy = [...arr]
    const indexArray = []

    // check what numbers match
    for(let index = 0; index < arr.length; index++){
        if (arr[index] === num){
            indexArray.push(index)
        }
    }

    // remove the number from the array copy
    for (let index = 0; index < indexArray.length; index++){
        arrayCopy.splice(indexArray[index], 1)
    }

    //return the copy with the number removed
    return arrayCopy
}

// Tests
arrayRemove([1,2,3] 1) // [2,3]
arrayRemove([2,2,4], 2) // [4]
arrayRemove([3,3,3], 3) // []

```

</details>
