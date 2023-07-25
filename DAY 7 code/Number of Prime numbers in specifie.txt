Number of Prime numbers in specified range.

import java.io.*; 
import java.util.*;
class UserMainCode{     
  public int countPrimesInRange(int input1, int input2){      
 
  int count = 0;

        for (int num = input1; num <= input2; num++) {
            if (isPrime(num)) {
                count++;
            }
        }

        return count;
    }

    public static boolean isPrime(int number) {
        if (number <= 1) {
            return false;
        }

        for (int i = 2; i <= Math.sqrt(number); i++) {
            if (number % i == 0) {
                return false;
            }
        }

        return true;
    }
}

