# 嵌入式系統與實習

## 加入一個新建的LED.md的檔案, 並完成以下LED應用實作

### 說明：

> 第13腳位的外部為LED與內部LED,1秒亮,另1秒暗


### 程式：
```c++
// C++ code
//
void setup()
{
  pinMode(13, OUTPUT);
}

void loop()
{
  digitalWrite(13, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(13, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
```
