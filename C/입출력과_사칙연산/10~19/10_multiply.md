# 10번 문제 풀이
![install](https://user-images.githubusercontent.com/81015704/118239342-98874380-b4d4-11eb-9165-a4e98990fd0e.png)

### 내 답
<pre><code>
#define _CRT_SECURE_NO_WARNINGS
#include stdio.h

int main() {
	int a, b;
	scanf("%d %d", &a, &b);
	printf("%d\n", a * (b % 10));
	printf("%d\n", a * (b / 10-((b / 100)*10)));
	printf("%d\n", a * (b / 100));
	printf("%d", a * b);
}
</code></pre>


#### 느낀점(배운점)
1.처음값은 나머지b의 나머지를 곱해서 나오게 해준다.
2.b에 10%나눈 몫을 구한다(38)에서 앞에 10의자리부분은 100의자리이기에 빼줘야하고
이부분은 b를 100으로 나눈다음에(3)곱하기 10을 해주면 30이 되고 이것들을 빼주면 (8)이 남는다 이게 2째자리이다.
3. 백의자리로 몫을 구해준다.
4.곱하기
