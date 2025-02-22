# fibonaccifac
EB3/61506/22   DAVID GITHUKU

public class FactorialAndFibonacci {

    // Method to calculate factorial
    public static long factorial(int n) {
        long result = 1;
        for (int i = 1; i <= n; i++) {
            result *= i;
        }
        return result;
    }

    // Method to calculate Fibonacci sequence
    public static long fibonacci(int n) {
        if (n <= 1) {
            return n;
        }
        long a = 0, b = 1, c;
        for (int i = 2; i <= n; i++) {
            c = a + b;
            a = b;
            b = c;
        }
        return b;
    }

    public static void main(String[] args) {
        // Test values
        int factorialInput = 20;
        int fibonacciInput = 40;

        // Measure the runtime for calculating factorial
        long startTime = System.nanoTime();
        long factorialResult = factorial(factorialInput);
        long endTime = System.nanoTime();
        long factorialTime = endTime - startTime;

        // Measure the runtime for calculating Fibonacci
        startTime = System.nanoTime();
        long fibonacciResult = fibonacci(fibonacciInput);
        endTime = System.nanoTime();
        long fibonacciTime = endTime - startTime;

        // Output results
        System.out.println("Factorial of " + factorialInput + " is: " + factorialResult);
        System.out.println("Time taken to calculate factorial: " + factorialTime + " nanoseconds");

        System.out.println("Fibonacci number at position " + fibonacciInput + " is: " + fibonacciResult);
        System.out.println("Time taken to calculate Fibonacci: " + fibonacciTime + " nanoseconds");
    }
}
