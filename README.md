# PATTERNS

* Pattern 1
[
        ![Alt text](https://takeuforward.org/wp-content/uploads/2022/08/P1.png)
    ](#pattern-1)
<br>

* Pattern 2
[
        ![Alt text](https://takeuforward.org/wp-content/uploads/2022/08/P2.png)
    ](#pattern-2)
<br>

* Pattern 3
[
        ![Alt text](https://takeuforward.org/wp-content/uploads/2022/08/P3.png)
    ](#pattern-3)
<br>


* Pattern 4
[
        ![Alt text](https://takeuforward.org/wp-content/uploads/2022/08/P4.png)
    ](#pattern-4)<br>

* Pattern 5
[
        ![Alt text](https://takeuforward.org/wp-content/uploads/2022/08/P5.png)
    ](#pattern-5)
<br>

* Pattern 6
  [
        ![Alt text](https://takeuforward.org/wp-content/uploads/2022/08/P6.png)
    ](#pattern-6)
<br>

* Pattern 7
  [
    ![Alt text](https://takeuforward.org/wp-content/uploads/2022/08/P7.png)
  ](#pattern-7)
  <br>

* Pattern 8
    [
        ![Alt text](https://takeuforward.org/wp-content/uploads/2022/08/P8.png)
    ](#pattern-8)
    <br>


* Pattern 9
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P9.png)](#pattern-9)
  <br>

* Pattern 10
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P10.png)
  ](#pattern-10)
  <br>

* Pattern 11
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P11.png)
  ](#pattern-11)
  <br>


* Pattern 12
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P12.png)
  ](#pattern-12)
  <br>


* Pattern 13
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P13.png)
  ](#pattern-13)
  <br>

* Pattern 14
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P14.png)
  ](#pattern-14)
  <br>

* Pattern 15
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P15.png)
  ](#pattern-15)
  <br>

* Pattern 16
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P16.png)
  ](#pattern-16)
  <br>

* Pattern 17
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P17.png)
  ](#pattern-17)
  <br>

* Pattern 18
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P18.png)
  ](#pattern-18)
  <br>

* Pattern 19
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P19.png)
  ](#pattern-19)
  <br>

* Pattern 20
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P20.png)
  ](#pattern-20)
  <br>

* Pattern 21
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P21.png)
  ](#pattern-21)
  <br>

* Pattern 22
  [![Alt Text](https://takeuforward.org/wp-content/uploads/2022/08/P22.png)
  ](#pattern-22)
  <br>


---

<a id="pattern-1"></a>
### Pattern 1

    Input: 5

    Output:
    * * * * *
    * * * * *
    * * * * *
    * * * * *
    * * * * *

```java
import java.io.*;
import java.util.*;

class Main {
    // Driver code
    public static void main(String[] args) throws Exception {
        BufferedReader br =
            new BufferedReader(new InputStreamReader(System.in));
        int t = Integer.parseInt(br.readLine().trim());
        while (t-- > 0) {
            int n = Integer.parseInt(br.readLine().trim());
            Solution obj = new Solution();
            obj.printSquare(n);
        }
    }
}


class Solution {

    void printSquare(int n) {
        // code here
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```


<a id="pattern-2"></a>
### Pattern 2

    Input: 5

    Output:
    * 
    * * 
    * * * 
    * * * * 
    * * * * *

```java
import java.io.*;
import java.util.*;

class Main {
    // Driver code
    public static void main(String[] args) throws Exception {
        BufferedReader br =
            new BufferedReader(new InputStreamReader(System.in));
        int t = Integer.parseInt(br.readLine().trim());
        while (t-- > 0) {
            int n = Integer.parseInt(br.readLine().trim());
            Solution obj = new Solution();
            obj.printTriangle(n);
        }
    }
}


class Solution {

    void printTriangle(int N) {
        // code here
        for (int i = 0; i < N; i++) {
            for (int j = 0; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-3"></a>
### Pattern 3

    Input: 5

    Output:
    1
    1 2 
    1 2 3 
    1 2 3 4 
    1 2 3 4 5

```java
class Solution {

    void printTriangle(int N) {
        // code here
        for (int i = 1; i <= N; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-4"></a>
### Pattern 4

    Input: 5

    Output:
    1
    2 2 
    3 3 3 
    4 4 4 4 
    5 5 5 5 5

```java
class Solution {
    void printTriangle(int N) {
        // code here
        for (int i = 1; i <= N; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(i + " ");
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-5"></a>
### Pattern 5

    Input: 5

    Output:
    * * * * *
    * * * * 
    * * * 
    * *  
    *

```java
class Solution {

    void printTriangle(int N) {
        // code here
        
        for (int i = N; i >= 1; i--) {
            for (int j = i; j >= 1; j--) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-6"></a>
### Pattern 6

    Input: 5

    Output:
    1 2 3 4 5
    1 2 3 4
    1 2 3 
    1 2  
    1 

```java
class Solution {

    void printTriangle(int N) {
        // code here
        
        for (int i = N; i > 0; i--) {
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-7"></a>
### Pattern 7

    Input: 5

    Output:

        *
       ***  
      *****
     *******
    *********

```java
class Solution {

    void printTriangle(int N) {
        // code here
        for (int i = 0; i < N; i++) {
            // for spacing before each row
            for(int j = 0; j < N - i - 1; j++) {
                System.out.print(" ");
            }
            
            // Stars
            // ***0 indexing*** 
            // On row 0 it is 1, on row 1 it is 3, on row 2 it is 5 and on row 3 it is (3 * 2 + 1) = 7
            // We can write it as (row * 2 + 1)
            
            for(int j = 0; j < i * 2 + 1; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-8"></a>
### Pattern 8

    Input: 5

    Output:

    *********
     *******
      *****
       ***
        *


```java
class Solution {

    void printTriangle(int N) {
        // code here
        for (int i = N; i > 0; i--) {
            for(int j = 0; j < N - i; j++) {
                System.out.print(' ');
            }
            for(int j = 0; j < i * 2 - 1; j++) {
                System.out.print('*');
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-9"></a>
### Pattern 9

    Input: N = 5
    Result:   

        *
       * *
      * * * 
     * * * *
    * * * * *
    * * * * *
     * * * *
      * * * 
       * *    
        *

```java
class Solution {

    void printDiamond(int N) {
        // Your code here
        
        // Upper pyramid
        
        for (int i = 1; i <= N; i++) {
            for (int j = N; j > i; j--) {
                System.out.print(' ');
            }
            for (int j = 0; j < i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
        
        // Lower pyramid
        
         for (int i = 1; i <= N; i++) {
            for (int j = 1; j < i; j++) {
                System.out.print(' ');
            }
            for (int j = N; j >= i; j--) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-10"></a>
### Pattern 10

    Input: 5

    Output:

    * 
    * * 
    * * * 
    * * * * 
    * * * * *
    * * * *
    * * *
    * *
    * 


```java
class Solution {

    void printTriangle(int N) {
        // code here

        // Upper Triangle 
        for (int i = 1; i <= N; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
        
        // Lower Triangle
        for (int i = N - 1; i > 0; i--) {
            for (int j = i; j > 0; j--) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-11"></a>
### Pattern 11

    Input: 5

    Output:

    1 
    0 1 
    1 0 1
    0 1 0 1 
    1 0 1 0 1

```java
class Solution {

    void printTriangle(int N) {
        
        for (int i = 1; i <= N; i++) {
            boolean flag = (i % 2 == 1) ? true : false;
            for (int j = 1; j <= i; j++) {
                if (flag == true) System.out.print("1 ");
                else System.out.print("0 ");
                flag = !flag;
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-12"></a>
### Pattern 12

    Input: 5

    Output:

    1                 1
    1 2             2 1
    1 2 3         3 2 1
    1 2 3 4     4 3 2 1
    1 2 3 4 5 5 4 3 2 1

```java
class Solution {

    void printTriangle(int N) {
        // code here
        for (int i = 1; i <= N; i++) {
            
            // Number before spaces
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            
            //Spaces
            int spaces = (N - i) * 2;
            for (int j = 1; j <= spaces; j++) {
                System.out.print("  ");
            }
            
            //Numbers after spaces
            for(int j = i; j > 0; j--) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```


<a id="pattern-13"></a>
### Pattern 13

    Input: 5

    Output:

    1 
    2 3 
    4 5 6 
    7 8 9 10 
    11 12 13 14 15

```java
class Solution {

    void printTriangle(int N) {
        int count = 1;
        
        for (int i = 1; i <= N; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(count++ + " ");
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-14"></a>
### Pattern 14

    Input: 5

    Output:

    A
    AB
    ABC
    ABCD
    ABCDE

```java
class Solution {

    void printTriangle(int N) {
        // code here
        for (int i = 0; i < N; i++) {   
            for (char ch = 'A'; ch <= 'A' + i; ch++) {
                System.out.print(ch);
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-15"></a>
### Pattern 15

    Input: 5

    Output:

    ABCDE
    ABCD
    ABC
    AB
    A

```java
class Solution {

    void printTriangle(int N) {
        // code here
        for (int i = N; i > 0; i--) {
            for (char ch = 'A'; ch < 'A' + i; ch++) {
                System.out.print(ch);
            }
            System.out.println();
        }
    }
}
```


<a id="pattern-16"></a>
### Pattern 16

    Input: 5

    Output:
    A
    BB
    CCC
    DDDD
    EEEEE

```java
class Solution {

    void printTriangle(int N) {
        // code here
        char ch = 'A';
        for (int i = 1; i <= N; i++)  {
            // we can also do something like char ch = 'A' + i here
            for (int j = 1; j <= i; j++) {
                System.out.print(ch);
            }
            ch++;
            System.out.println();
        }
    }
}
```

<a id="pattern-17"></a>
### Pattern 17

    Input: 4

    Output:

       A
      ABA
     ABCBA
    ABCDCBA

```java
class Solution {

    void printTriangle(int N) {
        // code here
        for (int i = 1; i <= N; i++) {
            for (int j = 1; j <= N - i; j++) {
                System.out.print(' ');
            }
            
            char ch = 'A';
            
            // With 2 loops
            // for(int j = 1; j <= i; j++) {
            //     System.out.print(ch++);
            // }
            
            // ch -= 2;
            
            // for (int j = 1; j < i; j++) {
            //     System.out.print(ch--);
            // }
            
            // With 1 loop
            int printReverse = (i * 2) / 2;
            for(int j = 1; j <= i * 2 - 1; j++) {
                System.out.print(ch);
                if(j < printReverse) ch++;
                else ch--;
            }
            
            System.out.println();
        }
    }
}
```

<a id="pattern-18"></a>
### Pattern 18

    Input: 5

    Output:

    E
    E D
    E D C
    E D C B
    E D C B A

```java
class Solution {

    void printTriangle(int N) {
        // code here
        for (int i = 1; i <= N; i++) {
            char ch = (char)((int)('A' + N - 1));
            
            for (int j = 1; j <= i; j++) {
                System.out.print(ch-- + " ");
            }
            System.out.println();
        }
    }
}
```

<a id="pattern-19"></a>
### Pattern 19

    Input: 5

    Output:

    **********
    ****  ****
    ***    ***
    **      **
    *        *
    *        *
    **      **
    ***    ***
    ****  ****
    **********

```java
class Solution {

    void printTriangle(int N) {
        // code here
        
        /* 
            divide the pattern into 2 parts
                - Upper part
                - Lower part
                
            Upper and Lower parts can be divided into 3 parts
                - Stars before spacing
                - Spacing (can be calculated from i. Consider 0 indexing, if i = 0 -> space = 0, i = i -> space = 2, i = N -> space = i * 2 )
                - Stars after spacing
        */
        
        // Upper pattern
        
        for (int i = 1; i <= N; i++) {
            for (int j = 1; j <= N - i + 1; j++) {
                System.out.print('*');
            }
            
            int spaces = (i - 1) * 2;
            for (int j = 1; j <= spaces; j++) {
                System.out.print(" ");
            }
            
            for (int j = 1; j <= N - i + 1; j++) {
                System.out.print('*');
            }
            System.out.println();
        }
        
        // Lower Pattern
        for (int i = N; i >= 1; i--) {
            for (int j = 1; j <= N - i + 1; j++) {
                System.out.print('*');
            }
            
            int spaces = (i - 1) * 2;
            for (int j = 1; j <= spaces; j++) {
                System.out.print(" ");
            }
            
            for (int j = 1; j <= N - i + 1; j++) {
                System.out.print('*');
            }
            System.out.println();    
        }
    }
```

<a id="pattern-20"></a>
### Pattern 20

    Input: 5

    Output:

    *        *
    **      **
    ***    ***
    ****  ****
    **********
    ****  ****
    ***    ***
    **      **
    *        *

```java
class Solution {

    void printTriangle(int N) {
        /* 
            divide the pattern into 2 parts
                - Upper part
                - Lower part
                
            Upper and Lower parts can be divided into 3 parts
                - Stars before spacing
                - Spacing
                - Stars after spacing
        */
        
        // Upper pattern
        for (int i = 1; i <= N; i++) {
            // Stars before spacing
            for(int j = 1; j <= i; j++) System.out.print('*');
            
            // Spacing
            int spaces = (N - i) * 2;
            for (int j = 1; j <= spaces; j++) System.out.print(" ");
            
            // Stars after spacing
            for (int j = 1; j <= i; j++) System.out.print('*');
            System.out.println();
        }
        
        // Lower pattern
        for (int i = N - 1; i > 0; i--) {
            // Stars before spacing
            for(int j = 1; j <= i; j++) System.out.print('*');
            
            // Spacing
            int spaces = (N - i) * 2;
            for (int j = 1; j <= spaces; j++) System.out.print(" ");
            
            // Stars after spacing
            for (int j = 1; j <= i; j++) System.out.print('*');
            System.out.println();
        }
    }
}
```

<a id="pattern-21"></a>
### Pattern 21

    Input: 5

    Output:

    *****
    *   *
    *   *
    *   *
    *****

```java
class Solution {

    void printSquare(int N) {
        // code here
        for (int i = 1; i <= N; i++) {
            for (int j = 1; j <= N; j++) {
                if (i == 1 || i == N || j == 1 || j == N) System.out.print("*");
                else System.out.print(' ');
            }
            System.out.println();
        }
    }
}
```


<a id="pattern-22"></a>
### Pattern 22

    Input: 4

    Output:

    4 4 4 4 4 4 4
    4 3 3 3 3 3 4
    4 3 2 2 2 3 4
    4 3 2 1 2 3 4
    4 3 2 2 2 3 4
    4 3 3 3 3 3 4
    4 4 4 4 4 4 4

```java
class Solution {

    void printSquare(int N) {
        // code here
        
        for (int i = 1; i < N * 2; i++) {
            for (int j = 1; j < N * 2; j++) {
                
                // Find minimum distance from all sides and subtract it by N
                int top = i;
                int bottom = 2 * N - i;
                int left = j;
                int right = 2 * N - j;
                
                int number = N + 1 - Math.min(Math.min(top, bottom), Math.min(left, right));
                System.out.print(number + " ");
            }
            System.out.println();
        }
    }
}
```
