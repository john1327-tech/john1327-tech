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
```
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the base (positive integer): ");
        int base = scanner.nextInt();
        System.out.print("Enter the exponent (positive integer): ");
        int exponent = scanner.nextInt();
        if (base <= 0 || exponent <= 0) {
            System.out.println("Both base and exponent must be positive.");
            return;
        }
        int sum = 0;
        int power = 1;
        System.out.println("Explanation:");
        for (int i = 1; i <= exponent; i++) {
            power *= base;
            sum += power;
            System.out.println(base + "^" + i + " = " + power + ",Sum = " + sum);
        }
        System.out.println("The total power of sum from " + base + "^1 to " + base + "^" + exponent + " is: " + sum);
        scanner.close();
    }
}
```
```
import java.util.Scanner;

public class SimpleRideHailingSystem {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Maximum number of bookings that can be made
        final int MAX_BOOKINGS = 50;
        
        // Arrays to hold booking details
        String[] passengerNames = new String[MAX_BOOKINGS];
        String[] dates = new String[MAX_BOOKINGS];
        String[] times = new String[MAX_BOOKINGS];
        String[] pickupLocations = new String[MAX_BOOKINGS];
        String[] dropoffLocations = new String[MAX_BOOKINGS];
        double[] distances = new double[MAX_BOOKINGS];
        double[] fares = new double[MAX_BOOKINGS];
        
        // Counter for the number of bookings made
        int bookingCount = 0;

        // Main loop for the application
        while (true) {
            // Display menu options
            System.out.println("\nRIDE-HAILING BOOKING SYSTEM");
            System.out.println("1. View All Bookings");
            System.out.println("2. Book a Ride");
            System.out.println("3. Delete a Booking");
            System.out.println("4. Generate Booking Report");
            System.out.println("5. Exit Application");
            System.out.print("Choose an option: ");
            int choice = scanner.nextInt();
            scanner.nextLine(); // Consume newline character after nextInt()

            // Option 1: View all bookings
            if (choice == 1) {
                if (bookingCount == 0) {
                    System.out.println("No bookings available.");
                } else {
                    System.out.println("\n# Date       Time      Passenger Name  Pick-up Location  Drop-off Location  Distance (km)  Fare (PHP)");
                    for (int i = 0; i < bookingCount; i++) {
                        // Display each booking's details
                        System.out.printf("%d %s %s %s %s %s %.1f %.2f\n", 
                            (i + 1), dates[i], times[i], passengerNames[i], 
                            pickupLocations[i], dropoffLocations[i], distances[i], fares[i]);
                    }
                }
            } 
            // Option 2: Book a ride
            else if (choice == 2) {
                if (bookingCount < MAX_BOOKINGS) {
                    // Collect booking details from the user
                    System.out.print("Enter Passenger Name: ");
                    passengerNames[bookingCount] = scanner.nextLine();
                    System.out.print("Enter Date (MM/DD/YYYY): ");
                    dates[bookingCount] = scanner.nextLine();
                    System.out.print("Enter Time (HH:MM AM/PM): ");
                    times[bookingCount] = scanner.nextLine();
                    System.out.print("Enter Pick-up Location: ");
                    pickupLocations[bookingCount] = scanner.nextLine();
                    System.out.print("Enter Drop-off Location: ");
                    dropoffLocations[bookingCount] = scanner.nextLine();
                    
                    // Get distance and calculate fare
                    System.out.print("Enter Distance (km): ");
                    distances[bookingCount] = scanner.nextDouble();
                    fares[bookingCount] = (distances[bookingCount] <= 1) ? 25.00 : 25.00 + (distances[bookingCount] - 1) * 20.00;

                    bookingCount++; // Increment the booking count
                    System.out.println("Booking successful!");
                } else {
                    System.out.println("Maximum booking limit reached.");
                }
            } 
            // Option 3: Delete a booking
            else if (choice == 3) {
                if (bookingCount == 0) {
                    System.out.println("No bookings to delete.");
                } else {
                    System.out.println("Enter the booking number to delete (1 to " + bookingCount + "): ");
                    int bookingNumber = scanner.nextInt();
                    if (bookingNumber > 0 && bookingNumber <= bookingCount) {
                        // Shift bookings to remove the selected one
                        for (int i = bookingNumber - 1; i < bookingCount - 1; i++) {
                            passengerNames[i] = passengerNames[i + 1];
                            dates[i] = dates[i + 1];
                            times[i] = times[i + 1];
                            pickupLocations[i] = pickupLocations[i + 1];
                            dropoffLocations[i] = dropoffLocations[i + 1];
                            distances[i] = distances[i + 1];
                            fares[i] = fares[i + 1];
                        }
                        bookingCount--; // Decrement the booking count
                        System.out.println("Booking deleted successfully!");
                    } else {
                        System.out.println("Invalid booking number.");
                    }
                }
            }
		// Option 4: Generate booking report
            else if (choice == 4) {
                if (bookingCount == 0) {
                    System.out.println("No bookings available.");
                } else {
                    System.out.println("\n# Date       Time      Passenger Name  Distance (km)  Fare (PHP)");
                    double totalDistance = 0;
                    double totalFare = 0;

                    for (int i = 0; i < bookingCount; i++) {
                        // Display each booking's distance and fare for the report
                        System.out.printf("%d %s %s %s %.1f %.2f\n", 
                            (i + 1), dates[i], times[i], passengerNames[i], 
                            distances[i], fares[i]);
                        totalDistance += distances[i]; // Accumulate total distance
                        totalFare += fares[i]; // Accumulate total fare
                    }
                    // Display total distance and fare
                    System.out.printf("Total Distance: %.1f km\n", totalDistance);
                    System.out.printf("Total Fare: %.2f PHP\n", totalFare);
                }
            } 
            // Option 5: Exit the application
            else if (choice == 5) {
                System.out.println("Exiting the application. Goodbye!");
                break; // Exit the loop and terminate the program
            } 
            // Invalid option handling
            else {
                System.out.println("Invalid option. Please try again.");
            }
        }
        scanner.close(); // Close the scanner resource
    }
}
```
```
https://www.programiz.com/online-compiler/8NwWrupPPBaId
```
```
import javax.swing.*;
import java.awt.*;

public class Totoybibo {

    public static void main(String[] args) {
        JFrame frame = new FutureValueFrame();
        frame.setVisible(true); 
    }
}

class FutureValueFrame extends JFrame {
    
    public FutureValueFrame() {
        setTitle("Future Value Calculator");
        setSize(267, 200);
        centerWindow(this);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        
        FutureValuePanel panel = new FutureValuePanel();
        this.add(panel);
        
        setLayout(new FlowLayout());
    }

    private void centerWindow(Window w) {
        Toolkit tk = Toolkit.getDefaultToolkit();
        Dimension d = tk.getScreenSize();
        setLocation((d.width - w.getWidth()) / 2, (d.height - w.getHeight()) / 2);
    }
    
    class FutureValuePanel extends JPanel { 
        private final JButton calculateButton;
        private final JButton exitButton;

        public FutureValuePanel() { 
            calculateButton = new JButton("Calculate");
            this.add(calculateButton);
            exitButton = new JButton("Exit");
            this.add(exitButton);
        }
    }
}
```
