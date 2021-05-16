# 3번 문제 풀이
![install](https://user-images.githubusercontent.com/81015704/118400229-b8b52f00-b69b-11eb-8ba8-ae8fd7e538fe.png)
![install](https://user-images.githubusercontent.com/81015704/118400234-b9e65c00-b69b-11eb-9910-5d896e0a4237.png)
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
글이 많아서 이해 못했습니다 ..걍 횟수 정하고 a+b값만 나오게 했어요!
