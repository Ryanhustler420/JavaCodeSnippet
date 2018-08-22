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
