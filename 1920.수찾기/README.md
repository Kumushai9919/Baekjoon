# 수 찾기
<img width="1145" alt="Screenshot 2023-05-14 at 10 19 39 PM" src="https://github.com/Kumushai9919/Baekjoon/assets/83897840/60b021bc-5b17-4627-84eb-9b06c9c52e94">





##### 자바 해결 코드:
````
import java.util.Arrays;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] a = new int[n];
        for (int i = 0; i < n; i++) {
            a[i] = sc.nextInt();
        }
        Arrays.sort(a);

        int m = sc.nextInt();

        for (int i = 0; i < m; i++) {
            int answer = 0;
            int start = 0, end = n - 1;
            int x = sc.nextInt();
            while (start <= end) {
                int mid = (start + end) / 2;
                if (a[mid] == x) {
                    answer = 1;
                    break;
                }
                if (a[mid] > x) end = mid - 1;
                else start = mid + 1;
            }
            System.out.println(answer);
        }
    }
}
````
