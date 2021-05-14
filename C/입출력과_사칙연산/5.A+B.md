# 5번 문제 풀이
![install](https://user-images.githubusercontent.com/81015704/118220636-1ccace00-b4b7-11eb-8f16-15e3c2eda108.png)

### 내 답
<pre><code>
#define _CRT_SECURE_NO_WARNINGS
#include stdio.h

int main() {
    int a, b;
    scanf("%d %d", &a, &b); //&<-주소로 보내줌
    printf("%d", a + b);
    return 0;
}
</code></pre>


#### 느낀점(배운점)
입력 : scanf ("받는 형식",&변수)//변수의 주소로 보냄
받아서 더해줌.
