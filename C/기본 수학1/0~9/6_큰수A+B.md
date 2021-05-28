# 6번 문제 풀이
![image](https://user-images.githubusercontent.com/81015704/119938809-ecf7ec00-bfc7-11eb-8b02-b2f3637b0282.png)

### 내 답
<pre><code>
#define _CRT_SECURE_NO_WARNINGS
#include stdio.h
#include string.h

int main(void) {
	int i, c[10000] = { 0, },t=0;
	char a[10000] = { 0, }, b[10000] = { 0, };
	scanf("%s %s", a, b);
	//b를 뒤집에서 c에 넣기
	for (i = 0; i < strlen(b); i++) {
		c[i] =b[strlen(b) - i-1]-48;
	}
	//c에 a포함시키기
	for (i = 0; i < strlen(a); i++) {
		c[i] +=a[strlen(a) - i - 1]-48;
	}
	if (strlen(b) >= strlen(a)) {t = strlen(b);}else {t = strlen(a);}
	//c횟수 구하기
	for (i = 0; i < t; i++) {
		if (c[i] / 10 > 0 && i != t - 1) {
			c[i + 1] += c[i] / 10;
			c[i] = c[i] % 10;
		}
	}
	//c출력
	for (i = t - 1; i >= 0; i--) {
		printf("%d", c[i]);
	}
}
</code></pre>


#### 느낀점(배운점)
//뒤에서 부터 더해줘야 한다고 생각합니다.<br>
1.b를 다른 c배열 안에 넣는다.<br>
2.c배열안에 a를 뒤부터 더해주는식으로 넣어줍니다.이때 A또는 B중 길이가 긴것의 길이를 t에 저장해 놓는다.(c의 길이가 된다)<br>
3.c[i]안에 값이 10이상이면 몫만큼을 다음값에 더해주고 나머지만 남겨준다(그리고 마지막은 나눠지지않게)<br>
4.그리고 1의 자리부터 되어있으니 t부터(c의 길이)-1만큼에서 0이 될때까지 쭉 출력해주면 된다.
