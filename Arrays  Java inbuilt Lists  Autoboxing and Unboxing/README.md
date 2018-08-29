# Array

> Array starts with 0

## How to use

```java

int [] myIntArray;
myIntArray = new int[10];

```

```java

double[] myDoubleArray = new double[10];
myDoubleArray[0] = 4.5d;
myDoubleArray[1] = 5.5d;
myDoubleArray[2] = 6.5d;

System.out.println(myDoubleArray[0]);
	// 4.5

```

```java

int[] myIntArray = new int[10];
myIntArray[0] = 45;
myIntArray[1] = 478;
myIntArray[5] = 50;

System.out.println(myIntArray[5]);
// 50

```

```java

int[] mySecondArray = {1,2,3,4,5,6,7,8,9,10};
System.out.println(mySecondArray[0]);
System.out.println(mySecondArray[1]);
System.out.println(mySecondArray[2]);
// 1  2	3

```

> Populate array using for loop

```java

int[] myIntArrayForLoop = new int[10];

// Pushing
for(int i=0 ; i < 10; i++) {
	myIntArrayForLoop[i] = i*10;
}

//Printing
for(int i=0 ; i < 10; i++) {
	System.out.println("Element " + i + ", value is " + myIntArrayForLoop[i]);
}

```

```java

public static void main(String[] args) {
	myIntArrayForLoop = new int[20];
	//	Using Array Method .length

	// Pushing
	for(int i=0 ; i < myIntArrayForLoop.length; i++) {
		myIntArrayForLoop[i] = i*10;
	}

	//printing using method by passing entire array as an Argument
	printArray(myIntArrayForLoop);

}

//Using Method
public static void printArray(int[] array) {
	//Printing
	for(int i=0 ; i < array.length; i++) {
		System.out.println("Element " + i + ", value is " + array[i]);
	}
}

```

> Real Life Example of Use of Array's

```java

// first step
private static Scanner scanner = new Scanner(System.in);

public static void main(String[] args) {
	// Taking input from User
	int[] myIntegers = getintegers(5);

	for(int i=0;i<myIntegers.length;i++) {
		System.out.println("Element " + i + ", typed value was " + myIntegers[i]);
	}
	System.out.println("The average is " + getAverage(myIntegers));

}

//Taking Input from user Function
public static int[] getintegers(int number) {
	System.out.println("Enter " + number + " integer value. \r");

	int[] values = new int[number];

	for(int i=0; i< values.length;i++) {
		values[i] = scanner.nextInt();
	}

	return values;
}

//get Average
public static double getAverage(int[] array) {
	int sum = 0;
	for(int i=0; i< array.length; i++) {
		sum += array[i];
	}		
	return (double) sum/ (double) array.length;
}

```

# Sorting Array

> this approch will modify the original Array Element **BE CAREFULL**

```java
private static Scanner scanner = new Scanner(System.in);

public static void main(String[] args) {
	// Array Challenge
	int[] gettingInt = getIntegers(4);
	int[] sortedArray = sortArray(gettingInt);
	printArray(sortedArray);
}

public static int[] getIntegers(int arrayLength) {
	int[] newInt = new int[arrayLength];

	for (int i = 0; i < arrayLength; i++) {
		newInt[i] = scanner.nextInt();
	}

	return newInt;
}

public static int[] sortArray(int[] array) {
	for (int i = 0; i < array.length - 1; i++) {
		for (int j = 0; j < array.length - 1; j++) {
			if (array[j] < array[j + 1]) {
				int temp = array[j + 1];
				array[j + 1] = array[j];
				array[j] = temp;
			}
		}
	}
	return array;
}

public static void printArray(int[] array) {
	for (int i = 0; i < array.length; i++) {
		System.out.println("array is " + array[i]);
	}
}

```
## Copy an Array to another Array

###### there is a class in java called [Array](https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html) which comes with built-in function for copying array!



> this method will not modify the original array which is being pass as params

```java

//Copying array

public static int[] sortArray(int[] array) {
	int[] sortedArray = new int[array.length];
	
	for(int i=0;i<array.length;i++){
		sortedArray[i] = array[i];
	}
	boolean flag = true;
	while(flag){
	flag = false;
		for (int i = 0; i < sortedArray.length - 1; i++) {
			if (sortedArray[i] < sortedArray[i + 1]) {
				int temp = sortedArray[i];
				sortedArray[i] = sortedArray[i + 1];
				sortedArray[i + 1] = temp;
				flag = true;
			}
		}
	}
	
	return sortedArray;
}

```
# Resize an array

```java
private static Scanner s = new Scanner(System.in);
private static int[] baseData = new int[10];

public static void main(String[] args) {
	// Resizing an Array Dynamically 

	System.out.println("Enter 10 integers: ");
	getInput();
	printArray(baseData);
	resizeArray();
	System.out.println("Enter 12 integers: ");
	getInput();
	printArray(baseData);

}

private static void getInput() {
	for(int i=0; i< baseData.length; i++) {
		baseData[i] = s.nextInt();
	}
}

private static void printArray(int[] arr) {
	for(int i=0; i< baseData.length; i++) {
		System.out.print(arr[i] + " ");
	}
	System.out.println();
}

private static void resizeArray() {
	int[] original = baseData;
	baseData = new int[12];
	for(int i = 0; i < original.length ; i ++) {
		baseData[i] = original[i];
	}
}


```

# Sum of Array Element

```java
import java.utils.Scanner;

private static Scanner s = new Scanner(System.in);
public static void main(String[] args){
	int n=4,sum=0;
	int[] myArray = new int[n];


	for(int i=0;i<n;i++) {
		myArray[i] = s.nextInt();
	}

	for(int i=0;i<myArray.length;i++) {
		if(myArray[i]%2==0 || myArray[i]%3==0) {
			sum+=myArray[i];
		}
	}

	System.out.println(sum);

}

/*
>> Output

4 <-- Size
2 4 5 6 <-- Element
8 <-- sum of 2,6

*/

```

# Special Sum of Array

```java
int n=3,sum=0;
int[] myArray = new int[n];

for(int i=0;i<n;i++) {
	myArray[i] = s.nextInt();
}

for(int i=0;i<myArray.length;i++) {
	sum+=myArray[i];
}

while(sum>9) {
	String val = Integer.toString(sum);
	sum = 0;
	for(int i=0;i<val.length();i++) {
		sum += (int) val.charAt(i) - 48;				
	}
}

System.out.println(sum);


/*

	3 <- size of array

	9 9 9 <- Element

	9 <- answer

	>>Explanation

	9 + 9 + 9

	2 + 7 = 9

	Hence,ans is 9

*/


```

# Consecutive element using Array

>> Array Elements Value has difftence of 1 Like for Example :- 3,7,2,5,4,6 will be 2,3,4,5,6,7 so this is Consecutive element Array

```java
int[] arr = {1,3,4,4,2};

// 1 9 2 4 0 3
// 10 1 2 3 8 6 7 2 4 9 12 3 5 7 19 20 14 15 17 18
// 3,7,2,5,4,6

Arrays.sort(arr);

for(int i=0;i<arr.length;i++) {
	System.out.print(arr[i] + " ");
}

System.out.println();
boolean isShorted = true;

boolean initial = true;
for(int i=0;i<arr.length-1;i++) {
	int value = arr[i+1] - arr[i];
	if(value==1 || value == 0 && initial) {
		isShorted = true;
		initial = true;
	}else {
		isShorted = false;
		initial = false;
	}			
}

System.out.println(isShorted);


```









