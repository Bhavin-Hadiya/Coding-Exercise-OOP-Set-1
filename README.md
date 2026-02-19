# Coding-Exercise-OOP-Set-1
Develop a Java program that prompts the user to enter a distance in meters. Your program shouldthen convert this distance to feet (1 meter = 3.28084 feet) and display the result formatted to twodecimal places.

import java.util.Scanner;

public class CE01 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter distance in meters: ");
        double meters = input.nextDouble();
        double feet = meters * 3.28084;
        System.out.printf("Distance in feet: %.2f\n", feet);
        input.close();
    }
}
Write a Java program to solve a system of two linear equations with two variables (e.g., ax + by =e and cx + dy = f). Prompt the user to enter the coefficients a, b, c, d, e, f. Calculate and display thevalues of x and y using Cramer's rule. Include error handling for cases where the denominator iszero Cramer's rule : D=ad−bc, Dx=ed−bf, Dy=af−ce, x=Dx/D, y=Dy/D

import java.util.Scanner;

public class CE02 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter a:");
        double a = input.nextDouble(); 
        System.out.println("Enter b:");
        double b = input.nextDouble();
        System.out.println("Enter c:");
        double c = input.nextDouble();
        System.out.println("Enter d:");
        double d = input.nextDouble();
        System.out.println("Enter e:");
        double e = input.nextDouble();
        System.out.println("Enter f:");
        double f = input.nextDouble();
        double D = (a * d) - (b * c);
        double Dx = (e * d) - (b * f);
        double Dy = (a * f) - (e * c);

   if (D == 0) {
            System.out.println("The equation has no unique solution (D = 0).");
        } else {
            double x = Dx / D;
            double y = Dy / D;
            System.out.printf("x = %.2f\n", x);
            System.out.printf("y = %.2f\n", y);
        }

}
}
Write a Java program that prompts the user to enter a single letter (character). Determine whether the entered character is a vowel (a, e, i, o, u, case-insensitive) or a consonant, and display the result.
import java.util.Scanner;

public class CE03 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a letter: ");
        char ch = sc.next().charAt(0);
        ch = Character.toLowerCase(ch);
        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
            System.out.println("It is a vowel.");
        } else if (ch >= 'a' && ch <= 'z') {
            System.out.println("It is a consonant.");
        } else {
            System.out.println("Invalid input. Please enter a letter.");
        }
    }
}
Develop a Java application that calculates a person's Body Mass Index (BMI). The program should ask the user for their weight in pounds and height in inches. Convert these values to kilograms and meters respectively (1 pound = 0.45359237 kg, 1 inch = 0.0254 meters) and then calculate BMI (weight in kg / (height in meters)^2). Display the calculated BMI.
import java.util.Scanner;

public class CE04 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter weight in pounds: ");
        double pounds = sc.nextDouble();
        System.out.print("Enter height in inches: ");
        double inches = sc.nextDouble();
        double weightKg = pounds * 0.45359237;
        double heightMeters = inches * 0.0254;
        double bmi = weightKg / (heightMeters * heightMeters);
        System.out.printf("Your BMI is: %.2f\n", bmi);
    }
}
Write a program that takes the lengths of three sides of a triangle as input. Calculate and print the area of the triangle. Ensure that the program validates if the given side lengths can actually form a triangle (sum of any two sides must be greater than the third side) before calculating the area (use Heron's formula: Area = sqrt(s*(s-a)*(s-b)*(s-c)) where s = (a+b+c)/2).
import java.util.Scanner;
public class CE05{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter side a: ");
        double a = sc.nextDouble();
        System.out.print("Enter side b: ");
        double b = sc.nextDouble();
        System.out.print("Enter side c: ");
        double c = sc.nextDouble();
        if (a + b > c && a + c > b && b + c > a) {
            double s = (a + b + c) / 2;
            double area = Math.sqrt(s * (s - a) * (s - b) * (s - c));
            System.out.printf("Area of the triangle: %.2f\n", area);
        } else {
            System.out.println("The given sides do not form a valid triangle.");
        }
    }
}

    }
}
