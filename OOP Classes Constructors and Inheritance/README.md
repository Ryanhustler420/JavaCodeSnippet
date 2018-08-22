# Classes Constructors and Inheritance Code Snippet

###### ***java Classes***

> Car.java

```java

public class Car {

    private int doors;
    private int wheels;
    private String model;
    private String engine;
    private String colour;

    public void setModel(String model) {
        String validModel = model.toLowerCase();
        if(validModel.equals("carrera") || validModel.equals("commodore")) {
            this.model = model;
        } else {
            this.model = "Unknown";
        }
    }

    public String getModel() {
        return this.model;
    }
}

```


> Main.java

```java

public class Main {

    public static void main(String[] args) {
	    Car porsche = new Car();
        Car holden = new Car();
        porsche.setModel("911");
        System.out.println("Model is " + porsche.getModel());
    }
}
```

# Classes with Constructors 

> Account.java

```java

public class Account {
    private String number;
    private double balance;
    private String customerName;
    private String customerEmailAddress;
    private String customerPhoneNumber;
    
    //Default Constructor
    public Account() {
        this("56789", 2.50, "Default name", "Default address", "default phone");
        System.out.println("Empty constructor called");
    }
    
    //Constructor with params
    public Account(String number, double balance, String customerName, String customerEmailAddress,
                   String customerPhoneNumber) {
        System.out.println("Account constructor with parameters called");
        this.number = number;
        this.balance = balance;
        this.customerName = customerName;
        this.customerEmailAddress = customerEmailAddress;
        this.customerPhoneNumber = customerPhoneNumber;
    }
    
    //Constructor calling other constructor
    public Account(String customerName, String customerEmailAddress, String customerPhoneNumber) {
        this("99999",100.55, customerName, customerEmailAddress, customerPhoneNumber);
    }

    public void deposit(double depositAmount) {
        this.balance += depositAmount;
        System.out.println("Deposit of " + depositAmount + " made.  New balance is " + this.balance);
    }

    public void withdrawal(double withdrawalAmount) {
        if(this.balance - withdrawalAmount <=0) {
            System.out.println("Only " + this.balance + " available. Withdrawal not processed");
        } else {
            this.balance -= withdrawalAmount;
            System.out.println("Withdrawal of " + withdrawalAmount + " processed.  Remaining balance = " + this.balance);
        }
    }
    
    //Getter's and Setter's
    
    public String getNumber() {
        return number;
    }

    public void setNumber(String number) {
        this.number = number;
    }

    public double getBalance() {
        return balance;
    }

    public void setBalance(double balance) {
        this.balance = balance;
    }

    public String getCustomerName() {
        return customerName;
    }

    public void setCustomerName(String customerName) {
        this.customerName = customerName;
    }

    public String getCustomerEmailAddress() {
        return customerEmailAddress;
    }

    public void setCustomerEmailAddress(String customerEmailAddress) {
        this.customerEmailAddress = customerEmailAddress;
    }

    public String getCustomerPhoneNumber() {
        return customerPhoneNumber;
    }

    public void setCustomerPhoneNumber(String customerPhoneNumber) {
        this.customerPhoneNumber = customerPhoneNumber;
    }
}

```

> VipPerson.java

```java

public class VipPerson {
    private String name;
    private double creditLimit;
    private String emailAddress;

    public VipPerson() {
        this("Default name", 50000.00, "default@email.com");
    }
    
    public VipPerson(String name, double creditLimit) {
        this(name, creditLimit, "unknown@email.com");
    }

    public VipPerson(String name, double creditLimit, String emailAddress) {
        this.name = name;
        this.creditLimit = creditLimit;
        this.emailAddress = emailAddress;
    }

    public String getName() {
        return name;
    }

    public double getCreditLimit() {
        return creditLimit;
    }

    public String getEmailAddress() {
        return emailAddress;
    }
}
```

> Main.java

```java

public class Main {

    public static void main(String[] args) {

        VipPerson person1 = new VipPerson();
        System.out.println(person1.getName());

        VipPerson person2 = new VipPerson("mike", 25000.00);
        System.out.println(person2.getName());

        VipPerson person3 = new VipPerson("Gaurav", 100.00, "gupta840065@email.com");
        System.out.println(person3.getName());
        System.out.println(person3.getEmailAddress());
    }
}

```
# Inheritance

> Animal.java

```java

public class Animal {

    private String name;
    private int brain;
    private int body;
    private int size;
    private int weight;

    public Animal(String name, int brain, int body, int size, int weight) {
        this.name = name;
        this.brain = brain;
        this.body = body;
        this.size = size;
        this.weight = weight;
    }

    public void eat() {
        System.out.println("Animal.eat() called");

    }

    public void move(int speed) {
        System.out.println("Animal.move() called.  Animal is moving at " +speed);

    }

    public String getName() {
        return name;
    }

    public int getBrain() {
        return brain;
    }

    public int getBody() {
        return body;
    }

    public int getSize() {
        return size;
    }

    public int getWeight() {
        return weight;
    }
}

```

> Dog.java

```java

public class Dog extends Animal {

    private int eyes;
    private int legs;
    private int tail;
    private int teeth;
    private String coat;

    public Dog(String name, int size, int weight, int eyes, int legs, int tail, int teeth, String coat) {
        super(name, 1, 1, size, weight);
        this.eyes = eyes;
        this.legs = legs;
        this.tail = tail;
        this.teeth = teeth;
        this.coat = coat;
    }

    private void chew() {
        System.out.println("Dog.chew() called");
    }

    @Override
    public void eat() {
        System.out.println("Dog.eat() called");
        chew();
        super.eat();
    }

    public void walk() {
        System.out.println("Dog.walk() called");
        super.move(5);
    }

    public void run() {
        System.out.println("Dog.run() called");
        move(10);

    }

    private void moveLegs(int speed) {
        System.out.println("Dog.moveLegs() called");
    }
    @Override
    public void move(int speed) {
        System.out.println("Dog.move() called");
        moveLegs(speed);
        super.move(speed);
    }
}

```

> Fish.java

```java

public class Fish extends Animal {

    private int gills;
    private int eyes;
    private int fins;

    public Fish(String name, int size, int weight, int gills, int eyes, int fins) {
        super(name, 1, 1, size, weight);
        this.gills = gills;
        this.eyes = eyes;
        this.fins = fins;
    }

    private void rest() {  }

    private void moveMuscles() {   }

    private void moveBackFin() {   }

    private void swim(int speed) {
        moveMuscles();
        moveBackFin();
        super.move(speed);
    }
}

```

> Main.java

```java

public class Main {

    public static void main(String[] args) {
	    Animal animal = new Animal("Animal", 1, 1, 5, 5);

        Dog dog = new Dog("Yorkie", 8, 20, 2, 4, 1, 20, "long silky");
        dog.eat();
        dog.walk();
        dog.run();

    }
}

```
