# 대주제
문제 1. ㅁㅁㅁㅁㅁㅁ 하세요.
```java
package day07.homework;

import java.util.Scanner;

/*
1. UP & DOWN
     1) 컴퓨터는 1 ~ 100 중 랜덤한 1개의 숫자를 정한다.
     2) 사용자가 정수를 입력한다.
     3) 정답 > 입력 인 경우 UP 출력
        정답 < 입력 인 경우 DOWN 출력
        정답 == 입력 인 경우 CORRECT! 출력한다.
     4) 사용자가 정답을 입력할 때까지 2 ~ 3 과정을 반복한다.
     (+5) 총 몇 회 소요되었는 지 시도 횟수를 출력한다.)
     (+6) 시도 횟수가 8회 미만인 경우 WIN 을 출력, 아닌 경우 LOSE 출력)

 */
public class Homework02 {
	public static void main(String[] args) {
		
		// 정답 
		int correct = (int)(Math.random() * 100) + 1;
		
		
		// 사용자 답
		Scanner sc = new Scanner(System.in); 
		int answer;
		
		
		// 시도 횟수 
		int count = 0;
		
		while(true) {
			
			++count; // 시도 횟수 1 증가 
			
			System.out.print("답 : ");
			answer = sc.nextInt();
			
			if(correct > answer) {
				System.out.println("UP!");
			}
			else if(correct < answer) {
				System.out.println("DOWN!");
			}
			else {
				System.out.println("CORRECT!");
				break; // 반복 종료
			}
		}
		sc.close();
		System.out.println("총 " + count + "시도");
		System.out.println(count < 8 ? "WIN!" : "LOSE..");
	}
}
```


## 중주제
##### 소소소소주제
