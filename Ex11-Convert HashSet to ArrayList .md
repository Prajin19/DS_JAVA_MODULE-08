# Ex11 Convert HashSet to ArrayList in Java
## DATE: 12-10-2025
## AIM:
To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
## Algorithm
1. Read n and insert n input integers into a HashSet to store unique values.
2. Call convertToArrayList to create an ArrayList by passing the HashSet.
3. Inside the method, construct a new ArrayList using the set to copy all elements.
4. Return the newly created ArrayList.
5. Print all elements of the ArrayList sequentially.


## Program:
```JAVA
/*
Program to To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
Developed by: Prajin S
RegisterNumber: 212223230151
*/
import java.util.*;

public class HashSetToArrayList {

    public static ArrayList<Integer> convertToArrayList(HashSet<Integer> set) {
        // Type Your Code Here.
        return new ArrayList<>(set);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        HashSet<Integer> set = new HashSet<>();
        for (int i = 0; i < n; i++) {
            int num = sc.nextInt();
            set.add(num);
        }

        ArrayList<Integer> list = convertToArrayList(set);
        System.out.println("ArrayList contents:");
        for (int num : list) {
            System.out.print(num + " ");
        }
        sc.close();
    }
}

```

## Output:
<img width="744" height="743" alt="image" src="https://github.com/user-attachments/assets/8e3fea1b-1d59-4596-873d-7146f20e3919" />


## Result:
The program successfully converts a collection of distinct integers stored in a HashSet into an ArrayList
