# 連接到 Wi-Fi

_以下是連接到 Wi-Fi 的基本腳本，成功連接後會輸出連接資訊。此範例使用 Arduino Mega2560 搭配 Wi-Fi 模組（如 ESP8266）。_

<br>

## 設置

_確保 Arduino Mega2560 或 ESP8266 模組正確連接_

<br>

## 腳本

1. 這段腳本會嘗試連接到指定的 Wi-Fi 網路，並在連接成功後輸出連接資訊。

    ```cpp
    // ESP8266 的 Wi-Fi 庫
    #include <ESP8266WiFi.h>

    const char* ssid     = "SamHome";
    const char* password = "sam112233";

    void setup() {
      // 初始化 Serial 連線
      Serial.begin(9600);
      delay(10);

      // 開始連接 Wi-Fi
      Serial.println();
      Serial.println("Connecting to ");
      Serial.println(ssid);

      WiFi.begin(ssid, password);

      while (WiFi.status() != WL_CONNECTED) {
        delay(500);
        Serial.print(".");
      }

      // Wi-Fi 連接成功
      Serial.println("");
      Serial.println("WiFi connected");

      // 輸出 IP 地址
      Serial.println("IP address: ");
      Serial.println(WiFi.localIP());
    }

    void loop() {
      // 此範例中，loop() 不執行任何操作
    }
    ```

<br>

___

_END_