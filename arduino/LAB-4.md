# 嵌入式系統與實習

## 4-1 七段顯示器, LCD 顯示器 + 超音波感測器 (W7, W9) 

### 電路圖：
> ![LAB-4_1](https://user-images.githubusercontent.com/31268069/137610806-cb647f05-5665-43d8-8ae7-a5f815538590.gif)

### 程式：
> ```c++
>void setup()
>{
>  for(int x = 1; x < 9; x++) {
>  pinMode(x,OUTPUT);
>  }
>}
>
>void seg71(int a, int b, int c, int d, int e, int f, int g, int h)
>{
>  digitalWrite(1, a);
>  digitalWrite(2, b);
>  digitalWrite(3, c);
>  digitalWrite(4, d);
>  digitalWrite(5, e);
>  digitalWrite(6, f);
>  digitalWrite(7, g);
>  digitalWrite(8, h);
>  delay(500);
>}
>
>void loop()
>{
>  //    a, b, c, d, e, f, g, h
>  seg71(0, 0, 0, 0, 0, 0, 0, 0); // OFF
>  seg71(1, 1, 1, 1, 1, 1, 1, 1); // 8
>}
> ```


## 4-2 如下圖的Demo, 用七段顯示器, 顯示 . →1→ ... → 9 → 0 → 全滅, 狀態改變的間隔時間為0.5秒

### 電路圖：
> 
### 程式：
> ```c++
> ```
