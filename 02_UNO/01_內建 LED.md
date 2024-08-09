# 內建 LED

## 說明

1. Uno 開發板上內建的 LED 引腳在 `D13`，可使用 `LED_BUILTIN` 常量來控制這個 LED。

    ```cpp
    void setup() {
        // 將內建 LED 設置為輸出模式
        pinMode(LED_BUILTIN, OUTPUT); 
    }

    void loop() {
        digitalWrite(LED_BUILTIN, HIGH); // 打開 LED
        delay(1000);                     // 等待 1 秒
        digitalWrite(LED_BUILTIN, LOW);  // 關閉 LED
        delay(1000);                     // 等待 1 秒
    }
    ```

<br>

___

_END_
