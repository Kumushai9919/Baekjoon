# 1181 단어 정렬

<img width="1207" alt="Screenshot 2023-04-23 at 12 17 37 PM" src="https://user-images.githubusercontent.com/83897840/233817826-7a3bd67a-4ab8-4c1b-b849-9f406ff7bcee.png">
<img width="1199" alt="Screenshot 2023-04-23 at 12 17 49 PM" src="https://user-images.githubusercontent.com/83897840/233817835-8efe3d55-71d1-46dc-9b9b-4627e51a671c.png">


````
import java.util.Scanner;
import java.util.Arrays;
import java.util.Comparator;
 
 
public class Main {
	public static void main(String[] args) {
    
		Scanner in = new Scanner(System.in);
 
		int N = in.nextInt();
		String[] arr = new String[N];
 
		in.nextLine();	 
 
		for (int i = 0; i < N; i++) {
			arr[i] = in.nextLine();
		}
		
		Arrays.sort(arr, new Comparator<String>() {
			public int compare(String s1, String s2) {
				 
				if (s1.length() == s2.length()) {
					return s1.compareTo(s2);
				} 
				 
				else {
					return s1.length() - s2.length();
				}
			}
		});
 
 
		System.out.println(arr[0]);
		
		for (int i = 1; i < N; i++) {
		 
			if (!arr[i].equals(arr[i - 1])) {
				System.out.println(arr[i]);
			}
		}
	}
 
}
````
