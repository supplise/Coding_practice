![image](https://user-images.githubusercontent.com/81015704/123546397-4f930200-d797-11eb-93c6-167b01f51895.png)

<code><pre>
void setup()
{
  for(int x=2;x<14;x++){
   pinMode(x,OUTPUT);
  }
  for(int x=14;x<18;x++){
   pinMode(x,INPUT);
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
void F1(){digitalWrite(10, LOW);digitalWrite(11, HIGH);digitalWrite(12, HIGH);digitalWrite(13, HIGH);}
void F2(){digitalWrite(11, LOW);digitalWrite(10, HIGH);digitalWrite(12, HIGH);digitalWrite(13, HIGH);}
void F3(){digitalWrite(12, LOW);digitalWrite(13, HIGH);digitalWrite(11, HIGH);digitalWrite(10, HIGH);}
void F4(){digitalWrite(13, LOW);digitalWrite(12, HIGH);digitalWrite(11, HIGH);digitalWrite(10, HIGH);}
int N=0;
int mon=0;
int DATE=1;
int day[12]={31,28,31,30,31,30,31,31,30,31,30,31};
void Plus_minus(){
  for(int x=0;x<30;x++){
    F4();
  	disp(int(N/1000)%10);
  	delay(1);
  	CLS();
    F3();
  	disp(int(N/100)%10);
  	delay(1);
  	CLS();
	F2();
  	disp(int(N/10)%10);
  	delay(1);
  	CLS();
  	F1();
  	disp(N%10);
  	delay(1);
  	CLS();
  } 
}
void calendar(int i,int j){
      for(int x=0;x<30;x++){
    	F4();
  		disp(int((i+1)/10)%10);
  		delay(1);
  		CLS();
    	F3();
  		disp((i+1)%10);
  		delay(1);
  		CLS();
		F2();
  		disp(int(j/10)%10);
  		delay(1);
  		CLS();
  		F1();
  		disp(j%10);
  		delay(1);
  		CLS();
    }
}
void time(){
    for(int x=0;x<30;x++){
    F4();
  	disp(int(N/(60*10))%3);
  	delay(1);
  	CLS();
    F3();
  	disp(int(N/(60))%10);
  	delay(2);
  	CLS();
	F2();
  	disp(int(N/10)%6);
  	delay(2);
  	CLS();
  	F1();
  	disp(N%10);
  	delay(2);
  	CLS();
  }
}
int t=0;
void loop()
{ 
  if(t==0){
    Plus_minus();
  }else if(t==1){
   calendar(mon,DATE); 
  }else if(t==2){
   time(); 
  }
  if(digitalRead(14)==HIGH){
   t=0;
   N++;
  }
  if(digitalRead(15)==HIGH){
   t=0;
   if(N==0){N=9999;Plus_minus();}else{N--;Plus_minus();} 
  }
  if(digitalRead(16)==HIGH){
    t=1;
    if(DATE==day[mon]&&mon!=11){mon+=1;DATE=1;calendar(mon,DATE);}else if(DATE==day[mon]&&mon==11){mon=0;DATE=1;}else{DATE+=1;calendar(mon,DATE);}
  }
  if(digitalRead(17)==HIGH){
  	t=2;
  	if(N>=24*60-1){N=0;time();}else{N++;time();}
  }
}
</pre></code>


## 설명
0~9999까지 카운트<br>
9999~0까지 카운트<br>
달력식 카운트<br>
시간 카운트

