# 3번 문제 풀이
![image](https://user-images.githubusercontent.com/81015704/119504202-b8591a00-bda6-11eb-8792-102a50edb8bf.png)
![image](https://user-images.githubusercontent.com/81015704/119504249-c018be80-bda6-11eb-8506-351567927857.png)


### 내 답
<pre><code>
#define _CRT_SECURE_NO_WARNINGS
#include stdio.h
#include string.h

int main(void) {
	int count,h,w,n,t,r;
	scanf("%d\n", &count);
	for (int i = 0; i < count; i++) {
		scanf("%d %d %d", &h, &w, &n);
		if (n%h == 0) {
			t = h;
			r = n / h;
		}
		else {
			t = n % h;
			r = n / h + 1;
		}
		if (h * w >= n) {
			printf("%d%02d\n", t, r);
		}
	}
}
</code></pre>


#### 느낀점(배운점)
1.3개를 받는다. 처음줄은 나머지 값을 받는다 (층이 나와야 함으로) 이때 0이면 그냥 h값이 나오게 한다.<br>
2. 끝에는 몫이 나오게 해준다거기에 1을 더해주고 나머지가 0이면 더한 1을 없애준다.<br>
3. 곱하기 이상의 값이 안나오게 조건을 걸어주고 t와 r을해준다 이때(r에 02로 2자리가 나오게하고 처음은 0이나오게 해준다!)
