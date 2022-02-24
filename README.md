


# FreeCodeCamp

# Basic Algorithms 

## Repeat a String Repeat a String
### Repeat a given string str (first argument) for num times (second argument). Return an empty string if num is not a positive number. For the purpose of this challenge, do not use the built-in .repeat() method.

```jsx
function repeatStringNumTimes(str, num) {
  return num > 0 ? str + repeatStringNumTimes(str, num - 1) : '' ;
}

repeatStringNumTimes("abc", 3);
```

# Intermediate Algorithm 
## Seek and Destroy
### You will be provided with an initial array (the first argument in the destroyer function), followed by one or more arguments. Remove all elements from the initial array that are of the same value as these arguments.

```jsx 
function destroyer(arr,...arg) {
  return arr.filter(ele=> !arg.includes(ele))
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```

# Functional Programming 

```jsx 
function ascendingOrder(arr) {
  return arr.sort(function(a, b) {
    return a - b;
  });
}

ascendingOrder([1, 5, 2, 3, 4]);
This would return the value [1, 2, 3, 4, 5].

function reverseAlpha(arr) {
  return arr.sort(function(a, b) {
    return a === b ? 0 : a < b ? 1 : -1;
  });
}

reverseAlpha(['l', 'h', 'z', 'b', 's']);
```

## Explanation 
### This would return the value ['z', 's', 'l', 'h', 'b'].

JavaScript's default sorting method is by string Unicode point value, which may return unexpected results. Therefore, it is encouraged to provide a callback function to specify how to sort the array items. When such a callback function, normally called compareFunction, is supplied, the array elements are sorted according to the return value of the compareFunction: If compareFunction(a,b) returns a value less than 0 for two elements a and b, then a will come before b. If compareFunction(a,b) returns a value greater than 0 for two elements a and b, then b will come before a. If compareFunction(a,b) returns a value equal to 0 for two elements a and b, then a and b will remain unchanged.
