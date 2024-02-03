# JavaScript-Q7
Write a JavaScript program that uses a try-catch block to catch and handle a 'RangeError' when accessing an array with an invalid index.

function access_Array_Element(array, index) {
  try {
    const element = array[index];
    console.log('Accessed element:', element);
  } catch (error) {
    if (error instanceof RangeError) {
      console.log('Error: Invalid index. Please provide a valid index within the array bounds.');
    } else {
      throw error; // re-throw the error if it's not a RangeError
    }
  }
}

// Example
const nums = [1, 2, 3, 4, 5];
access_Array_Element(nums, 1); // Valid index
access_Array_Element(nums, 5); // Invalid index

**Sample Output:**

"Accessed element:"
2
"Accessed element:"
undefined
