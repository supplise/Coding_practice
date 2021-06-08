# 2번 문제 풀이
![image](https://user-images.githubusercontent.com/81015704/121201616-9e8ffa80-c8af-11eb-991c-269e9e1ecb45.png)
![image](https://user-images.githubusercontent.com/81015704/121201647-a51e7200-c8af-11eb-83bd-8fe957ae4386.png)

### 내 답
<pre><code>
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

int main(void) {
	int a, b, c[10000] = { 0 },t=0,i;
	scanf("%d %d", &a, &b);
	//값넣어주기
	for (i = 0; i < a; i++) {
		scanf("%d",&c[i]);
	}
	for (i=0;i<a;i++) {
		if (t > 1) {
			break;
		}
		for (int j = 0; j < a; j++) {
			if (i == j) {
				continue;
			}
			for (int k = 0; k < a; k++) {
				if (i == k || j == k) {
					continue;
				}
				if (b - c[i] == c[k] + c[j]) {
					t=c[i]+c[j]+c[k];
					break;
				}
				if (i == a - 1 && j == a - 2 && k == a-3 && b - c[i] != c[k] + c[j])
				{
					i = -1;
					b -= 1;
				}
			}
		}
	}
	printf("%d", t);
}
</code></pre>


#### 느낀점(배운점)
//일단 무엇인지 찾아보질 못해서 .. 나오는 식만 만들어서 해보았습니다 ..(시간초과가 나오네요)
1.값을 배열안에 받는 부분을 만들어줍니다.<br>
2.3장이여서 반복문은 3중으로 만들었습니다(이거때문에 시간적 손해가 ...)
3.트리거를 걸어서 만약에 t안에 값이 들어가면 (어처피 합이라 1이상입니다) break가 걸립니다<br>
4.같은 값이 나올경우는 컨티뉴로 넘겨줍니다<br>
5.그리고 만약 i가 갈 수 있는 최대 j가 갈 수 있는 최대 k가 갈 수 있는 최대가 되면 i가 -1(++되기에)으로 되고 b를 -1을 해주게 만들었습니다.<br>
수정 예정입니다 ...
