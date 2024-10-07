## Hi there 👋

// Sample if statement code
```
import java.util.Scanner;
public class Myclass {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.println("Grade");
        double Grade = scan.nextDouble();
     if (Grade >=90 && Grade <= 100){
           System.out.print("A+");
       }
       else if (Grade >=80 && Grade <= 90){
           System.out.print("B+");
       }
       else if (Grade >=75 && Grade <=80){
           System.out.print("C+");
       }
       else{
           System.out.print("BoBo");
        }   
    }
}
```


```
import java.util.Scanner;

public class Myclass {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String membershipLevel = "";
        double purchaseAmount = 0;
        double discountRate = 0;

        System.out.print("Enter membership level (Silver, Gold, Platinum):");
        membershipLevel = scan.nextLine();

        System.out.print("Enter purchase amount: ");
        if (scan.hasNextDouble()) {
            purchaseAmount = scan.nextDouble();
            scan.nextLine();
            if (purchaseAmount <= 0) {
                System.out.println("Invalid purchase amount.");
                return;
            }
        } else {
            System.out.println("Invalid input. Please enter a number.");
            return;
        }

        if (membershipLevel.equalsIgnoreCase("Silver")) {
            discountRate = 0.05;
        } else if (membershipLevel.equalsIgnoreCase("Gold")) {
            discountRate = 0.10;
        } else if (membershipLevel.equalsIgnoreCase("Platinum")) {
            discountRate = 0.15;
        }

        if (purchaseAmount > 1000) {
            discountRate += 0.10;
        } else if (purchaseAmount > 500) {
            discountRate += 0.05;
        }

        double finalPrice = purchaseAmount - (purchaseAmount * discountRate);

        System.out.printf("Your final price after discount is: %.2f%n", finalPrice);
        if (finalPrice > 1000) {
            System.out.println("Wow yaman haup");
        } else if (finalPrice >= 500) {
            System.out.println("Nakatipid naman kahit papano salamat");
        } else {
            System.out.println("Gumamit ka na nang membership makakatipid ka");
        }
    }
}
```

```
import java.util.Scanner;

class HelloWorld {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the starting number:");
        int start = scanner.nextInt();
        System.out.println("Enter the ending number:");
        int end = scanner.nextInt();
        System.out.print("Even numbers from " + start + " to " + end + ":");
        for (int number = start; number <= end; number++) {
            if (number % 2 == 0) {
                System.out.println(number);
            }
        }
        
    }
}
```
```
import java.util.Scanner;

class HelloWorld {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter the starting number:");
        int begin = scanner.nextInt();
        
        System.out.print("Enter the ending number:");
        int end = scanner.nextInt();
        
        while ((begin % end ) !=0) {
            System.out.println(begin);
            begin+=2;
        }
            }
        }
        
    

```
```
import java.util.Scanner;

public class NumberChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int choice = 0;

        while (choice != 4) {
            
            System.out.println("Choose an option:");
            System.out.println("1. Check if this number is odd or even");
            System.out.println("2. Check if this number is prime or composite");
            System.out.println("3. Check if this number is perfect, deficient, or abundant");
            System.out.println("4. Close Program");

            choice = scanner.nextInt();

            if (choice == 1) {
                System.out.print("Enter a positive Number: ");
                int number = scanner.nextInt();
                while (number <= 0) {
                    System.out.println("Error: Please enter a positive Number.");
                    number = scanner.nextInt();
                }
                if (number % 2 == 0) {
                    System.out.println(number + " is even.");
                } else {
                    System.out.println(number + " is odd.");
                }
            } else if (choice == 2) {
                System.out.print("Enter a positive Number: ");
                int number = scanner.nextInt();
                while (number <= 0) {
                    System.out.println("Error: Please enter a positive Number.");
                    number = scanner.nextInt();
                }
                if (number <= 1) {
                    System.out.println(number + " is neither prime nor composite.");
                } else {
                    int count = 0;
                    for (int i = 1; i <= number; i++) {
                        if (number % i == 0) {
                            count++;
                        }
                    }
                    if (count == 2) {
                        System.out.println(number + " is prime.");
                    } else {
                        System.out.println(number + " is composite.");
                    }
                }
            } else if (choice == 3) {
                System.out.print("Enter a positive Number: ");
                int number = scanner.nextInt();
                while (number <= 0) {
                    System.out.println("Error: Please enter a positive Number.");
                    number = scanner.nextInt();
                }
                int sum = 0;
                for (int i = 1; i < number; i++) {
                    if (number % i == 0) {
                        sum += i;
                    }
                }
                if (sum == number) {
                    System.out.println(number + " is a perfect number.");
                } else if (sum < number) {
                    System.out.println(number + " is a deficient number.");
                } else {
                    System.out.println(number + " is an abundant number.");
                }
            } else if (choice == 4) {
                System.out.println("Closing Program Now.");
            } else {
                System.out.println("Invalid Number. Please try again.");
            }
        }

        scanner.close();
    }
}
```
```
import java.util.Scanner;

public class NumberClassification {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int choice;

        do {
            // Display the menu with top and bottom borders only
            System.out.println("***************************************");
            System.out.println("       Number Classification Menu      ");
            System.out.println("***************************************");
            System.out.println(" 1. Check if the number is odd or even ");
            System.out.println(" 2. Check if the number is prime or    ");
            System.out.println("    composite                         ");
            System.out.println(" 3. Check if the number is perfect,    ");
            System.out.println("    deficient, or abundant             ");
            System.out.println(" 4. Exit                              ");
            System.out.println("***************************************");
            System.out.print("Enter your choice: ");
            
            // Input choice from the user
            choice = scanner.nextInt();
            
            if (choice == 1) {
                System.out.print("Enter a positive integer: ");
                int num = scanner.nextInt();
                if (num > 0) {
                    if (num % 2 == 0) {
                        System.out.println(num + " is even.\n");
                    } else {
                        System.out.println(num + " is odd.\n");
                    }
                } else {
                    System.out.println("Invalid input! Enter a positive integer.\n");
                }
            } else if (choice == 2) {
                System.out.print("Enter a positive integer: ");
                int num = scanner.nextInt();
                if (num > 1) {
                    boolean isPrime = true;
                    // Check for factors from 2 to num-1
                    for (int i = 2; i < num; i++) {
                        if (num % i == 0) {
                            isPrime = false;
                            break;
                        }
                    }
                    if (isPrime) {
                        System.out.println(num + " is a prime number.\n");
                    } else {
                        System.out.println(num + " is a composite number.\n");
                    }
                } else {
                    System.out.println("Invalid input! Enter a number greater than 1.\n");
                }
            } else if (choice == 3) {
                System.out.print("Enter a positive integer: ");
                int num = scanner.nextInt();
                if (num > 0) {
                    int sum = 0;
                    for (int i = 1; i <= num / 2; i++) {
                        if (num % i == 0) {
                            sum += i;
                        }
                    }
                    if (sum == num) {
                        System.out.println(num + " is a perfect number.\n");
                    } else if (sum < num) {
                        System.out.println(num + " is an abundant number.\n");
                    } else {
                        System.out.println(num + " is a deficient number.\n");
                    }
                } else {
                    System.out.println("Invalid input! Enter a positive integer.\n");
                }
            } else if (choice == 4) {
                System.out.println("Exiting program. Thank you!\n");
            } else {
                System.out.println("Invalid choice. Please try again.\n");
            }
        } while (choice != 4);
    }
}
```
