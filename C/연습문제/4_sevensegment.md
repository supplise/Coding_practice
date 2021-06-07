### 회로
![image](https://user-images.githubusercontent.com/81015704/121031488-57d5ce00-c7e5-11eb-8fd2-ab284be5a26d.png)

### 내코드
<pre><code>
int N=0;
void setup()
{
  for(int x=2;x<14;x++){
   pinMode(x,OUTPUT); 
  }
}
void CLS() {  for(int X=2; X<9; X++) {  digitalWrite(X, LOW); } }
void disp(int N) {
   switch (N) {
      case 1 :digitalWrite(3, HIGH); digitalWrite(4, HIGH); break;
      case 2 :digitalWrite(2, HIGH); digitalWrite(3, HIGH); digitalWrite(5, HIGH); digitalWrite(6, HIGH); digitalWrite(8, HIGH); break;
      case 3 :digitalWrite(2, HIGH); digitalWrite(3, HIGH); digitalWrite(4, HIGH); digitalWrite(5, HIGH); digitalWrite(8, HIGH); break;
      case 4 :digitalWrite(3, HIGH); digitalWrite(4, HIGH); digitalWrite(7, HIGH); digitalWrite(8, HIGH); break;
      case 5 :digitalWrite(2, HIGH); digitalWrite(4, HIGH); digitalWrite(5, HIGH); digitalWrite(7, HIGH); digitalWrite(8, HIGH); break;
      case 6 :digitalWrite(2, HIGH); digitalWrite(4, HIGH); digitalWrite(5, HIGH); digitalWrite(6, HIGH); digitalWrite(7, HIGH); digitalWrite(8, HIGH); break;
      case 7 :digitalWrite(2, HIGH); digitalWrite(3, HIGH); digitalWrite(4, HIGH); break;
      case 8 :digitalWrite(2, HIGH); digitalWrite(3, HIGH); digitalWrite(4, HIGH); digitalWrite(5, HIGH); digitalWrite(6, HIGH); digitalWrite(7, HIGH); digitalWrite(8, HIGH); break;
      case 9 :digitalWrite(2, HIGH); digitalWrite(3, HIGH); digitalWrite(4, HIGH); digitalWrite(5, HIGH); digitalWrite(7, HIGH); digitalWrite(8, HIGH); break;
      case 0 :digitalWrite(2, HIGH); digitalWrite(3, HIGH); digitalWrite(4, HIGH); digitalWrite(5, HIGH); digitalWrite(6, HIGH); digitalWrite(7, HIGH); break;
   } 
}
void F1(){digitalWrite(12, HIGH);digitalWrite(13, LOW);}
void F2(){digitalWrite(12, LOW);digitalWrite(13, HIGH);}
void loop()
{
N++;
   for (int R = 0; R <= 30; R++) {  // 반복 표시, 
     F1();
     disp(int(N / 10) % 10);
     delay(1);
     CLS();
     F2();
	 disp(N % 10);
     delay(2);
     CLS();
   }
}
</code></pre>
