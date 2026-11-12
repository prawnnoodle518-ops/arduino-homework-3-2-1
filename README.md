# arduino-homework-3-2-1
/*
  Button
  按住按鈕時，LED 燈會亮起；放開按鈕時，LED 燈會熄滅。
*/

// 設定腳位代號
const int buttonPin = 2;     // 按鈕的 In 腳接 D2
const int ledPin =  3;       // LED 接 D3

// 變數會改變：
int buttonState = 0;         // 用來記錄按鈕狀態的變數

void setup() {
  // 將 LED 腳位設定為輸出模式：
  pinMode(ledPin, OUTPUT);
  // 將按鈕腳位設定為輸入模式：
  pinMode(buttonPin, INPUT);
}

void loop() {
  // 讀取按鈕的狀態值：
  buttonState = digitalRead(buttonPin);

  // 檢查按鈕是否被按下
  // 如果是高電位 (HIGH)，代表按鈕被按下了
  if (buttonState == HIGH) {
    // 點亮 LED 燈：
    digitalWrite(ledPin, HIGH);
  } else {
    // 熄滅 LED 燈：
    digitalWrite(ledPin, LOW);
  }
}
