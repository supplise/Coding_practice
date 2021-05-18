멀티 플렉서(MUX라고도 불림)
1. 2^n 입력중에서 하나의 2진 정보를 선택하여 단일 출력선으로 연결하는 회로
2. 2^n의 입력선과 n개의 선택선 그리고 한개의 출력선으로 구성됨
<br>
선택선에 따라 D0D1D2D3로 출력하는 형식
<br>

### 진리표<br>
 ![2](https://user-images.githubusercontent.com/81015704/118645212-9c3f0100-b819-11eb-9014-6633c6ed6917.jpg)<br>
### 블럭도<br>
![1](https://user-images.githubusercontent.com/81015704/118645201-9b0dd400-b819-11eb-9f7c-b532365b081e.jpg)<br>
### 논리회로도<br>
![3](https://user-images.githubusercontent.com/81015704/118645213-9c3f0100-b819-11eb-99bd-8b19c341b9fc.jpg)<br>
### 예제풀이<br>
![123](https://user-images.githubusercontent.com/81015704/118645538-03f54c00-b81a-11eb-943f-c45350abc1bb.jpg)
### 진리표
![123455](https://user-images.githubusercontent.com/81015704/118645549-08216980-b81a-11eb-8ece-2732be47de61.jpg)
<br>
#### A가 입력선일경우(자동으로 B와C는 선택선)일때
<br>
설명:옆에 보면 B와C가 겹치는 부분이 있다 그부분에서 반복되기전까지 옆으로 출력하다가 반복되면 아래로 내려준다.
<br>
![a](https://user-images.githubusercontent.com/81015704/118646104-b88f6d80-b81a-11eb-92d5-75bc7d2d6fae.jpg)
![a블록도](https://user-images.githubusercontent.com/81015704/118646112-baf1c780-b81a-11eb-8399-b85be28fa830.jpg)
<br>
#### B가 입력선일경우(자동으로 A와C는 선택선)일때
<br>
설명:위에 나온것처럼 00,01,다음 00,01이 나오므로 00,01에서 반복되는부분이나오니 아래로내려준다그후 10,11부분에선 다시 위에 적어주고 2번째10,11에서 내려준다
<br>
![b](https://user-images.githubusercontent.com/81015704/118646489-394e6980-b81b-11eb-8706-3fe20d78f94b.jpg)
![ㅠ블록도](https://user-images.githubusercontent.com/81015704/118646501-3d7a8700-b81b-11eb-93ac-5fbde2142997.jpg)

<br>
#### C가 입력선일경우(자동으로 A와B는 선택선)일때
<br>
설명:00,00처럼 바로바로 나오므로 한칸씩만차지하고 바로 내려짐

<br>
![c](https://user-images.githubusercontent.com/81015704/118646540-479c8580-b81b-11eb-987f-212483157da2.jpg)
![c블록도](https://user-images.githubusercontent.com/81015704/118646544-48351c00-b81b-11eb-8199-ab8506765547.jpg)


