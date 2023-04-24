## Part 2

For the method `reverseInPlace` there are two crutial bugs in the code:

1. The method does not contain a temporary value to save the value of the list's element before it is replaced by `arr[i] = arr[arr.length - i - 1];`
2. The method's for loop contains the condition `i < arr.length` when it should have been `i , arr.length/2` because if it goes through the entire list then it would replave values that have alrteady been replaced before.

Some JUnit test which I used to debug this code are:

• A JUnit test that displays this bug is `@Test public void testReverseInPlace() { int[] input4 = {1, 2, 3, 4}; ArrayExamples.reverseInPlace(input4); assertArrayEquals(new int[]{4, 3, 2, 1}, input4); }` 

• A JUnit test that works despite the bug is `@Test public void testReverseInPlace() { int[] input1 = { 3 }; ArrayExamples.reverseInPlace(input1); assertArrayEquals(new int[]{ 3 }, input1);`




