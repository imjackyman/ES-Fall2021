# 嵌入式系統與實習

## 2-1 analogWrite(): 並且觀查LED亮度變化是否有像"呼吸的效果"和示波器的波形有什麼關連性?

### 電路圖：
> ![test1](https://user-images.githubusercontent.com/31268069/132115079-7816d953-140b-4f84-aa95-9427b47de9dd.gif)

### 程式：
> ```c++
> void setup()
> {
>   pinMode(LED_BUILTIN, OUTPUT);
> }
> 
> void loop()
> {
>   digitalWrite(LED_BUILTIN, HIGH);
>   delay(30); 
>   digitalWrite(LED_BUILTIN, LOW);
>   delay(30); 
>   
>   digitalWrite(LED_BUILTIN, HIGH);
>   delay(60); 
>   digitalWrite(LED_BUILTIN, LOW);
>   delay(60);
>   
>   digitalWrite(LED_BUILTIN, HIGH);
>   delay(90);
>   digitalWrite(LED_BUILTIN, LOW);
>   delay(90); 
> }
> ```



## 2-2, RGB LED燈全彩模組, 分別讓LED輪流表現正紅、正綠、正藍，三個顏色，時間間隔1秒鐘。並且觀查LED顏色和波形或是電壓有什麼關連性

### 電路圖：
> ![test2](https://user-images.githubusercontent.com/31268069/132115082-819007ea-5e67-49a0-a76f-4ff99fec2c43.gif)

### 程式：
> ```c++
>int R = 11;
>int G = 9;
>int B = 10;
>
>void setup()
>{
>  pinMode(R, OUTPUT);
>  pinMode(G, OUTPUT);
>  pinMode(B, OUTPUT);  
>}
>
>void loop()
>{
>	analogWrite(R, 255);
>	analogWrite(G, 0);
>	analogWrite(B, 0);
>  	delay(1000);
>	analogWrite(R, 0);
>	analogWrite(G, 255);
>	analogWrite(B, 0);
>  	delay(1000);
>	analogWrite(R, 0);
>	analogWrite(G, 0);
>	analogWrite(B, 255);
>  	delay(1000);  
>}
> ```

## 2-3, 讓你的RGB LED燈全彩模組也可會"呼吸", LED顏色變化是否有像"呼吸的效果"和示波器的波形有什麼關連性? (

### 電路圖：
> ![lab3](https://user-images.githubusercontent.com/31268069/132971088-573ba7b4-7c84-4bae-988c-de328ad67ae3.gif)

### 程式：
> ```c++
> int brightness = 0;
> int Red = 9;
> int Green = 10;
> int Blue = 11;
> int number = 5;
> void setup()
> {
>   pinMode(Red, OUTPUT);
>   pinMode(Green, OUTPUT);
>   pinMode(Blue, OUTPUT);
> }
> 
> void loop()
> {
> //Red
>   for ( brightness = 0 ; brightness <=255 ; brightness +=number){
>   	analogWrite(Red,brightness);
>     delay(50);
>   }
>   
>   for ( brightness = 255 ; brightness >=0 ; brightness -=number){
>   	analogWrite(Red,brightness);
>     delay(50);
>   }
>   delay(500);
> //Green
>   for ( brightness = 0 ; brightness <=255 ; brightness +=number){
>   	analogWrite(Green,brightness);
>     delay(50);
>   }
>   
>   for ( brightness = 255 ; brightness >=0 ; brightness -=number){
>   	analogWrite(Green,brightness);
>     delay(50);
>   }
>   delay(500);
> //Blue
>   for ( brightness = 0 ; brightness <=255 ; brightness +=number){
>     analogWrite(Blue,brightness);
>     delay(50);
>   }
> 
>   for ( brightness = 255 ; brightness >=0 ; brightness -=number){
>     analogWrite(Blue,brightness);
>     delay(50);
>   }
>   delay(500);
> }
> ```

