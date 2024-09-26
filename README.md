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

