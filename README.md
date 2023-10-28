Java


A. Shuffling an array in Java can be achieved using the `Collections` class.

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


Javascript

A. Here's a JavaScript function that takes a sentence as input and reverses every word in that sentence:

```javascript
function reverseWords(sentence) {
    return sentence.split(' ').map(word => word.split('').reverse().join('')).join(' ');
}

// Example usage
const inputSentence = 'This is a sunny day';
const reversedSentence = reverseWords(inputSentence);
console.log(reversedSentence); // Output: shiT si a ynnus yad
```

B. Here's how you can sort an array in descending order using JavaScript:

```javascript
const array = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5];
array.sort((a, b) => b - a);

console.log(array);
```

This will output: `[9, 6, 5, 5, 5, 4, 3, 3, 2, 1, 1]` which is the sorted array in descending order.





Html

A. Basic Calculator:<!DOCTYPE html>
<html>
<head>
  <title>Basic Calculator</title>
  <style>
    /* Add your CSS styling here */
  </style>
</head>
<body>
  <div class="calculator">
    <input type="text" id="result" class="result" disabled>
    <button onclick="appendValue('1')">1</button>
    <button onclick="appendValue('2')">2</button>
    <button onclick="appendValue('3')">3</button>
    <button onclick="appendValue('+')">+</button>
    <button onclick="appendValue('4')">4</button>
    <button onclick="appendValue('5')">5</button>
    <button onclick="appendValue('6')">6</button>
    <button onclick="appendValue('-')">-</button>
    <button onclick="appendValue('7')">7</button>
    <button onclick="appendValue('8')">8</button>
    <button onclick="appendValue('9')">9</button>
    <button onclick="appendValue('*')">*</button>
    <button onclick="appendValue('0')">0</button>
    <button onclick="clearResult()">C</button>
    <button onclick="calculate()">=</button>
    <button onclick="appendValue('/')">/</button>
  </div>

  <script>
    // Add your JavaScript code here
  </script>
</body>
</html>



B. Survey Form:

<!DOCTYPE html>
<html>
<head>
  <title>Survey Form</title>
  <style>
    /* Add your CSS styling here */
  </style>
</head>
<body>
  <form id="surveyForm" onsubmit="submitForm(); return false;">
    <label for="firstName">First Name:</label>
    <input type="text" id="firstName" required><br><br>

    <label for="lastName">Last Name:</label>
    <input type="text" id="lastName" required><br><br>

    <label for="dob">Date of Birth:</label>
    <input type="date" id="dob" required><br><br>

    <label for="country">Country:</label>
    <select id="country" required>
      <option value="USA">USA</option>
      <option value="UK">UK</option>
      <option value="Canada">Canada</option>
      <!-- Add more options as needed -->
    </select><br><br>

    <label>Gender:</label><br>
    <input type="checkbox" id="male" name="gender" value="male">
    <label for="male">Male</label><br>
    <input type="checkbox" id="female" name="gender" value="female">
    <label for="female">Female</label><br><br>

    <label for="profession">Profession:</label>
    <input type="text" id="profession" required><br><br>

    <label for="email">Email:</label>
    <input type="email" id="email" required><br><br>

    <label for="mobile">Mobile Number:</label>
    <input type="tel" id="mobile" required><br><br>

    <button type="submit">Submit</button>
    <button type="button" onclick="resetForm()">Reset</button>
  </form>

  <script>
    // Add your JavaScript code here
  </script>
</body>
</html>

