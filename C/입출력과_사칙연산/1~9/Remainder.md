# 9번 문제 풀이
![install](https://user-images.githubusercontent.com/81015704/118237797-99b77100-b4d2-11eb-8e6e-3c6fe5370240.png)

### 내 답
<pre><code>
#define _CRT_SECURE_NO_WARNINGS
#include stdio.h

int main() {
	int a, b, c;
	scanf("%d %d %d", &a, &b, &c);
	printf("%d\n", (a + b) % c);
	printf("%d\n", ((a%c)+(b%c))%c);
	printf("%d\n", (a * b) % c);
	printf("%d", ((a % c) * (b % c)) % c);
}
</code></pre>


#### 느낀점(배운점)
(a+b)%c 와 ((a%c)+(b%c))%c 는같다.
<br>
(a * b) % c 와 ((a % c) * (b % c)) % c도 같다.
