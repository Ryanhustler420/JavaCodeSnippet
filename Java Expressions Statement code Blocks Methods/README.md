# if keyword and code blocks

> code blocks are building blocks of program

```java

boolean gameOver = true;
int score = 5000;
int bonus = 100;
int levelCompleted = 5;

// for more than one statement
if (score == 5000) {
  System.out.println("Your score was 5000");
}

// Your score was 5000

// possible if you have only one statement
if (score == 5000)
  System.out.println("Your score was 5000");

System.out.println("This was executed");

// Your score was 5000
// This was executed

// OR

if (score == 4000)
  System.out.println("Your score was 5000");

System.out.println("This was executed");

// This was executed

// OR

if (score == 5000) {
  System.out.println("Your score was 5000");
  System.out.println("This was executed");
}
// Your score was 5000
// his was executed

// NOTE : Always use Curly bracket because code looks cleaner


//Flow

if (score < 5000) {
  System.out.println("Your score was 5000");
}else {
  System.out.println("Got here");
}

// Got here

if (score <= 5000) {
  System.out.println("Your score was 5000");
}else {
  System.out.println("Got here");
}

// Your score was 5000


if (score < 5000 && score > 1000) {
  System.out.println("Your score was less than 5000 but greater than 1000");
}else if(score < 1000) {
  System.out.println("Your score was less than 1000");
}else {
  System.out.println("Got here");
}

// Got here

// Scope

if(gameOver) {
  int finalScore = score + (levelCompleted * bonus);
  System.out.println("Your final score was "+ finalScore);
}

//	int savedFinalScore = finalScore; //Wrong Expression because 'finalScore' is local Variable



```
