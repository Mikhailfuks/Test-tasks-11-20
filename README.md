tasks 11 

import static org.junit.jupiter.api.Assertions.assertTrue;
import org.junit.jupiter.api.Test;

public class PersonTest {
    @Test
    public void testEquals() {
        Person person1 = new Person("Alice", 30);
        Person person2 = new Person("Alice", 30);
        assertTrue(person1.equals(person2));
    }
}

tasks 12 


public class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (obj == null || getClass() != obj.getClass()) return false;

        Person person = (Person) obj;

        if (age != person.age) return false;
        return name.equals(person.name);
    }

    @Override
    public int hashCode() {
        return 31 * name.hashCode() + age;
    }
}

tasks 13 

import java.util.Arrays;

public class MedianUtil {
    public double findMedian(int[] array) {
        Arrays.sort(array);
        int n = array.length;
        if (n % 2 == 0) {
            return (array[n / 2 - 1] + array[n / 2]) / 2.0;
        } else {
            return array[n / 2];
        }
    }
}

tasks 14 

public class ArraySearchUtil {
    public boolean contains(int[] array, int element) {
        for (int num : array) { 
            if (num == element) {
                return true;
            }
        }
        return false;
    }
}

tasks 15

public class FactorialUtil {
    public int factorial(int n) {
        if (n == 0) return 1;
        return n * factorial(n - 1);
    }
}

import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.Test;

public class FactorialUtilTest {
    @Test
    public void testFactorial() {
        FactorialUtil factorialUtil = new FactorialUtil();
        assertEquals(120, factorialUtil.factorial(5));
    }
}

tasks 16 

public class NumberUtil {
    public boolean isEven(int number) {
        return number % 2 == 0;
    }
}

import static org.junit.jupiter.api.Assertions.assertTrue;
import org.junit.jupiter.api.Test;

public class NumberUtilTest {
    @Test
    public void testIsEven() {
        NumberUtil numberUtil = new NumberUtil();
        assertTrue(numberUtil.isEven(4));
    }
}

tasks 17 

public class ArrayUtil {
    public int findMax(int[] numbers) {
        int max = numbers[0];
        for (int number : numbers) {
            if (number > max) {
                max = number;
            }
        }
        return max;
    }
}

import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.Test;

public class ArrayUtilTest {
    @Test
    public void testFindMax() {
        ArrayUtil arrayUtil = new ArrayUtil();
        assertEquals(5, arrayUtil.findMax(new int[]{1, 2, 5, 4}));
    }
}

tasks 18

public class PalindromeUtil {
    public boolean isPalindrome(String str) {
        String reversed = new StringBuilder(str).reverse().toString();
        return str.equals(reversed);
    }
}

import static org.junit.jupiter.api.Assertions.assertTrue;
import org.junit.jupiter.api.Test;

public class PalindromeUtilTest {
    @Test
    public void testIsPalindrome() {
        PalindromeUtil palindromeUtil = new PalindromeUtil();
        assertTrue(palindromeUtil.isPalindrome("madam"));
    }
}

tasks 19 

public class StringLengthUtil {
    public String compareLength(String str1, String str2) {
        return str1.length() > str2.length() ? str1 : str2;
    }
}

import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.Test;

public class StringLengthUtilTest {
    @Test
    public void testCompareLength() {
        StringLengthUtil stringLengthUtil = new StringLengthUtil();
        assertEquals("longer string", stringLengthUtil.compareLength("short", "longer string"));
    }
}





tasks 20 

public class MathUtil {
    public int add(int a, int b) {
        return a + b;
    }
}

import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.Test;

public class MathUtilTest {
    @Test
    public void testAdd() {
        MathUtil mathUtil = new MathUtil();
        assertEquals(5, mathUtil.add(2, 3));
    }
}
