# 連接到 Wi-Fi

_以下是連接到 Wi-Fi 的基本腳本，成功連接後會輸出連接資訊。此範例使用 Arduino Mega2560 搭配 Wi-Fi 模組（如 ESP8266）。_

## 設置

_確保 Arduino Mega2560 或 ESP8266 模組正確連接_

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

### 步驟
1. 安裝 ESP8266 庫：
   - 在 Arduino IDE 中，依次選擇 工具 > 開發板 > 開發板管理員。
   - 搜尋並安裝 ESP8266 庫。

2. 連接 ESP8266 模組：
   - 確保 ESP8266 模組正確連接到 Arduino Mega2560。以下是常見的連接方式：
     - RX (Arduino) 接 TX (ESP8266)
     - TX (Arduino) 接 RX (ESP8266)
     - GND 接 GND
     - 3.3V 接 VCC

3. 上傳腳本：
   - 將上面的腳本複製到 Arduino IDE 中。
   - 選擇正確的開發板和序列埠。
   - 上傳腳本到 Arduino Mega2560。

4. 檢查 Serial 監視器：
   - 打開 Serial 監視器，設置波特率為 9600。
   - 應該會看到連接 Wi-Fi 的過程，連接成功後會顯示 IP 地址。

### 注意事項
- 確保 Wi-Fi SSID 和密碼正確無誤。
- 如果使用其他 Wi-Fi 模組，請根據模組的需求修改連接方式和程式碼。