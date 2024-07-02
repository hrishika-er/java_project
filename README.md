//Temperature converter description: create a program that converts temperatures between celsius and fahrenheit. prompt the user to enter a temperature value and the unit of measurement, and then perform the conversion. display the converted temperature. 


//Here's a simple Java program that converts temperatures between Celsius and Fahrenheit. The program prompts the user to enter a temperature value and the unit of measurement, performs the conversion, and then displays the converted temperature.



import java.util.Scanner;

public class abc {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the temperature value:");
        double temperature = scanner.nextDouble();

        System.out.println("Enter the unit of measurement (C for Celsius, F for Fahrenheit):");
        char unit = scanner.next().charAt(0);

        if (unit == 'C' || unit == 'c') {
            double fahrenheit = (temperature * 9/5) + 32;
            System.out.println(temperature + "°C is equal to " + fahrenheit + "°F");
        } else if (unit == 'F' || unit == 'f') {
            double celsius = (temperature - 32) * 5/9;
            System.out.println(temperature + "°F is equal to " + celsius + "°C");
        } else {
            System.out.println("Invalid unit of measurement.");
        }

