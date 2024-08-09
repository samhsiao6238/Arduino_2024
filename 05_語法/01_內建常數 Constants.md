# 常數

<br>

## Constants

1. HIGH | LOW：用於設置和讀取數字引腳的狀態。

    ```cpp
    digitalWrite(13, HIGH); // 設置引腳 13 為高電平
    int state = digitalRead(13); // 讀取引腳 13 的狀態
    ```

<br>

2. INPUT | INPUT_PULLUP | OUTPUT：用於設置引腳的模式。

    ```cpp
    pinMode(13, OUTPUT); // 設置引腳 13 為輸出模式
    pinMode(12, INPUT); // 設置引腳 12 為輸入模式
    pinMode(11, INPUT_PULLUP); // 設置引腳 11 為上拉輸入模式
    ```

<br>

3. LED_BUILTIN：內建 LED 的引腳號，一般為 13。

    ```cpp
    pinMode(LED_BUILTIN, OUTPUT); // 設置內建 LED 為輸出模式
    digitalWrite(LED_BUILTIN, HIGH); // 打開內建 LED
    ```

<br>

4. true | false：布林值，用於邏輯判斷。

    ```cpp
    bool flag = true;
    if (flag) {
        // 執行某些操作
    }
    ```

<br>

## Floating Point Constants

1. 用於表示浮點數常數。

    ```cpp
    float pi = 3.14159;
    double e = 2.71828;
    ```

<br>

## Integer Constants

1. 用於表示整數常數，可以是十進制、十六進制或八進制。

    ```cpp
    int dec = 123; // 十進制
    int hex = 0x7B; // 十六進制
    int oct = 0173; // 八進制
    ```

<br>

___

_END_