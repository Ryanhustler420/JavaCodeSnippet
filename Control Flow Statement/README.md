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
