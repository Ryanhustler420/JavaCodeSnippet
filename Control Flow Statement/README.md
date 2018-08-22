# Switch Statement

> Make sure you have jdk above 8 or 8
> fileMenu -> projectStructure / Project / project language leve


> Using if statement

```java

int value = 1;

if (value == 1) {
  System.out.println("value was 1");
} else if (value == 2) {
  System.out.println("value was 2");
} else {
  System.out.println("was not 1 or 2");
}

```
> Using switch statement

```java

int switchValue = 2;

switch (switchValue) {
  case 1:
    System.out.println("value was 1");
    break;

  case 2:
    System.out.println("value was 2");
    break;

  case 3:
  case 4:
  case 5:
    System.out.println("was a 3, or a 4, or a 5");
    System.out.println("Actually it was a " + switchValue);
    break;

  default:
    System.out.println("was not 1 or 2");
    break; // we can remove this break statement because this is last! Recommended: always include break
}

```

> In java version 7 we can use 'String' data type as well in switch statement

```java

String month = "January";
		
switch(month.toLowerCase()) {
  case "january":
    System.out.println("Jan");
    break;
  case "june":
    System.out.println("Jun");
    break;
  default:
    System.out.println("Not sure");
}

```

# do While loop

```java

count = 6;
do {
    System.out.println("Count value was " + count);
   count++;

   if(count >100) {
       break;
   }

} while(count != 6);

```
## while loop

```java

int number = 5;
int finishNumber = 20;
int evenNumbersFound = 0;

while(number <= finishNumber) {
    if(!isEvenNumber(number)) {
	number++;
	continue;
    }

    System.out.println("Even number " + number);
    number++;

    evenNumbersFound++;
    if(evenNumbersFound >=5) {
	break;
    }
}

System.out.println("Total even numbers found = " + evenNumbersFound);

public static boolean isEvenNumber(int number) {
	if((number % 2)  == 0) {
	    return true;
	} else {
	    return false;
	}
}

```
# for loop

```java

	
System.out.println("10,000 at 2% interest = " + calculateInterest(10000.0, 2.0));
System.out.println("10,000 at 3% interest = " + calculateInterest(10000.0, 3.0));
System.out.println("10,000 at 4% interest = " + calculateInterest(10000.0, 4.0));
System.out.println("10,000 at 5% interest = " + calculateInterest(10000.0, 5.0));

for(int i=2; i<9; i++) {
    System.out.println("10,000 at " + i + "% interest = " + String.format("%.2f",calculateInterest(10000.0, i)));
}

for(int i=8; i>=2; i--) {
    System.out.println("10,000 at " + i + "% interest = " + String.format("%.2f",calculateInterest(10000.0, i)));
}

int count = 0;
for(int i=10; i<50; i++) {
    if(isPrime(i)) {
	count++;
	System.out.println("Number " + i + " is a prime number");
	if(count == 10) {
	    System.out.println("Exiting for loop");
	    break;
	}
    }
}

public static boolean isPrime(int n) {
	if(n == 1) {
	    return false;
	}

	for(int i=2; i <= n/2; i++) {
		System.out.println("Looping " +i);
		if(n % i == 0) {
			return false;
		}
	}
	return true;
}


public static double calculateInterest(double amount, double interestRate) {
	return(amount *(interestRate/100));
}


```
