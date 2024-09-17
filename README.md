## Hi there 👋

<!--
**john1327-tech/john1327-tech** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->


// Online Java Compiler
// Use this editor to write, compile and run your Java code online

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


