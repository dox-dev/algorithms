# Primality Test

### Task:
Given a positive integer, examine whether the number is prime or not.

### Explanation:
Any number in order to be prime, has to follow these rules:<br>
<sub>&bull; It must be greater than 2</sub><br>
<sub>&bull; It must be a positive integer</sub><br>
<sub>&bull; It has no divisors other than 1 and the number itself</sub><br>

### Solution:
We want our algorithm to be as time efficient as possible. In order to achieve that, we could do this:<br>
We do is loop through every number from **2** to the square root of **N** (where n is the number we are currently checking).<br>
If we find any number that is a divisor of N, then we return **False**, otherwise, we return **True**.

**Time Complexity**: O(√N) <sub>[the algorithm requires O(N^(1/2)) evaluations where the size of input is N]

<br>

<details open>
    <summary><h3>Python</h3></summary>
     
    import math
      
    def isPrime(N):
    
      # we check if N is less than 2
      if N < 2:
       return False

     # we loop through every number from 2 to square root of N
     for d in range(2, int(math.sqrt(N)) + 1):
     
       # if we find a divisor (d) of N we return False
       if N % d == 0:
         return False

     # otherwise we return True
     return True
</details>
<details>
    <summary><h3>C</h3></summary>
     
    #include <math.h>

    int isPrime(int N) {
    
      // we check if N is less than 2
      if (N < 2) {
        return 0;
      }
    
      // we loop through every number from 2 to square root of N
      for (int d = 2; d < (int) sqrt(N) + 1; d++) {
        
        // if we find a divisor (d) of N we return False
        if (N % d == 0) {
          return 0;
        }
      }
    
      // otherwise we return True
      return 1;
    }
</details>
<details>
    <summary><h3>C++</h3></summary>
     
    #include <math.h>

    bool isPrime(int N) {
      if (N < 2) {
        return false;
      }

      // we loop through every number from 2 to square root of N
      for (int d = 2; d < (int) sqrt(N) + 1; d++) {
    
        // if we find a divisor (d) of N we return False
        if (N % d == 0) {
          return false;
        }
       }

      // otherwise we return True
      return true;
    }
</details>
