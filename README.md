
A. Shuffling an array in Java can be achieved using the `Collections` class. Here's an example:

```java
import java.util.ArrayList;
import java.util.Collections;

public class ShuffleArray {
    public static void main(String[] args) {
        ArrayList<Integer> arr = new ArrayList<>();
        arr.add(1);
        arr.add(2);
        arr.add(3);
        arr.add(4);
        arr.add(5);
        arr.add(6);
        arr.add(7);

        Collections.shuffle(arr);
        System.out.println(arr);
    }
}
```

B. To convert a Roman numeral to an integer in Java, you can use the following code:

```java
import java.util.HashMap;

public class RomanToInteger {
    public int romanToInt(String s) {
        HashMap<Character, Integer> romanMap = new HashMap<>();
        romanMap.put('I', 1);
        romanMap.put('V', 5);
        romanMap.put('X', 10);
        romanMap.put('L', 50);
        romanMap.put('C', 100);
        romanMap.put('D', 500);
        romanMap.put('M', 1000);

        int result = 0;
        int prevValue = 0;
        for (int i = s.length() - 1; i >= 0; i--) {
            int curValue = romanMap.get(s.charAt(i));
            if (curValue < prevValue) {
                result -= curValue;
            } else {
                result += curValue;
            }
            prevValue = curValue;
        }
        return result;
    }

    public static void main(String[] args) {
        RomanToInteger r = new RomanToInteger();
        String inputRoman = "IX";
        System.out.println(r.romanToInt(inputRoman));
    }
}
```

C. Checking if a sentence is a pangram in Java can be done as follows:

```java
public class PangramCheck {
    public static boolean isPangram(String sentence) {
        String lowerCaseSentence = sentence.toLowerCase();
        for (char c = 'a'; c <= 'z'; c++) {
            if (lowerCaseSentence.indexOf(c) < 0) {
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        String inputSentence = "The quick brown fox jumps over the lazy dog";
        if (isPangram(inputSentence)) {
            System.out.println("The input is a pangram.");
        } else {
            System.out.println("The input is not a pangram.");
        }
    }
}
```

Feel free to try these out and let me know if you need further assistance!
