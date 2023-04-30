# 수열의 합

<img width="1245" alt="Screenshot 2023-04-30 at 11 22 39 PM" src="https://user-images.githubusercontent.com/83897840/235358213-4ab81e38-f165-47d3-96e8-61ba658a2b5e.png">


````
import java.util.Scanner;

public class Main {
	static int n,l;
	static int s,e;
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		
		n=sc.nextInt(); 
		l=sc.nextInt(); 
		int min=Integer.MAX_VALUE;
		int sum=0;
		int start=0;
		for (int i = 0; i <=n; i++) { 
				sum+=i;
				while(sum>n) {
					sum-=start;
					start+=1; 
				}
				if(sum==n && i-start+1>=l) { 
					if(min>i-start+1) { 
						s=start;
						e=i;
						min=i-start+1;
					}
                   
					if(i-start+1==1)break;
				}
		}
		 
		if(sum-s==n && (e-s+1)>l) { 
			s+=1;
		}
		
		if(e-s+1>100 || min==Integer.MAX_VALUE) { 
			System.out.println(-1);
		}else {
			for (int i = s; i <=e; i++) {
				System.out.print(i+" ");
			}
		}
}
		
	}
	
````
