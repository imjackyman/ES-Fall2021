# 嵌入式系統與實習

## 1-1 在TinkerCAD開一個新的Circuit, 加上一個外部的LED, 並且ON (亮) 1秒, OFF(滅) 1秒 

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



## 1-2 在TinkerCAD開一個新的Circuit, 分別使甪R, G, B三種顏色的LED, ON (亮) 0.5秒, OFF(滅) 0.5秒

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
