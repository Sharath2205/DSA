# BASICS TO PROGRAMMING

- [MATHS](#maths)
  - [Easy problems](#easy-problems)
    - [Count digits](#count-digits)
    - [Reverse Bits](#reverse-bits)
    - [Palindrome](#palindrome)
    - [LCM and GCD](#lcm-and-gcd)
  - [Medium Problems](#medium-problems)
    - [Reverse Integer](#reverse-integer)
- [RECURSION](#recursion)
- [HASHING](#hashing)

<a name="maths"></a>

## MATHS

<a name="easy-problems"></a>

## Easy problems

<a name="count-digits"></a>

### Count digits

[Problem link](https://practice.geeksforgeeks.org/problems/count-digits5716/1) - [article](https://takeuforward.org/data-structure/count-digits-in-a-number/) - [youtube solution](https://www.youtube.com/watch?v=1xNbjMdbjug)

Given a number N. Count the number of digits in N which evenly divides N.

Note :- Evenly divides means whether N is divisible by a digit i.e. leaves a remainder 0 when divided.

Example 1:

    Input:
    N = 12

    Output:
    2

    Explanation:
    1, 2 both divide 12 evenly

Example 2:

    Input:
    N = 23

    Output
    0

    Explanation:
    2 and 3, none of them divide 23 evenly

Constraints:

    1<=N<=105

Solution:

```java
class Solution{
    static int evenlyDivides(int N){
        // code here
        int x = N;
        int ans = 0;

        while(x > 0) {

            // Extract the last digit
            int temp = x % 10;

            // Check if the digit completely divived N
            // Handle divide by zero exception with temp != 0
            if(temp != 0 && N % temp == 0) ans++;

            x /= 10;
        }

        return ans;
    }
}
```

<a name="reverse-bits"></a>

### Reverse Bits

[Problem link](https://practice.geeksforgeeks.org/problems/reverse-bits3556/1) - [article](https://takeuforward.org/data-structure/count-digits-in-a-number/) - [youtube solution](https://www.youtube.com/watch?v=1xNbjMdbjug)

Given a 32 bit number X, reverse its binary form and print the answer in decimal.

Example 1:

    Input:
    X = 1

    Output:
    2147483648

    Explanation:
    Binary of 1 in 32 bits representation - 00000000000000000000000000000001
    Reversing the binary form we get, 10000000000000000000000000000000,
    whose decimal value is 2147483648.

Example 2:

    Input:
    X = 5

    Output:
    2684354560

    Explanation:
    Binary of 5 in 32 bits representation - 00000000000000000000000000000101
    Reversing the binary form we get, 10100000000000000000000000000000,
    whose decimal value is 2684354560.

Constraints:

    0 <= X < 2^32

solution

```java
class Solution {
    static Long reversedBits(Long X) {
        // code here
        long ans = 0, pow = 31;

        while(X != 0) {
            /*
                - Check if the last bit is 1
                - X & 1 gives 1 if the last bit is 1 or 0 if the bit is 0
                - Left shift the value with the pow such that it will be reversed
                - Example: input 1, binary rep is 00000000000000000000000000000001
                - On when the first set bit is encountered the value of pow is 31
                - So the set will be left shifted with 31
                - The value of 1 << 31 is 10000000000000000000000000000000
            */
            ans += ((X & 1) << pow--);
            X /= 2;
        }

        return ans;
    }
};
```

<a name="palindrome"></a>

### Palindrome

Given an integer, check whether it is a palindrome or not.

Example 1:

    Input: n = 555
    Output: Yes

Example 2:

    Input: n = 123
    Output: No

Constraints:

    1 <= n <= 1000

Solution:

```java
class Solution {
    public String is_palindrome(int N)
    {
        // Code here
        int rev = 0, temp = N;
        
        while (N != 0) {
            rev = rev * 10 + N % 10;
            N /= 10;
        }
        
        return (rev == temp) ? "Yes" : "No";
    }
}
```

<a name="lcm-and-gcd"></a>

### LCM and GCD

[Problem link](https://practice.geeksforgeeks.org/problems/lcm-and-gcd4516/1) - [article](https://takeuforward.org/data-structure/find-gcd-of-two-numbers/) - [youtube solution](https://practice.geeksforgeeks.org/problems/lcm-and-gcd4516/1)

Given two numbers A and B. The task is to find out their LCM and GCD.

Example 1:

    Input:
    A = 5 , B = 10

    Output:
    10 5

    Explanation:
    LCM of 5 and 10 is 10, while
    their GCD is 5.

Example 2:

    Input:
    A = 14 , B = 8

    Output:
    56 2
    
    Explanation:
    LCM of 14 and 8 is 56, while
    their GCD is 2.

Constraints:

    1<=N<=105

Solution:

```java
class Solution {
    static Long[] lcmAndGcd(Long A , Long B) {
        // code here
        long gcd = GCD(A, B);
        long lcm = (A * B) / gcd;
        return new Long[] {lcm, gcd};
    }
    
    static long GCD (long A, long B) {
        if (A == 0) return B;
        return GCD(B % A, A);
    }
}
```

<a name="medium-problems"></a>

### Medium Problems

<a name="reverse-integer"></a>

### Reverse Integer

Given a signed 32-bit integer `x`, return `x` with its digits reversed. If reversing `x` causes the value to go outside the signed 32-bit integer range `[-231, 231 - 1]`, then return `0`.

Assume the environment does not allow you to store 64-bit integers (signed or unsigned).

Example 1:

    Input: x = 123
    Output: 321

Example 2:

    Input: x = -123
    Output: -321

Example 3:

    Input: x = 120
    Output: 21

Constraints:

    -231 <= x <= 231 - 1

Solution:

```java
class Solution {
    public int reverse(int x) {
        int ans = 0;

        while (x != 0) {
            // Add pop after checking. It may cause overflow
            int pop = x % 10;
            x /= 10;

            /*
                - As per constraints the value of result should be -2^31 <= x <= 2^31 - 1
                - As we didn't add pop yet let's check with MAX / 10 ans MIN / 10
                - There are 2 edge cases here
                    - If the ans is greater || lesser than MAX / 10 || MIN / 10 it will cause overflow
                    - If the ans == MAX and the popped value is 7 the result will be overflowed ans if ans == MIN ans popped value is -8 the result will be less than Integer.MIN_VALUE.
                    - So in both cases return 0
                - Else return ans;
            */
            if (ans > Integer.MAX_VALUE / 10 || (ans == Integer.MAX_VALUE / 10 && pop > 7)) return 0;
            if (ans < Integer.MIN_VALUE / 10 || (ans == Integer.MIN_VALUE / 10 && pop < -8)) return 0;
            ans = (ans * 10) + pop;
        }
        return ans;
    }
}
```

<a name="recursion"></a>

### RECURSION

<a name="hashing"></a>

### HASHING
