# JavaCodeSnippet

primitive data types are 8 in total<br />
which is defined by java language and it is named as special reserved keyword

- byte
- short
- int
- long
- float
- double
- char
- boolean
> And there is one more which is also considerd as primitive data type
- string

## Variable declaration in java
*int has a width of 32bit (4 bytes)*
- int myMinValue = -2147483648;
-	int myMaxValue = 2147483647;

> you can use number like this which come in java 7

- int myMinValue = -21_474_836_48;
-	int myMaxValue = 21_474_836_47;

*float has a width of 32bit (4 bytes)*
- float myFloatValue = 5f;
- float myFloatValueAlternative = (float) 5.4;

*double has a width of 64bit (8 bytes)*
- double myDoubleValue = (double) 5;
- double myDoubleValueAlternative = 5d;

*width of 16 (2 bytes)*
- char myChar = 'aa'; **Wrong**
- char myChar = 'A'   **Right**
- char symbol = '\u00A9';

*byte has a width of 8 bit*
- byte myByteMinValue = -128;
- byte myByteMaxValue = 127;

*short has a width of 16bit*
- short myShortValue = -32768;
- short myLargestValue = 32767;

*long has a width of 64*
- long myLongValue = -9_223_372_036_854_775_808L;
- long myLongValue = 9_223_372_036_854_775_807L;
- boolean myBoolean = false;
- boolean isMale = true;

- String myString = "This is a String";
- String myString = "This is a String" + ", this is more string";

```java
String numberString = "250.55";
numberString = numberString + "49.95";
System.out.println("The result is " + numberString);
//The result is 250.5549.95
		
String lastString = "10";
int myInt = 50;
lastString = lastString + myInt;
System.out.println("LastString is equal to " + lastString);
//LastString is equal to 1050
				
```

## Code example

```java 
int myIntValue = 5;
float myFloatValue = 5f;
float myFloatValueAlternative = (float) 5.4;
double myDoubleValue = (double) 5;
double myDoubleValueAlternative = 5d;
System.out.println("myInt:" + myIntValue);
System.out.println("myFloatValue:" + myFloatValue);
System.out.println("myFloatValueAlternative:" + myFloatValueAlternative);
System.out.println("myDoubleValue:" + myDoubleValue);
System.out.println("myDoubleValueAlternative:" + myDoubleValueAlternative);

```
## Result

```
  myInt:5
  myFloatValue:5.0
  myFloatValueAlternative:5.4
  myDoubleValue:5.0
  myDoubleValueAlternative:5.0

```

## Complete Primitive Example

```java
//has a width of 32bit (4 bytes)
  int myIntValue = 5 / 2;

//has a width of 32bit (4 bytes)
  float myFloatValue = 5f / 2f;
  float myFloatValueAlternative = (float) 5.4 / (float)2;

//has a width of 64bit (8 bytes)
  double myDoubleValue = (double) 5/2;
  double myDoubleValueAlternative = 5d  /2d;
  System.out.println("myInt:" + myIntValue);
  System.out.println("myFloatValue:" + myFloatValue);
  System.out.println("myFloatValueAlternative:" + myFloatValueAlternative);
  System.out.println("myDoubleValue:" + myDoubleValue);
  System.out.println("myDoubleValueAlternative:" + myDoubleValueAlternative);

  myInt:2
  myFloatValue:2.5
  myFloatValueAlternative:2.7
  myDoubleValue:2.5
  myDoubleValueAlternative:2.5

```

**use double in java which is recommended way because of correctness value and java inbuild class also uses double like math class**
> convert a give number of pound to kilogram
```java
double pound = 200d;
double kilogram = pound * 0.45359237;
System.out.println(kilogram);
_________________
>> 90.718474
```


**NOTE :-** int uses more space in memory so instead of using Integers data type you can use short! keep in mind the performence

# Casting

```java
  byte myByteValue = -128;
  byte myNewBytevalue = (myByteValue/2); **throw error**
```
> simple fix

```java
  byte = myNewBytevalue = (byte) (myByteValue/2);
```

# Operators

```java
// Adding
int result = 1 + 2;
System.out.println("1 + 2" + result);


int previousResult = result;

//Subtracting
result = result - 1;
System.out.println(previousResult + " - 1 =" + result);

previousResult = result;

// Multiply
result = result * 10;
System.out.println(previousResult + " * 10 ="  + result);

previousResult = result;

// Divide
result = result */10;
System.out.println(previousResult + " / 5 ="  + result);

previousResult = result;

//reminder
result = result % 3;
System.out.println(previousResult + " % 3 ="  + result);

previousResult = result;

//Adding using short hand x++;
result = result++;
System.out.println("Result is now "  + result);

```

## diffrence between single = and ==
```java
boolean isAlien = false;	// assigning

if(isAlien == false)		//compairing
	Ststem.out.println('Its not an Alien');

int topScore = 100;

if(topScore == 100)
	Ststem.out.println('You got the high score');

if(topScore >= 100)
if(topScore != 100)
if(topScore <= 100)
if(topScore <= 100 || topScore >= 0)
if(topScore <= 100 && topScore >= 0)

```
> ternary in java

```java
boolean isCar = true;
boolean wasCar = isCar ? true : false;
```


> short hand 
- result += 2;
- result *= 10;
- result -= 10;
- result /= 10;


# Keywords And Expressions

**java has 50 reserve keywords**

here is the complete list of Keywords [Java Keywords List](https://en.wikipedia.org/wiki/List_of_Java_keywords) & [here](https://javaconceptoftheday.com/java-keywords-with-examples/).

> int int = 5; **wrong** <br />
> int int2 = 5; **right**

## expression = are building blocks of java programs

> double kilometers = (100 * 1.609344); <br />
kilometers = (100 * 1.609344); this is expression including variable name except datatype


## Code snippet
```java
int highScore = 50; 	// this is expression except datatype and semicolon

if(highScore == 50) { 	// this is expression

	System.out.println("This is an expression");
		// ("This is an expression") <- this is expression except "System.out.println"
		//NOTE : - anything withen bracket is called expression

	int score = 100; 
		// score = 100 is expression except datatype and semicolon
}
```

## convert a String into an array of Strings containing one character each

```java
String[] result = input.split("(?!^)");
```
> What this does is split the input String on all empty Strings that are not preceded by the beginning of the String.

``or``

```java

String x = "gauravgupta";
String [] y = x.split("");

```
``or``

```java

String test = "aabbab ";
char[] t = test.toCharArray();

for(char c : t)
    System.out.println(c);    

System.out.println("The end!");    

```

## Getting input from user in Console without using Scanner

> if you are using the Java SE6 or higher then you can make use of Console class

```java

   Console console = System.console();
   if (console==null){
      System.out.print("console not available ");
   }else {
      String line = console.readLine("Enter name :");
      System.out.print("your name :"+line);
   }

```


## How to convert a char to a String?

```java

// 1. 
String stringValueOf = String.valueOf('c'); // most efficient

// 2. 
String stringValueOfCharArray = String.valueOf(new char[]{x});

// 3. 
String characterToString = Character.toString('c');

// 4. 
String characterObjectToString = new Character('c').toString();

   // Although this method seems very simple, 
   // this is less efficient because the concatenation
   // expands to new StringBuilder().append(x).append("").toString();

// 5. 
String concatBlankString = 'c' + "";

// 6. 
String fromCharArray = new String(new char[]{x});

```

## Converting String to char Array

```java

public static void main(String[] args) {
	String testString = "This Is Test";
	char[] stringToCharArray = testString.toCharArray();

	for (char output : stringToCharArray) {
		System.out.println(output);
	}
}

```

## Remove Duplicate String in String Array

```java

String a = "ThisIsASimpleStringWithExampleOfDuplicateCharacter";
String s[] = (a).split("(?!^)");
int counter = 26;

String[] array = Arrays.stream(s).distinct().toArray(String[]::new);


for(int i=0;i<array.length-1;i++) {
		System.out.print(array[i]);
}

```

## convert string array to string in Java

> Use Arrays.toString method
```java
public class ArrayToString    {
      	public static void main(String[] args){      
 	
	String[] strArray = new String[]{"Java", "PHP", ".NET", "PERL", "C", "COBOL"};
        String newString = Arrays.toString(strArray);
        newString = newString.substring(1, newString.length()-1);           
        System.out.println("New New String: " + newString); 

 }

}
```

## Example of a String Contains all Alphabate or not

```java

int counter = 0;
//String a = "toosmallword".toUpperCase();
String s[] = (str.toUpperCase()).split("(?!^)");
String[] array = Arrays.stream(s).distinct().toArray(String[]::new); //[a,b,c,d,e,f]

for (int i = 0; i < array.length; i++) {
	int val = (int) array[i].charAt(0) - 64;
	if(val > 0 && val < 27) {
		counter++;				
	}
}

//System.out.println(counter);

if(counter==26){
	System.out.println("YES");
}else{
	System.out.println("NO");
}


```

## convert a char to int in Java

> As it happens, the ascii/unicode value of the character '9' is nine greater than the value of '0' (similarly for the other digits).
So you can get the int value of a decimal digit char using subtraction.

```java

char x = '9';
int y = x - '0'; // will gives 9

```


## convert minutes to Hours and minutes (hh:mm) in java

```java

int hours = t / 60; //since both are ints, you get an int
int minutes = t % 60;
System.out.printf("%d:%02d", hours, minutes);

```
