# 2D-Array
import java.util.Arrays;
import java.util.Scanner;

public class TwoDArray {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Get dimensions from the user
        System.out.print("Enter the number of rows: ");
        int rows = scanner.nextInt();
        System.out.print("Enter the number of columns: ");
        int cols = scanner.nextInt();

        // Error handling for invalid input (optional but recommended)
        if (rows <= 0 || cols <= 0) {
            System.out.println("Rows and columns must be positive integers.");
            scanner.close();
            return; // Exit the program
        }


        // Create and initialize the 2D array
        int[][] array2D = new int[rows][cols];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                array2D[i][j] = i * j;
            }
        }

        // Print the 2D array
        System.out.println("Generated 2D array:");
        for (int[] row : array2D) {
            System.out.println(Arrays.toString(row));
        }

        scanner.close();
    }
}
