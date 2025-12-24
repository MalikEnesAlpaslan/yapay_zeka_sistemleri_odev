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

## Karınca Kolonisi Algoritması ile İstanbul Gezi Rotası Optimizasyonu
Bu projede, İstanbul’da bulunan 15 turistik ve tarihi mekanın tek bir gün içinde en kısa mesafe ile gezilebilmesi amaçlanmıştır. Günlük hayatta bir tur şirketinin ya da bireysel bir gezginin karşılaşabileceği “Hangi sırayla gezmeliyim?” sorusu, bu projede Karınca Kolonisi Algoritması (Ant Colony Optimization – ACO) kullanılarak çözülmüştür.
Projede gerçek mekan isimleri kullanılmış, bu mekanların koordinatları Google Maps Geocoding API üzerinden otomatik olarak alınmış ve aralarındaki mesafeler hesaplanarak en uygun gezi rotası belirlenmiştir.

## Projenin Temel Fikri
Günlük hayatta bir turist İstanbul’a geldiğinde, Ayasofya, Topkapı Sarayı, Galata Kulesi gibi birçok noktayı görmek ister. Ancak bu noktaları rastgele bir sırayla gezmek hem zaman hem de mesafe açısından verimsiz olur. Bu proje, tam olarak bu problemi ele alır ve:
Nereden başlanmalı?
Hangi mekan hangi sırayla gezilmeli?
Toplam yol ne kadar olur?
sorularına algoritmik bir çözüm üretir.

## Nasıl Çalışıyor?
Öncelikle, gezilecek mekanların isimleri Google Maps API’ye gönderilir ve her mekan için enlem–boylam bilgileri alınır. Daha sonra bu koordinatlar kullanılarak mekanlar arasındaki kuş uçuşu mesafeler Haversine formülü ile hesaplanır.
Elde edilen mesafe matrisi, Karınca Kolonisi Algoritmasına giriş olarak verilir. Algoritma, doğadaki karıncaların yiyecek bulma davranışından esinlenerek farklı rota alternatifleri dener. Kısa ve verimli rotalar zamanla daha fazla tercih edilir ve iterasyonlar sonunda en kısa toplam mesafeye sahip kapalı tur elde edilir. Başlangıç ve bitiş noktası olarak Sultanahmet Meydanı alınmıştır.

## Sonuçların Gösterimi
Algoritma çalıştıktan sonra elde edilen en iyi rota, PyDeck kütüphanesi kullanılarak harita üzerinde görselleştirilmiştir. Harita üzerinde:
Ziyaret edilen mekanlar nokta olarak,
Bulunan en iyi rota ise çizgi olarak
gösterilmektedir. Böylece algoritmanın ürettiği çözüm hem sayısal hem de görsel olarak anlaşılır hale gelmiştir.

## Kullanılan Teknolojiler
Bu projede Python programlama dili kullanılmıştır. Gerçek dünya verisi sağlamak için Google Maps API’den yararlanılmış, matematiksel işlemler NumPy ile gerçekleştirilmiş ve sonuçlar PyDeck ile harita üzerinde gösterilmiştir. Proje, Google Colab veya yerel Python ortamlarında çalıştırılabilir.

## Genel Değerlendirme
Bu çalışma, Karınca Kolonisi Algoritmasının teorik yapısının günlük hayatta karşılaşılabilecek bir problem üzerinde nasıl uygulanabileceğini göstermektedir. Tur planlama, rota optimizasyonu ve karar destek sistemleri gibi alanlarda benzer yaklaşımların kullanılabileceğini ortaya koymaktadır.




