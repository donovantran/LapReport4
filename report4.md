# Lab Report 4
---
For lab report 4, I recreated the steps within Lab 7 using the ArrayExamples from the previous lab. The error in the code is displayed here:

```


public class ArrayExamples {

  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/3; i++) {
      int holder;
      holder = arr[i];
      arr[i] = arr[arr.length - i -1];
      arr[arr.length - i - 1] = holder;
    }
  }

  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }

  // Averages the numbers in the array (takes the mean), but leaves out the
  // lowest number when calculating. Returns 0 if there are no elements or just
  // 1 element in the array
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }


}

```
The error in the code lies within line 8, where the lenght of the `arr` should be divided by 2 instead of 3 in order the reverse the contents of the int array.
The following screen shots are the steps taken to recreate the steps we did during lab, but on ArrayExamples.
