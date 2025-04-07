# led-kayan-efekt ![Wokwi CI](https://github.com/robotdevre/karasimsek/actions/workflows/wokwi.yml/badge.svg)

Bu proje, Arduino Uno kartı ile 8 adet LED’in soldan sağa ve sağdan sola kayan ışık efektiyle yanıp sönmesini sağlar. Bu efekt, genellikle Knight Rider (KITT) gibi görsel geçişlerde kullanılır. Başlangıç ve orta seviye Arduino öğrenimi için uygundur.

---

## 🔧 Kullanılan Malzemeler

- Arduino Uno  
- 8 x LED (Kırmızı)  
- 8 x 220 Ohm direnç  
- Breadboard  
- Jumper kablolar  

---

## 🎯 Proje Amacı

- Diziler (arrays) ile çoklu pin kontrolü öğrenmek  
- `for` döngüsü ile LED sıralaması yapmak  
- Soldan sağa ve sağdan sola kayan efekt mantığını kavramak  
- Görsel efekt oluşturmak için `delay()` fonksiyonunu kullanmak  

---

## 📷 Devre Şeması

📁 `diagram.json` dosyasında Wokwi uyumlu devre şeması bulunmaktadır.  
🔗 [Projeyi Wokwi'de görmek için tıklayın](https://wokwi.com/projects/426609331783848961)

---

## 💡 Kod

```cpp
int ledCount = 8;              // LED sayısı
int leds[] = {2, 3, 4, 5, 6, 7, 8, 9}; // LED pinleri

void setup() {
  for (int i = 0; i < ledCount; i++) {
    pinMode(leds[i], OUTPUT);
  }
}

void loop() {
  // Soldan sağa geçiş
  for (int i = 0; i < ledCount; i++) {
    digitalWrite(leds[i], HIGH);
    delay(100);
    digitalWrite(leds[i], LOW);
  }

  // Sağdan sola geçiş
  for (int i = ledCount - 2; i > 0; i--) {
    digitalWrite(leds[i], HIGH);
    delay(100);
    digitalWrite(leds[i], LOW);
  }
}
``` 
---

## 📫 Benimle İletişime Geç / Takip Et

Eğer proje hakkında bir fikrin varsa, soruların olursa ya da sadece selam vermek istersen; aşağıdaki kanallardan bana ulaşabilir ya da sosyal medya hesaplarımdan takip edebilirsin:

- 📧 [E-posta](mailto:info@robotdevre.com)  
- 📷 [Instagram](https://www.instagram.com/robotdevre/)  
- 🌐 [Web Sitesi](https://robotdevre.com/)  
- 🎥 [YouTube](https://www.youtube.com/@robotdevre)  
- 💼 [LinkedIn](https://www.linkedin.com/in/ugur-kerim-sirke/)  
- 🐦 [X (Twitter)](https://x.com/robotdevre)
