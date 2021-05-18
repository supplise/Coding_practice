# 5번 문제 풀이
![1](https://user-images.githubusercontent.com/81015704/118668439-d5826b80-b82f-11eb-9099-1fce82c06916.jpg)
![2](https://user-images.githubusercontent.com/81015704/118668445-d61b0200-b82f-11eb-9b92-d712d2db4386.jpg)


### 내 답
<pre><code>
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

int main(void) {
	int a,count,total;
	char t[100];
  //1번
	scanf("%d", &a);
	for (int i = 0; i < a; i++) {
  //2번
		count = 0;
		total = 0;
   //3번
		scanf("%s", t);
		for (int j = 0; t[j] != '\0'; j++) {
    //4번
			if (t[j] == 'O') {
				count ++;
			}
			else {
				count = 0;
			}
     //5번
            total += count;
		}
    //6
		printf("%d\n", total);
	}
}
</code></pre>


#### 느낀점(배운점)
1. 횟수 값을 받는다.
2. count와 total을 계속적으로 초기화 해준다.
3. 문자를 받아 배열에 넣는다 이때 \0(마지막에 이렇게 넣어짐)이 아닐경우 반복 되도록 만든다.
4. 그후 조건으로 O면 count가 올라가고 아니면 count가 0이 되게 해준다
5. 그후 total에 계속 count를 더해준다.
6. 마지막 total을 중간중간 출력한다.
