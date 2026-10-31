# PC-1-Hackerrank-Primality-_IT24030
<img width="752" height="211" alt="Prime checker" src="https://github.com/user-attachments/assets/a039e1f9-b145-42eb-b072-6391456e3bb5" />
<img width="743" height="261" alt="Java_priliminaryTest" src="https://github.com/user-attachments/assets/b896b76b-ccaa-412c-8afa-e7e1d4f65a78" />

Prime_Checker
import java.io.*;
import java.util.*;
import static java.lang.System.in;

class Prime {

    public void checkPrime(int... nums) {
        String result = "";

        for (int num : nums) {
            if (isPrime(num)) {
                result += num + " ";
            }
        }

        System.out.println(result);
    }

    private boolean isPrime(int n) {
        if (n < 2) {
            return false;
        }
        for (int i = 2; i * i <= n; i++) {
            if (n % i == 0) {
                return false;
            }
        }
        return true;
    }
}

public class Solution {

    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(in));
            int n1 = Integer.parseInt(br.readLine());
            int n2 = Integer.parseInt(br.readLine());
            int n3 = Integer.parseInt(br.readLine());
            int n4 = Integer.parseInt(br.readLine());
            int n5 = Integer.parseInt(br.readLine());

            Prime ob = new Prime();
            ob.checkPrime(n1);
            ob.checkPrime(n1, n2);
            ob.checkPrime(n1, n2, n3);
            ob.checkPrime(n1, n2, n3, n4, n5);
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}



