# Classification via Hybridization of CNN Models
## Proje Tanıtımı
Bu proje, Convolutional Neural Networks (CNN) ve diğer makine öğrenmesi algoritmalarını birleştirerek görüntü sınıflandırma problemlerini çözmeyi amaçlamaktadır. Özellikle Malaria ve MNIST veri setlerinde, CNN ile K-Nearest Neighbors (KNN), Support Vector Machines (SVM) ve Long Short-Term Memory (LSTM) algoritmalarının hibrit kullanımı araştırılmıştır. Proje, hibrit modellerin performansını değerlendirmek ve bu modellerin etkisini incelemek amacıyla hazırlanmıştır.

## Model Mimarisinin Görseli

Aşağıda, proje kapsamında kullanılan hibrit modellerin genel mimarisini gösteren bir görsel bulunmaktadır:

  <p align="center">
    <img src="https://github.com/user-attachments/assets/af140a3c-32c5-44e4-8888-3d706d50fd05" alt="Malaria Parasitized Görselleri" width="600"/>
    <br>
    Şekil 1: Projede kullanılan CNN-KNN, CNN-SVM ve CNN-LSTM Hibrit Modellerinin Genel Mimarisi.
  </p>

## Kullanılan Teknolojiler
- **Convolutional Neural Networks (CNN):** Görüntü verilerinden özellikleri öğrenmek için kullanılan temel derin öğrenme yapılarından biridir.
- **K-Nearest Neighbors (KNN):** Özellik vektörlerinin sınıflandırılması için kullanılan basit bir makine öğrenme algoritmasıdır.
- **Support Vector Machines (SVM):** Sınıflandırma problemlerinde kullanılan ve yüksek boyutlu veri setlerinde iyi performans gösteren bir algoritmadır.
- **Long Short-Term Memory (LSTM):** Zaman serisi verilerinde ve ardışık verilerde etkili olan bir tür RNN'dir, ancak bu projede sadece CNN-LSTM hibritleri üzerinde çalışılmıştır.

## Veri Setleri

- **Malaria Veri Seti:** Malaria enfekte hücrelerini içeren mikroskop görüntülerinden oluşur. Bu veri seti, hastalığın teşhisinde kullanılabilecek modellerin eğitilmesi için kullanılmıştır.

  <p align="center">
    <img src="https://github.com/user-attachments/assets/d9edf7f9-ea62-46b9-84f4-27818d38d64e" alt="Malaria Parasitized Görselleri" width="600"/>
    <br>
    Şekil 2: Malaria Veri Setindeki Parasitized Sınıfından Örnek Görseller.
  </p>

  <p align="center">
    <img src="https://github.com/user-attachments/assets/4e195421-0440-4888-8431-89fad80d2b60" alt="Malaria Uninfected Görselleri" width="600"/>
    <br>
    Şekil 3: Malaria Veri Setindeki Uninfected Sınıfından Örnek Görseller.
  </p>

- **MNIST Veri Seti:** El yazısı rakamların yer aldığı bir veri setidir. Genellikle yazı tanıma ve görüntü sınıflandırma problemlerinde standart test veri seti olarak kullanılır.

  <p align="center">
    <img src="https://github.com/user-attachments/assets/52d386f0-88bc-428a-bb1f-b5c2a7551ae1" alt="MNIST İlk 10 Görüntü" width="600"/>
    <br>
    Şekil 4: MNIST Veri Setindeki İlk 10 Görüntü.
  </p>

## Model Mimarisinin Açıklanması
Projede kullanılan CNN mimarileri, görüntü özelliklerini çıkarmak için derin katmanlar içermektedir. Bu CNN modellerinin çıktıları, KNN ve SVM algoritmalarında özellik vektörleri olarak kullanılmaktadır. LSTM ile hibrit model, zaman serisi verilerini analiz etmek amacıyla kullanılmaktadır. Aşağıda kullanılan model mimarilerinin kısa açıklamaları verilmiştir:

- **CNN-KNN:** CNN, görüntü özelliklerini çıkarır ve bu özellikler KNN algoritmasına giriş olarak sağlanır.
- **CNN-SVM:** CNN tarafından çıkarılan özellikler, SVM algoritması tarafından sınıflandırılır.
- **CNN-LSTM:** CNN, görüntü özelliklerini çıkarır ve bu özellikler LSTM ağına aktarılır, böylece zamansal ilişkilere dayalı sınıflama yapılır.

## Sonuçlar ve Performans Karşılaştırmaları
Projede farklı hibrit modellerin performansı değerlendirilmiştir. Aşağıda her bir hibrit modelin doğruluk, hassasiyet ve geri çağırma değerleri verilmiştir:
1. **MNİST VERİ SETİ SONUÇLARI**
- **CNN-KNN:** Eğitim verisi doğruluğu %0.999, test verisi doğruluğu %0.992.
- **CNN-SVM:** Eğitim verisi doğruluğu %0.997, test verisi doğruluğu %0.991.
- **CNN-LSTM:** Eğitim verisi doğruluğu %0.998, test verisi doğruluğu %0.989.
2. **MALARİA VERİ SETİ SONUÇLARI**
- **CNN-KNN:** Eğitim verisi doğruluğu %0.992, test verisi doğruluğu %0.949.
- **CNN-SVM:** Eğitim verisi doğruluğu %0.995, test verisi doğruluğu %0.946.
- **CNN-LSTM:** Eğitim verisi doğruluğu %0.995, test verisi doğruluğu %0.957.


Performans sonuçları, hibrit modellerin her birinin güçlü yönlerini ve sınırlamalarını anlamak için kıyaslanmıştır.


