# Ex19 Palindrome Check Using Deque
## DATE:23.3.26
## AIM:
To design a program that checks whether a given message is a palindrome by removing all non-alphanumeric characters, converting all characters to lowercase, and using a deque data structure for comparison.

## Algorithm
```
1.Start the program.
2.Read the input string from the user.
3.Remove all non-alphanumeric characters and convert the string to lowercase.
4.Use a deque to store characters of the string.
5.Compare characters from both ends of the deque.
6.If all pairs match, it’s a palindrome; otherwise, it’s not.
7.Display the result.
```
## Program:
```
Developed by: Ramya P
RegisterNumber: 212223230168 

```
```

import java.util.*;

public class PalindromeDeque {
    public static boolean isPalindrome(String str) {
        Deque<Character> deque = new LinkedList<>();
        for (char c : str.toCharArray()) {
            if (Character.isLetterOrDigit(c)) {
                deque.add(Character.toLowerCase(c));
            }
        }

        while (deque.size() > 1) {
            if (deque.removeFirst() != deque.removeLast())
                return false;
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a message: ");
        String message = sc.nextLine();
        if (isPalindrome(message))
            System.out.println("Palindrome");
        else
            System.out.println("Not a Palindrome");
        sc.close();
    }
}
```

## Output:

<img width="815" height="298" alt="image" src="https://github.com/user-attachments/assets/aaba5a1f-e91f-489b-83e1-f1509e3a3750" />


## Result:
The program successfully removes all non-alphanumeric characters, converts the text to lowercase, and uses a deque to efficiently compare characters from both ends. Hence, it determines whether the string is a palindrome.
