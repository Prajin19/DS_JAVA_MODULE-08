# Ex14 Tracking the First Unique Number in a Stream using LinkedHashMap
## DATE: 12-10-2025
## AIM:
To implement a program that tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.

## Algorithm
1. Read n and process n incoming numbers from the stream.
2. Use a LinkedHashMap to store each number along with a boolean indicating whether it is still unique.
3. For each new number, set its value to true if it appears for the first time, or set it to false if it repeats.
4. After each insertion, scan the LinkedHashMap in insertion order to find the first number whose boolean value is true.
5. Print that number as the first unique number, or print “No unique number” if none exists.

## Program:
```JAVA
/*
Program to tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.
Developed by: Prajin S
RegisterNumber: 212223230151
*/
import java.util.*;

public class FirstUniqueNumberStream {

    public static void processStream(int n, Scanner sc) {
        // Type Your Code Here.
        LinkedHashMap<Integer,Boolean> map=new LinkedHashMap<>();
        for(int i=0;i<n;i++){
            int num=sc.nextInt();
            if(map.containsKey(num))
            map.put(num,false);
            else
            map.put(num,true);
            
            int firstUnique=-1;
            for(Map.Entry<Integer,Boolean> entry : map.entrySet()){
                if(entry.getValue()){
                    firstUnique=entry.getKey();
                    break;
                }
            }
            if(firstUnique==-1)
            System.out.println("No unique number");
            else
            System.out.println("First unique number: "+firstUnique);
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        processStream(n, sc);
        sc.close();
    }
}

```

## Output:
<img width="815" height="689" alt="image" src="https://github.com/user-attachments/assets/d3ea29cc-a32a-41b7-a6a2-044c59f7a5b7" />



## Result:
The program successfully tracks and returns the first unique number at any point in the integer stream using a LinkedHashMap.
