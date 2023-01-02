# Comp-8.2

import java.util.Scanner;

public class Comp82 {

    public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
        int[] integs = new int[51];
        System.out.println("Enter integers -25 - 25 [enter -1 to quit]: ");
        int nums = scan.nextInt();
        while (nums != -1 && nums >= -25 && nums <= 25) {
            integs[nums+25]++;
            nums = scan.nextInt();
        }
        for (int index = 0; index <= 50; index++) {
            if (integs[index] > 0) {
                System.out.println(index-25 + " : " + integs[index]);
            }
        }
    }

}
