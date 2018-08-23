# ArrayList

> GroceryList.java

```java

public class GroceryList {

	// java knows that this array is type int, so that's why we used 'int[]' here
	private int[] myNumber = new int[10];

	//But in arrayList we have to put Type inside <E> . this is a class
	// this has its own constructor

	private ArrayList<String> groceryList = new ArrayList<String>();

	public ArrayList<String> getGroceryList(){
		return groceryList;
	}


	public void addGroceryItem(String item) {
		groceryList.add(item);
	}

	public void printGroceryList() {
		System.out.println("You have " + groceryList.size() + " items int your  grocery list.");

		for(int i=0;i<groceryList.size();i++) {
			System.out.println((i+1) + ". " + groceryList.get(i));
		}
	}

	public void modifyGroceryItem(String currentItem ,String newItem) {
		int position = findItem(currentItem);
		if(position >= 0) {
			modifyGroceryItem(position,newItem);
		}
	}

	private void modifyGroceryItem(int position,String newItem) {
		groceryList.set(position, newItem);
		System.out.println("Grocery item " + (position + 1) + " has been modified.");
	}

	public void removeGroceryItem(String item) {
		int position = findItem(item);
		if(position >= 0) {
			removeGroceryItem(position);
		}
	}

	private void removeGroceryItem(int position) {
		groceryList.remove(position);
	}

	private int findItem(String searchItem) {
		return groceryList.indexOf(searchItem);
	}

	public boolean onFile(String searchItem) {
		int position = findItem(searchItem);
		if(position >= 0) {
			return true;
		}
		return false;
	}

}

```



> Main.java

```java

public class Main {

	private static Scanner scanner = new Scanner(System.in);
	private static GroceryList groceryList = new GroceryList();

	public static void main(String[] args) {
		boolean quit = false;
		int choice = 0;
		printInstructions();
		while (!quit) {
			System.out.print("Enter your choice: ");
			choice = scanner.nextInt();
			scanner.nextLine();

			switch (choice) {
			case 0:
				printInstructions();
				break;
			case 1:
				groceryList.printGroceryList();
				break;
			case 2:
				addItem();
				break;
			case 3:
				modifyItem();
				break;
			case 4:
				remove();
				break;
			case 5:
				searchItem();
				break;
			case 6:
				quit = true;
				break;
			}
		}
	}

	public static void printInstructions() {
		System.out.println("\n 0 - To print choice options.");
		System.out.println("\n 1 - To print the list of grocery.");
		System.out.println("\n 2 - To add an item to the list.");
		System.out.println("\n 3 - To modify an item to the list.");
		System.out.println("\n 4 - To remove an item from the list.");
		System.out.println("\n 5 - To search for an item in the list.");
		System.out.println("\n 6 - To quit the application.");
	}

	public static void addItem() {
		System.out.print("Please enter the grocery item: ");
		groceryList.addGroceryItem(scanner.nextLine());
		// groceryList.addGroceryItem(scanner.next());
	}

	public static void modifyItem() {
		System.out.print("current item name: ");
		String itemNo = scanner.nextLine();
		System.out.print("Enter new name for the item: ");
		String itemName = scanner.nextLine();
		groceryList.modifyGroceryItem(itemNo, itemName);
	}

	public static void remove() {
		System.out.print("Please enter item number: ");
		String itemNo = scanner.nextLine();
		scanner.nextLine();
		groceryList.removeGroceryItem(itemNo);
	}

	public static void searchItem() {
		System.out.print("Item to search for: ");
		String searchItem = scanner.nextLine();
		if (groceryList.onFile(searchItem)) {
			System.out.println("Found " + searchItem + " in our grocery list.");
		} else {
			System.out.println(searchItem + " is not on File.");
		}
	}

	// copy an ArrayList
	public static void processArrayList() {
		ArrayList<String> newArray = new ArrayList<String>();
		newArray.addAll(groceryList.getGroceryList());

		ArrayList<String> nextArray = new ArrayList<String>(groceryList.getGroceryList());

		String[] myArray = new String[groceryList.getGroceryList().size()];
		myArray = groceryList.getGroceryList().toArray(myArray);
	}

}

```