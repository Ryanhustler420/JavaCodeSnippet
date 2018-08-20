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

```
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

``` 
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

```
> has a width of 32bit (4 bytes)
  int myIntValue = 5 / 2;

> has a width of 32bit (4 bytes)
  float myFloatValue = 5f / 2f;
  float myFloatValueAlternative = (float) 5.4 / (float)2;

> has a width of 64bit (8 bytes)
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
```
double pound = 200d;
double kilogram = pound * 0.45359237;
System.out.println(kilogram);
_________________
>> 90.718474
```


**NOTE :-** int uses more space in memory so instead of using Integers data type you can use short! keep in mind the performence

# Casting

```
  byte myByteValue = -128;
  byte myNewBytevalue = (myByteValue/2); **throw error**
```
> simple fix

```
  byte = myNewBytevalue = (byte) (myByteValue/2);
```
