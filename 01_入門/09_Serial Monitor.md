# Serial Monitor

_CR 和 NL & CR 等設置_

![](images/img_42.png)

<br>

1. No line ending (無行結束)：按下 `ENTER` 時，不會發送任何行結束字元。

<br>

2. Newline (NL)：按下 `ENTER` 時，只會發送一個新行字元（LF，Line Feed）；`LF` 的意思是 `換行`，這是一個 `控制字元`，用於指示文本中的下一個字元應該顯示在下一行，對應的 ASCII 編碼是 `\n（10）`。

<br>

3. Carriage Return (CR)：按下 `ENTER` 時，只會發送一個 `ENTER` 字元（CR，Carriage Return），對應 ASCII 編碼為 `\r`（13）。

<br>

4. Both NL & CR (NL & CR)：按下 `ENTER` 鍵時，會同時發送 `NL` 和 `ENTER` 字元，對應 ASCII 編碼為 `\r\n`（13 和 10）。

<br>

___

_END_