# 嵌入式系統與實習
<dl>
  <dt>定義列表</dt>
  <dd><a href="https://www.google.com/" target="_blank" title="Wibibi 網頁設計教學百科">google</a></dd>

  <dt>在 HTML 中撰寫 Markdown</dt>
  <dd>*無法* 運作的 **非常** 好。改用 HTML<em>標籤</em>。</dd>
</dl>
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
