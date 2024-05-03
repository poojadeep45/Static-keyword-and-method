package Pack1; // Package declaration

// Class providing basic calculator operations
public class Calculator {

    // Adds two double numbers and returns the result
    public static double add(double a, double b) {
        return a + b; // Return the sum of a and b
    }

    // Subtracts the second double from the first and returns the result
    public static double sub(double a, double b) {
        return a - b; // Return the difference between a and b
    }

    // Multiplies two double numbers and returns the result
    public static double multiply(double a, double b) {
        return a * b; // Return the product of a and b
    }

    // Divides the first double by the second and returns the result
    // Throws an exception if the second parameter is zero to avoid division by zero
    public static double divide(double a, double b) throws Exception {
        if (b == 0) {
            throw new Exception("Can't be divisible by Zero!"); // Division by zero error
        }
        return a / b; // Return the division result
    }
}

// Class providing additional mathematical utilities
class Mathutils {

    // Calculates the factorial of a non-negative integer
    // Throws IllegalArgumentException if the input is negative
    public static long factorial(int i) {
        if (i < 0) {
            throw new IllegalArgumentException("Factorial not defined for negative values");
        }
        long result = 1; // Initialize the result to 1 (factorial of zero or one is 1)
        for (int n = 1; n <= i; n++) { // Loop through numbers from 1 to i
            result *= n; // Multiply result by n
        }
        return result; // Return the factorial
    }

    // Checks if a given integer is prime
    public static boolean isPrime(int i) {
        if (i <= 1) { // 0, 1, and negative numbers are not prime
            return false;
        }
        for (int n = 2; n <= Math.sqrt(i); n++) { // Loop from 2 to sqrt(i)
            if (i % n == 0) { // If i is divisible by n, it's not prime
                return false;
            }
        }
        return true; // If no divisors found, i is prime
    }
}
