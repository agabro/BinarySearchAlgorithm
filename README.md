import java.util.Scanner;

public class BinarySearch {
    public static void main(String[] args) {
        int[] sortedArray = {5, 10, 15, 20, 30, 54, 76, 89, 111, 123};

        System.out.println("Enter the searching item: ");
        int searchingItem = new Scanner(System.in).nextInt();
        int firstIndex = 0;
        int lastIndex = 9;
        int middleIndex = (firstIndex + lastIndex) / 2;

        while (firstIndex <= lastIndex) {
            if (sortedArray[middleIndex] < searchingItem) {
                firstIndex = middleIndex + 1;
            } else if (sortedArray[middleIndex] == searchingItem) {
                System.out.println("Searching item: " + searchingItem + " found in the array.");
                break;
            } else {
                lastIndex = middleIndex - 1;
            }
            middleIndex = (firstIndex + lastIndex) / 2;

            if (firstIndex > lastIndex) {
                System.out.println("Searching item: " + searchingItem + " not found in the array.");
            }

        }
    }
}
