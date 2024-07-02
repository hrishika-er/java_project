Explanation:
Import Statement:

import java.util.Scanner; is used to import the Scanner class, which is used for getting user input.
Main Class and Method:

The class TemperatureConverter contains the main method, which is the entry point of the program.
Scanner Initialization:

Scanner scanner = new Scanner(System.in); creates a Scanner object to read input from the user.
Getting User Input:

double temperature = scanner.nextDouble(); reads the temperature value entered by the user.
char unit = scanner.next().charAt(0); reads the unit of measurement entered by the user. charAt(0) is used to get the first character of the input string.
Temperature Conversion:

If the user enters 'C' or 'c', the program converts the temperature from Celsius to Fahrenheit using the formula (temperature * 9/5) + 32.
If the user enters 'F' or 'f', the program converts the temperature from Fahrenheit to Celsius using the formula (temperature - 32) * 5/9.
Output:

The program prints the converted temperature.
If the user enters an invalid unit, the program prints an error message.
Closing Scanner:

scanner.close(); closes the Scanner object to free up resources.
You can run this program in any Java development environment or online Java compiler.

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

        scanner.close();
    }
}
