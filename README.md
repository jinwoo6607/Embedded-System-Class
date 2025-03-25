[1~4주차.zip](https://github.com/user-attachments/files/19439838/1.4.zip)
# Embedded-System-Class
![스크린샷 2025-03-25 093713](https://github.com/user-attachments/assets/696543c3-35eb-4016-bb8b-58ef1a9ea834)
![스크린샷 2025-03-25 093721](https://github.com/user-attachments/assets/5faac003-2abb-4bfc-a04f-e86737af47c9)
![스크린샷 2025-03-25 093729](https://github.com/user-attachments/assets/b8b9ccaa-52bb-4579-9fea-4d2842befeb6)
![스크린샷 2025-03-25 093737](https://github.com/user-attachments/assets/2230adce-4006-4174-9cfa-dbd4f7130644)
![스크린샷 2025-03-25 093746](https://github.com/user-attachments/assets/f1e37d27-0f0a-4abc-8560-7c0bb1e6659f)
![스크린샷 2025-03-25 093903](https://github.com/user-attachments/assets/94062ab3-7204-4a22-b27e-d7dc973ec955)
![스크린샷 2025-03-25 093929](https://github.com/user-attachments/assets/9b4e35fc-7cd4-4e37-9cad-23550f333b0a)
![스크린샷 2025-03-25 093948](https://github.com/user-attachments/assets/9a758133-2d80-404e-a696-8045bd3ab8a5)
![스크린샷 2025-03-25 094039](https://github.com/user-attachments/assets/769ea2fa-9aad-4c71-8007-7c4c75619547)
![스크린샷 2025-03-25 094046](https://github.com/user-attachments/assets/4b457921-7f8d-4b20-82ae-bc562389255d)
![스크린샷 2025-03-25 094058](https://github.com/user-attachments/assets/19df5e76-f0ee-4db9-a373-67cdbfeb8448)
![스크린샷 2025-03-25 094103](https://github.com/user-attachments/assets/d2e6be87-67f7-4c1e-946d-9b8165269e59)
![스크린샷 2025-03-25 094112](https://github.com/user-attachments/assets/98e01517-c411-4996-b1b8-3a3528f51f88)
![스크린샷 2025-03-25 094147](https://github.com/user-attachments/assets/505666e6-e101-477d-bc3b-030b91e1fd3d)
![스크린샷 2025-03-25 094213](https://github.com/user-attachments/assets/68607a9d-5cfd-48b1-8b90-12e327131907)




![스크린샷 2025-03-25 105155](https://github.com/user-attachments/assets/eb882fda-f386-4ee7-8e9a-f6e5dd1b3e0c)
![스크린샷 2025-03-25 105204](https://github.com/user-attachments/assets/bb588658-9935-48ee-97af-9a7e0ac54c0b)
![스크린샷 2025-03-25 105214](https://github.com/user-attachments/assets/c63e6462-b3d6-4e1a-bd8b-43f57d941010)
![스크린샷 2025-03-25 105223](https://github.com/user-attachments/assets/64c7896d-3ce9-4c97-943c-c871b58f7f3d)
![스크린샷 2025-03-25 105230](https://github.com/user-attachments/assets/864bbe3c-3214-4bc6-8183-050aa4696fee)
![스크린샷 2025-03-25 105239](https://github.com/user-attachments/assets/d44e7637-020a-42d0-a9ef-422b24c2e113)
![스크린샷 2025-03-25 105508](https://github.com/user-attachments/assets/34c19066-0005-4fb5-8f8d-7beb9e1d67f9)
![스크린샷 2025-03-25 111035](https://github.com/user-attachments/assets/1911ba81-1003-47b2-b4fc-6b2d00fd278f)
![스크린샷 2025-03-25 111041](https://github.com/user-attachments/assets/953367f7-9d30-47b3-94d6-a13b7f1ec012)
![스크린샷 2025-03-25 111047](https://github.com/user-attachments/assets/c946936d-7cde-4ff1-ad38-05189ebcd19f)
![스크린샷 2025-03-25 111221](https://github.com/user-attachments/assets/7d287190-0d3d-460b-8373-f877c62128b7)
![스크린샷 2025-03-25 111819](https://github.com/user-attachments/assets/96142510-9286-421a-a417-dfd1d1a1b637)
![스크린샷 2025-03-25 111221](https://github.com/user-attachments/assets/14c64e03-620c-4914-920a-cfdd71efef04)
![스크린샷 2025-03-25 112155](https://github.com/user-attachments/assets/c7ed4def-e190-4d70-b82a-5f7cfde0c3b1)
![스크린샷 2025-03-25 112513](https://github.com/user-attachments/assets/74daecd2-2833-48bd-b6bc-310a736f6c37)

// LED 핀 설정 (디지털 핀 6번부터 13번까지)
int ledPins[] = {6, 7, 8, 9, 10, 11, 12, 13};
int buttonPin = 2;  // 버튼 핀 (디지털 핀 2번)
int counter = 0;    // 카운터 변수
bool lastButtonState = HIGH;  // 마지막 버튼 상태 (풀업 상태로 시작)

// 버튼을 누를 때마다 카운트를 증가시키는 함수
void setup() {
  // LED 핀들을 출력으로 설정
  for (int i = 0; i < 8; i++) {
    pinMode(ledPins[i], OUTPUT);
  }

  pinMode(buttonPin, INPUT_PULLUP);  // 버튼 핀을 풀업 모드로 설정
}

void loop() {
  // 버튼 상태 읽기
  bool buttonState = digitalRead(buttonPin);

  // 버튼이 눌린 상태인지 확인 (낮은 상태)
  if (buttonState == LOW && lastButtonState == HIGH) {
    counter++;  // 카운터 증가
    if (counter > 255) {  // 8비트 최대값을 초과하면 0으로 초기화
      counter = 0;
    }
    delay(200);  // 버튼이 반복적으로 눌리지 않도록 잠시 대기
  }

  lastButtonState = buttonState;  // 마지막 버튼 상태 업데이트

  // 8개의 LED로 2진수 표시
  for (int i = 0; i < 8; i++) {
    if (bitRead(counter, i)) {
      digitalWrite(ledPins[i], HIGH);  // 해당 비트가 1이면 LED 켜기
    } else {
      digitalWrite(ledPins[i], LOW);   // 해당 비트가 0이면 LED 끄기
    }
  }
}

