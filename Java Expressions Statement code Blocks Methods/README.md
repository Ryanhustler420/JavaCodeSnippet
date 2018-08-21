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
# Methods return void

> methods help use to follow DRY Principle

```java
 
public static void main(String[] args) {

  boolean gameOver = true;
  int score = 800;
  int bonus = 100;
  int levelCompleted = 5;

  calculateScore(gameOver,score,bonus,levelCompleted);

  score = 10000;
  bonus = 200;
  levelCompleted = 8;

  calculateScore(true,score,bonus,levelCompleted);

} // <-- End main method

//use static when defining methods

public static void calculateScore(boolean gameOver,int score,int bonus,int levelCompleted) {			
  if(gameOver) {
    int finalScore = score + (levelCompleted * bonus);
    finalScore += 1000;
      System.out.println("Your final score was "+ finalScore);
  }
}
 
```

# method return something

```java
public static void main(String[] args) {

  boolean gameOver = true;
  int score = 800;
  int bonus = 100;
  int levelCompleted = 5;

  displayHighScorePosition("Gaurav",1500);
  displayHighScorePosition("Saurav",900);
  displayHighScorePosition("Sangeeta",400);
  displayHighScorePosition("Sarita",50);

  int valueBack = calculateScore(true,score,bonus,levelCompleted);

  score = 10000;
  bonus = 200;
  levelCompleted = 8;		

  valueBack = calculateScore(true,score,bonus,levelCompleted);
		
}
	
// this method returning an int  
public static int calculateScore(boolean gameOver,int score,int bonus,int levelCompleted) {
  if(gameOver) {
    int finalScore = score + (levelCompleted * bonus);
    finalScore += 1000;
    System.out.println("Your final score was "+ finalScore);
    return finalScore;
  }
  return -1;
}


public static void displayHighScorePosition(String PlayerName,int position) {
  System.out.println(PlayerName + " is managed to get into position " +
                                    calculateHighScorePosition(position) +
                                  " on the high score table.");
}

public static int calculateHighScorePosition(int playerScore) {
  int position = 0;
    if(playerScore >= 1000) {
      position = 1;
    }else if(playerScore >= 500 && playerScore < 1000) {
      position = 2;
    }else if(playerScore >= 100 && playerScore < 500) {
      position = 3;
    }else {
      position = 4;
    }
  return position; 
}

```
