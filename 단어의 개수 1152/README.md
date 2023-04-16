# 단어의 개수 1152

<img width="1252" alt="Screenshot 2023-04-16 at 9 26 30 PM" src="https://user-images.githubusercontent.com/83897840/232309845-c09602b3-a580-4e78-a9db-e4935db0d6f5.png">


#### 자바 풀이 방법:

````
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
        String words;
        int count = 0;

        words = input.nextLine();

        for(int i = 0; i < words.length(); i ++){
             if(words.charAt(i) == ' '){
                count++;
            }
           
        }
        
        if(words.charAt(0) != ' ' && words.charAt(words.length()-1) != ' '){  
            count = count + 1; 
        }
        if(words.charAt(0) == ' ' && words.charAt(words.length()-1) == ' '){  
            count = count - 1;
        }

        System.out.print(count);
        
    }
}

    
````
