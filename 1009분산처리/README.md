# 분산 처리
<img width="1151" alt="Screenshot 2023-05-07 at 10 40 30 PM" src="https://user-images.githubusercontent.com/83897840/236680990-a0c703ab-6830-4a3a-b5e7-ef285c965b66.png">
<img width="1217" alt="Screenshot 2023-05-07 at 10 40 45 PM" src="https://user-images.githubusercontent.com/83897840/236681008-51346317-68d7-4f7c-8f7c-5c732bf563ab.png">

````
import java.io.*;
import java.math.BigInteger;
import java.util.*;
public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int t = Integer.parseInt(br.readLine());
        StringBuilder sb = new StringBuilder();
        for (int i = 0; i < t; i++) {
            StringTokenizer st = new StringTokenizer(br.readLine());
            int a = Integer.parseInt(st.nextToken());
            int b = Integer.parseInt(st.nextToken());
            if (a % 10 == 0) {
                sb.append(10 + "\n");
                continue;
            }
            int num = a % 10;
            for (int j = 1; j < b; j++) {
                num = (num * a) % 10;
            }
            sb.append(num + "\n");
        }
        System.out.print(sb);
    }
}
````
