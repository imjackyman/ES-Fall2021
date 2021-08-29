# 嵌入式系統與實習

## 1-1 在TinkerCAD開一個新的Circuit, 加上一個外部的LED, 並且ON (亮) 1秒, OFF(滅) 1秒 
### 說明：

> 第13腳位的外部為LED與內部LED,1秒亮,另1秒暗

### 電路圖：
> ![image](https://user-images.githubusercontent.com/31268069/130342065-be43918a-33bf-4df8-b9ad-ff601897e91e.png)

### 程式：
> ```c++
> // C++ code
> //
> void setup()
> {
>   pinMode(13, OUTPUT);
> }
> 
> void loop()
> {
>   digitalWrite(13, HIGH);
>   delay(1000); // Wait for 1000 millisecond(s)
>   digitalWrite(13, LOW);
>   delay(1000); // Wait for 1000 millisecond(s)
> }
 ```

## 1-2 在TinkerCAD開一個新的Circuit, 分別使甪R, G, B三種顏色的LED, ON (亮) 0.5秒, OFF(滅) 0.5秒
### 說明：

> 待補

### 電路圖：
> 待補

### 程式：
> ```c++
> // C++ code
> //
> void setup()
> {
>   pinMode(13, OUTPUT);
> }
> 
> void loop()
> {
>   digitalWrite(13, HIGH);
>   delay(1000); // Wait for 1000 millisecond(s)
>   digitalWrite(13, LOW);
>   delay(1000); // Wait for 1000 millisecond(s)
> }
> ```
