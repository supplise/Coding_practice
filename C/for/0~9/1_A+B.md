# 2번 문제 풀이
![install](https://user-images.githubusercontent.com/81015704/118363762-f5682400-b5d0-11eb-9246-99535566a1cc.png)

### 내 답
<pre><code>
#define _CRT_SECURE_NO_WARNINGS
#include stdio.h

int main(void) {
	int count,a,b;
	scanf("%d", &count);
	for (int i = 1; i <= count; i++) {
		scanf("%d %d", &a, &b);
		printf("%d\n", a + b);
	}
}
</code></pre>


#### 느낀점(배운점)
처음 값을 반복하는 양으로 잡고안에서 계속 받아a+b 값을 출력
