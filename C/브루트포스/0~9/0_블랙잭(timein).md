# 0번 문제 풀이
![image](https://user-images.githubusercontent.com/81015704/121330205-c2574d00-c950-11eb-9cca-0315577ec444.png)
![image](https://user-images.githubusercontent.com/81015704/121330230-c7b49780-c950-11eb-967b-3a8f4c9a53e1.png)


### 내 답
<pre><code>
#define _CRT_SECURE_NO_WARNINGS
#include stdio.h

int main(void) {
	int a, b, c[10000], t, max = 0;
	scanf("%d %d", &a, &b);
	for (int i = 0; i < a; i++) {
		scanf("%d", &c[i]);
	}
	for (int i = 0; i < a; i++) {
		for (int j = i + 1; j<a ; j++) {
			for (int k = j + 1; k< a; k++) {
				t = c[i] + c[j] + c[k];
				if (t > max && t <= b) {
					max = t;
				}
			}
		}
	}
	printf("%d", max);
}
</code></pre>


#### 느낀점(배운점)
//지금까지 한거에서 i와 j에 1씩 더해주는 식으로 하면 겹치지 않는다는 점을 찾아냈습니다.<br>
1.위와 같이 겹치지 않게 하기위해 i j k에 각각 상위값에 +1 을 주도록 하였습니다.<br>
2.c[i]+c[j]+c[k]가 제일 크면서 b로 받은값과 같거나 작은값은 max안에 넣어준다.<br>
3.max를 출력해준다
