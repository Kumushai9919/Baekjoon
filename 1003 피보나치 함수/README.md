# 1003 피보나치 함수 

<img width="1219" alt="Screenshot 2023-04-09 at 11 38 03 PM" src="https://user-images.githubusercontent.com/83897840/230779130-e9cbf9f4-3f80-4ec7-a53d-34df38f339e7.png">
<img width="1211" alt="Screenshot 2023-04-09 at 11 39 00 PM" src="https://user-images.githubusercontent.com/83897840/230779193-fe11a22f-fb0c-47e5-806f-cc3bc35fc832.png">



#### 자바로 풀이
````
 import java.util.Scanner;
 
public class Main {
 
	static Integer[][] dp = new Integer[41][2];
	
	public static void main(String[] args) {
		Scanner in = new Scanner(System.in);
		
		dp[0][0] = 1;	 
		dp[0][1] = 0;	 
		dp[1][0] = 0;	 
		dp[1][1] = 1;	 
		
		int T = in.nextInt();
        
		while(T-- > 0){
			int N = in.nextInt();
			fibonacci(N);
			System.out.println(dp[N][0] + " " + dp[N][1]);
		}
		
	}
	
	static Integer[] fibonacci(int N) {
		 
		if(dp[N][0] == null || dp[N][1] == null) {
			 
			dp[N][0] = fibonacci(N - 1)[0] + fibonacci(N - 2)[0];
			dp[N][1] = fibonacci(N - 1)[1] + fibonacci(N - 2)[1];
		}
		 
		return dp[N];
 
	}
 
}
````
