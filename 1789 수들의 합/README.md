# 1789 수들의 합
<img width="1197" alt="Screenshot 2023-04-02 at 11 26 43 PM" src="https://user-images.githubusercontent.com/83897840/229359077-21ab1b48-bc7c-46eb-9be7-58afe05fcba5.png">

#### Solution:
````
import java.util.Scanner;

public class Main{
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		long N = sc.nextLong();
		long sum = 0;
		if (N == 1 | N == 2 ) {
			System.out.println(1);
			return;
		}
		for (int i = 0; i < N; i++) {
			sum += i;
			if (sum > N) {
				System.out.println(i-1);
				break;
			} else if (sum==N) {
				System.out.println(i);
				break;
			}
		}
	}
}
````
