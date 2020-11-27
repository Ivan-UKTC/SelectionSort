import java.util.*;

public class SelectionSort {
    public static void main(String[] args) {
    
        Scanner scan = new Scanner(System.in);

        int[] G = {25, 6, 44, 13, 20,35};
        int currentMinIDX = 0;
        int buff = 0;

        System.out.println("Before Sorting :" + Arrays.toString(G));

        for (int i = 0; i < G.length; i++) {
            currentMinIDX = i;

            for (int j = i; j < G.length; j++) {

                if (G[j] < G[currentMinIDX]) {
                    currentMinIDX = j;
                }
            }
                buff = G[i];
                G[i] = G[currentMinIDX];
                G[currentMinIDX] = buff;

        }
            System.out.println("After Sorting : " + Arrays.toString(G));
    }
}
