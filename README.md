# Çarpım Tablosu Alıştırma

Çocukların çarpım tablosunu çalışması için hazırlanmış tek sayfalık web uygulaması. Kurulum, bağımlılık veya internet bağlantısı gerektirmez; tek bir `index.html` dosyasından oluşur.

## Kullanım

1. `index.html` dosyasını tarayıcıda açın (çift tıklamak yeterli).
2. Üstteki **1–10** butonlarından çalışmak istediğiniz sayıları seçin. Birden fazla sayı seçilebilir; **Hepsi** butonu tüm sayıları seçer.
3. Seçilen sayılarla oluşturulan 200 soru ekrana gelir. Her sorunun `=` işaretinden sonraki kutusuna cevabı yazın.
4. **Yeni Çalışma** butonu ile yeni bir karışık soru dizilimi başlatın.

Telefonda denemek için bilgisayarda basit bir sunucu başlatıp aynı ağdan adrese girebilirsiniz:

```
python -m http.server 8080 --bind 0.0.0.0
```

Ardından telefonda `http://<bilgisayarın-yerel-ip-adresi>:8080` adresini açın.

## Özellikler

- **200 soru, tek sayfada:** Sorular `3×4=[ ]` biçiminde, ızgara düzeninde listelenir.
- **Seçilebilir sayılar:** Yalnızca seçilen sayıları içeren çarpmalar (1–10 ile) üretilir. Sayı seçimi değiştiğinde liste hemen yenilenir.
- **Karışık sıralama:** Sorular rastgele sıralanır, çarpanların yeri de rastgele değişir (3×4 veya 4×3). Aynı soru art arda gelmez.
- **Anında geri bildirim:** Doğru cevapta yeşil ✓, yanlış cevapta kırmızı ✗ görünür. Yanlış cevap silinip yeniden yazılabilir.
- **Serbest sıra:** İstenen soru tıklanıp cevaplanabilir; doğru cevaptan sonra imleç otomatik olarak sonraki kutuya geçer (Enter ile de geçilir).
- **Sayaç:** Doğru, yanlış ve toplam soru sayısı üst barda gösterilir.
- **Mobil uyumlu:** Telefonda dikey ve yatay kullanıma uygundur. Ekran genişliğine göre sütun sayısı değişir (10 / 8 / 6 / 4 / 3), dokunmatik ekranlarda butonlar büyür, sayısal klavye açılır.

## Teknik Notlar

- Saf HTML, CSS ve JavaScript; harici kütüphane yoktur.
- Cevaplar kaydedilmez; sayfa yenilendiğinde veya **Yeni Çalışma**'ya basıldığında sıfırlanır.
