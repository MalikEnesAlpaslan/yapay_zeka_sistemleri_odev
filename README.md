# Genetik Algoritma ile Fonksiyon Optimizasyonu

Bu proje, belirli kısıtlamalar altında matematiksel bir fonksiyonun maksimum değerini bulmak için Python ile yazılmış basit bir **Genetik Algoritma (Genetic Algorithm)** uygulamasıdır. Algoritma, popülasyon tabanlı bir yaklaşım kullanarak iterasyonlar boyunca en iyi sonucu ($x_1$ ve $x_2$ değerlerini) optimize etmeye çalışır.

## 🎯 Amaç Fonksiyonu ve Kısıtlamalar

Algoritma aşağıdaki fonksiyonu maksimize etmeye çalışır:

$$f(x_1, x_2) = x_1 \cdot x_2 - 0.1 \cdot x_1^2 - 0.1 \cdot x_2^2$$

**Kısıtlamalar:**
* $15 \le x_1 \le 40$
* $5 \le x_2 \le 20$
* $x_1 \cdot x_2 \le 600$

Eğer değişkenler bu kısıtlamaların dışına çıkarsa, fonksiyon ceza puanı olarak `-100` değerini döndürür.

## 🚀 Özellikler

* **Başlangıç Popülasyonu:** Rastgele değerlerle örnekler oluşturulur.
* **Seçilim (Selection):** Her iterasyonda en yüksek skora sahip bireyler ebeveyn olarak seçilir.
* **Çaprazlama (Crossover):** Seçilen ebeveynlerin genleri ($x_1$ ve $x_2$ değerleri) karıştırılarak yeni çocuklar üretilir.
* **Mutasyon (Mutation):** Çeşitliliği sağlamak ve yerel maksimumlara takılmamak için belirli oranlarda rastgele değişimler uygulanır.
* **Görselleştirme:** İterasyonlar sonucunda elde edilen en iyi skorların değişimi `matplotlib` kullanılarak grafikleştirilir.

## 🛠️ Gereksinimler

Bu projeyi çalıştırabilmek için aşağıdaki yazılım ve ortam gereksinimlerinin sağlanması gerekmektedir:
Yazılım Gereksinimleri : 
* Python 3.8 veya üzeri
* Kod, Python’un temel veri yapıları ve standart kütüphaneleri kullanılarak yazılmıştır.
* Matplotlib : Genetik algoritmanın iterasyonlar boyunca elde ettiği en iyi sonuçların görselleştirilmesi için kullanılır.

Kütüphaneyi yüklemek için terminalde şu komutu çalıştırın:

```bash
pip install matplotlib
